---
layout: post
title: Getting the Code Rolling
---

###7 March 2015

Group meeting/hackathon:
Working from Central Market. Still working on getting the HelloWorld sample app (in RubyMotion)running on a device. Everything is installed (I think).
To install: first of all, the RubyMotion tutorial is a great help, so that should be the starting point for anyone. 

Some notes: 
- To create a .profile file (if needed): "touch .bash_profile". Then open and add the two lines as directed in the RubyMotion guide. I still don't exactly understand what a .bash_profile file is, what the difference is from a .profile file, etc. Shaurya helped me get set up. Will try to do some personal research later.
- There was some confusion/mixup with the downloading/opening of the NDK. Follow RubyMotion instructions and not those on the Android site. Also, use your head and don't just copy the instructions exactly (where it specifies file locations may not match where it is in your machine). But it's not really an issue.

Right now, still having an issue getting the sample app running on the device. When I run "rake device", it runs one line of "Install" tells me:

ERROR! Cannot install an app built for API version 21 on a device running API version 19

When I run "rake", it runs one line of "Install" tells me:

error: device not found
- waiting for device -

Brainstormed with Shaurya, installed the proper APIs (either run the command "~/android-rubymotion/sdk/tools/android", but of course the path leading up the "android" at the end will depend on where you actually saved the content). Sample apps (both RubyMotion's and Shaurya's ADR one run beautifully!).

Time to get coding!
Tonight, I'm working on seeing how plain RubyMotion handles changing and updating the 60x60 character array that makes up the map.