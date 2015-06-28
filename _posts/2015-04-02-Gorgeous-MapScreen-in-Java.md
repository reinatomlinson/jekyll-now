---
layout: post
title: Gorgeous Map Screen in Java, Ctd.
---

###Continuing on Beefing up MapScreen

The projected move to Ruby last week was hugely bogged down by a mess of conflicting responsibilities, so I'm still working in Java.

After team retro at Central Market:
More aggressive move to Ruby. Since the semester is coming to an end, we've reevaluated priorities and decided to shoot for functional screens in RubyMotion, working together, by 24 A


####10 April:
Apparently there are no chars in Ruby, only Strings. So this is changing how I will implement the maps... It's looking like now I'll have a String for each map (Terrain and Landscape), and maybe split it at the newline in a loop as I add it to the corresponding textviews?

####15 April:
Fixed problems (for now) with height issues using monospaced fonts in Android. Not sure if this is a problem in iOS, as Amir has not addressed it or mentioned at all (seemed that using a monospace font in iOS automatically makes the text occupy a square space? Will ask at the hackathon tonight.) What I have working now is via the xml attribute "android:letterSpacing" but it isn't clear if that is also affecting the height?

Since that is working now, going to move to two-way scrolling. From what I've seen online, it isn't yet a well-addressed issue. I don't think anyone has figured out (or posted anything online about it anyway) how to implement a good scroller that accommodates diagonal scrolling. I think there is a a way to make it such that you can scroll either vertically or horizontally, but only one of those at a time. There may be some kind of solution with drag detection, but I have yet to look more into that. The implementation I pursue (for now; I may come back to this if it isn't resolved very nicely) will depend on what Amir wants, since he understands the underlying needs of the game and will be able to advise on which implementation will fit best with the rest of the pieces.

####At Central Market Hackathon
Reading a promising blog post at <http://web.archive.org/web/20131020193237/http://blog.gorges.us/2010/06/android-two-dimensional-scrollview>
Will have to look into performance issues and API compatibility.
It's a custom class, so I'm not sure if it will compatible in RubyMotion. And, I believe it only enables both horizontal and veritcal scrolling, but still no diagonal scrolling.

Just talked to Amir and he said this should be fine to use. May email the creator just to be safe!

