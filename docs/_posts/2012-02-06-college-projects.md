---
layout: post
title: College Projects
---

During my time in college there were a few projects I was involved with, some as requirements for graduation, others as attempts to improve things for online students at my school.  I'll go through and talk a little about each one below.

## Parallel Universe ([www.puniverse.org](https://web.archive.org/web/20110923115628/http://www.puniverse.org/))
<img align="left" width="200" height="200" src="/public/images/paralleluniverse.png">
I actually took over and recreated Parallel Universe from a prior University of Advancing Technology student.  It was intended as a club aimed towards online students, where they could collaborate and socialize with each other and the campus students.  As a project, it was my first attempt at managing a web server, club, and forum all at the same time.  I started off running Parallel Universe on a CentOS 4.5 box where I had to learn a lot about how to manage Linux and all of the other software required in running a website.  This includes Apache, MySQL, and the SimpleMachines forum software.

Learning how to properly set up Apache for a basic website took me about two weeks initially.  However, with each upgrade of the site software, that time shrank by a decent amount of time.   Figuring out and learning how MySQL worked was another task entirely.  I spent many an hour using Google to track down the proper way to set it up for tasks such as this one without messing it up first. The SimpleMachines software was mostly just HTML, which while I could read it, I didn’t always understand what it was doing.

Eventually, I migrated Parallel Universe to CentOS 5.2 and my understanding of how the underpinnings of a server running a website on Linux increased by a couple orders of magnitude. Setting up Apache, MySQL, and SimpleMachines was a bit easier and only takes me a couple hours to get the groundwork laid out with an hour to two more depending on what kind of tweaking I wanted to do to the website.

## Mint-Firix Forensic DVD
The Mint-Firix project came about as a result of a discussion I had with another classmate in one of my security related classes.  At that point we were trying to use a copy of the Forensic and Incident Response Environment (F.I.R.E.) live-cd and found it to be a bit clunky and not always working right.  I took a newer and more stable Linux distribution, Linux Mint, and tried to create my own live-cd that included the tools that F.I.R.E. had and a few that were included on the Helix3 live-cds.  For lack of a better idea, I called it Mint-Firix.  After going through the process and eliminating packages we didn’t need and adding the ones we wanted, the live-cd turned out quite well for a first try.

I gave a copy of the live-cd to one of my classmates that was interested in seeing if it worked and he reported that it seemed to boot up and work fine in a virtual machine, but the tools weren’t as intuitive as we wanted them to be.  At this point, Mint-Firix needed some tweaking on some of the packages that didn’t quite integrate as well as I had hoped and it needed an update to the user interface. Ideally it would have been something different than the original Mint interface. Basically it needed a facelift and some testing with the packages I included.

## Project Corezashi - Senior Innovation Project ([www.corezashi.com](https://web.archive.org/web/20110208051614/http://corezashi.com/))
<img align="left" width="200" height="25" src="/public/images/corezashi-trimmed.jpg">
<div style = "text-align: center">Project Corezashi was intended to be a method for proactively protecting computing environments from malware in real-time utilizing neural networks</div> and artificial intelligence.  The basic thought behind the project was to analyze all of the data we have available to us regarding malware in general and each piece specifically with neural networks looking for patterns that can be acted upon. Once those patterns had been identified, artificial intelligence equivalent to a modified expert system would have been used to automatically generate countermeasures.  After such countermeasures had been identified, they would have been fed back through the neural networks as part of the data for verification and improvement. 

I went through a few different iterations on the base idea for this project trying to figure out which language to write it, python or go.  Ultimately, I decided to use python, but I personally didn't have the required knowledge or skill in python at that point to do much more than a couple token files for downloading some information from ExploitDB and attempting to normalize the data. 

UPDATE 3/15/2023 - This idea is still a bit of pet project that I'd love to make some progress on, especially with the latest advancements like GPT4.
