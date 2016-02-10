---
layout: post
title: Android Studio and Java
---

10:51 AM
--------
Have been trying out different ways of implementing the Map Screen (a 60x60 character grid); the concern is whether or not we can build it such that the screen can update rapidly (doesn't delay: that would be unacceptable for users).
So, my first implementation was just using a single dimensional character array (of "a"), and displaying that in a TextView. When a button is pushed, the app calls the method "changeMap" which steps through a loop that takes each character in the array and appends it to a String, which the TextView's content is then set to (so the TextView is updtaed on each iteration of that loop, i.e. as many times as there are characters in the array).
Obviously, this was super slow. Running it on a Google Nexus 7, the screen would skip around 150 frames each time the button was pressed (and Android Studio would tell me my main thread was overwhelmed).
After checking in with the group, Amir suggested using StringBuilder. The logic of the program is pretty much the same (append to the StringBuilder object for each char, then set TextView to StringBuilder at the end -> only need to update TextView once). This helped a lot (only about 30 or 40 frames being skipped), but still pretty bad (and this was runnnig them on smaller arrays than what the actual game would be).
So now, I'm going to try it with multithreading and a 2-d array (as opposed to previous implementations 1-d).


Simple string conatenation:
03-13 11:38:51.959    1902-1902/com.example.reinatomlinson1.myapplication I/Choreographer﹕ Skipped 295 frames!  The application may be doing too much work on its main thread.
03-13 11:39:04.922    1902-1902/com.example.reinatomlinson1.myapplication I/Choreographer﹕ Skipped 183 frames!  The application may be doing too much work on its main thread.



Stringbuilder:
03-13 15:32:17.488    1936-1936/com.example.reinatomlinson1.myapplication I/Choreographer﹕ Skipped 63 frames!  The application may be doing too much work on its main thread.

Realized I was updating the TextView inside a for-loop; now that that's moved outside of the loop, it looks like the 60x60 grid is updating at a perfectly fine speed!

18:21 PM
--------
Going to finish out the semester using plain Java/Android controls, then translate to Ruby and compile and run in RubyMotion; then do a version with Cocos2dx (possibly over the summer). Michael had been working on Cocos2dx as an alaternative to using plain Java/Ruby controls (to emphasize RM's cross-platform capabilities), but due to time constraints (semester ending in a month or two), we want to focus on getting a game moving. Since the plain controls seem to be coming along quicker (plus three of us are working in it, and only Michael knows anything about Cocos2dx right now), that's what we're going to focus on during the school semester. We may continue working with Amir after the semester ends, and he has a few other games that need porting, so the opportunity to use Cocos2dx in RubyMotion is still there.
For the next week, I'm going to be working on building the real map screen (not just a prototype to check viability).