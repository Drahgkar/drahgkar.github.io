---
layout: post
title: OSDFcon Presentation
---
My good friend Andrew Quill and I had the honor to present our talk _Farming the Loot Cave: Threat Hunting in Memory with the Volatility Framework and Big Data_ at OSDFcon today and unveil our technical addon for Splunk that allows you to ingest Volatility 2.x results data. May I present [TA-Volatility](https://splunkbase.splunk.com/app/3919)! Here's the [source](https://github.com/mutedmouse/ta-volatility) if you're more interested in that than the Splunk app.

We created TA-Volatility because memory analysis has become a key way to hunt and track malware and advanced persistent threats (APTs). It's more important than ever to arm your analysts and investigators with better tools and capabilities for memory analysis.  In our talk we showed how to use this app to get your Volatility outputs into Splunk and create simple, yet effective, dashboards to visualize critical artifacts and rapidly pinpoint threats in memory.

TA-Volatility is also extensible, so you can ingest data from additional Volatility and community plugins if the capability isn't already included.  Here's the slide deck we presented if you're curious.
<div><iframe class="speakerdeck-iframe" frameborder="0" src="//www.osdfcon.org/presentations/2018/Andrew-Quill-Farming-the-Loot-Cave.pdf" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true" style="border: 0px; margin: 0px; padding: 0px; border-radius: 5px; width: 710px; height: 430.37499999999955px; background: transparent;"></iframe></div>
