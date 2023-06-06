---
layout: post
title: Malicious U2F/FIDO keys
---

I wanted to discuss an idea I had that morphed a bit during my initial discussions, into something that was demonstrated by the fine people at BHIS in 2019.  First, I'll give a brief overview of Black Hill's article and then I'll flesh out my idea.

## Black Hills - Weaponizing the Yubikey

In 2019 Black Hills wrote a blog post about [co-opting a vulnerable Yubikey](https://www.blackhillsinfosec.com/how-to-weaponize-the-yubikey/). The article describes the use of the Yubikey personalization tool, captured key codes, and innovative techniques to transform the Yubikey into an attack tool. Though the technique did not yield desired results, it has the benefit of being unobtrusive and less likely to raise suspicion during pentests.

## A Different Weaponization

My idea aims to take this concept further and could prove to be more challenging for defenders if successfully implemented.

First, a little primer on U2F/FIDO tokens. Actually, the FIDO Alliance already provides a [primer on FIDO](https://fidoalliance.org/how-fido-works/), I suggest you check it out before continuing.

Now for the idea I had a couple days ago; let's get to it!  Suppose we create a binary that is environment/context aware. This isn't a novel concept as it's been done before by multiple instances of malicious code.  This binary will run in the same manner as any other code but will display an authentication window asking for a U2F/FIDO/Yubikey token the moment an attempt is made to debug, reverse engineer or modify it in any way.  As a necessity this would have to be self-contained as to not give away C2 infrastructure with any kind of network traffic. Incorrect input into the authentication window results in scrambled code, polymorphism, potential retaliation/alternate infection from the binary.

As far as I'm currently aware, the U2F/FIDO framework is relatively small and supported almost everywhere on the majority of operating systems.  Including the framework and making it self-contained shouldn't increase the size of the binary appreciably, I think. We know this can be done because a Yubikey allows you to authenticate to a local machine without reaching out to a AD/LDAP service. My understanding is that the installed Yubikey package is what would authenticate you locally.

Now, if you could actually implement something like this, a defender is going to either enjoy tearing it apart or have quite an ordeal on their hands when they come across it, maybe both. Couple this capability with a ransomware engine and you'd have a nigh invulnerable piece of malicious logic. So the question then becomes; how would we detect or deal with this type of scenario? 

Some initial analysis, assuming you're on a Linux machine, is to perhaps run `lsof -p` against the PID associated with the binary and see if it has any file descriptors open. But if the binary is not communicating outside of itself, would you be able to see anything of use? The next logical thought is to monitor changes to the filesystem or watching for exchanges between the binary and `/dev/usb/`.

Things get really interesting when you take into account the [Virtual FIDO](https://github.com/bulwarkid/virtual-fido) project. This could really open up some interesting research.

Ultimately, there are some things I don't have an answer to right now.  Is it possible to identify a key/token without having access to a Windows registry or finding the device information in the logs on Linux?  When asking for authentication, does the process know or leak information about a specific expected key/token instead of just passing provided authentication information to the authentication process? 
