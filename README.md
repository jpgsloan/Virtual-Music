Virtual-Music
=============

An attempt at making music more tangible.

DEMO VIDEO: http://www.youtube.com/watch?v=NtcoviDCCwQ&feature=youtu.be

  For this project, my real goal starting out was just to experiment with 3d sound. So I started without an idea and kept playing around with various techniques of using different input devices and how they can be used with 3d sound. I ended up with this idea: it would be cool to be able to walk around inside of a music piece. Or even more so, being able to have the music more interactive with its listener, where the actual piece is influenced by those listening. It is also a way for people to experience music unlike they do on a daily basis. Whether you are listening on headphones or watching a live performance, the music is statically in front of you and that’s how you get to hear it. But for the musician, such as a member of a choir, they get a whole different experience of what it sounds like simply by being on stage, immersed in the sound. This was the inspiration to my project and this is what I came up with.
  
First off, you can “place” an instrument using any of 3 buttons on your iphone screen (one for each instrument I made for this demo). When an instrument is placed it will always remain there even if you walk away from it. The idea is that if you had several different instruments or tracks (like guitar, keys, anything) you could place them all relative to each other so that you could walk from one to the other to hear what that is like. To do this I have two parts in my patch. 
	
The first takes into account which direction you are facing using the iPhones compass. This works such that if you are looking at a placed instrument it sounds like it and if you turn away it still sounds like the instrument is coming from the same direction (you look to the right, the sound is more in your left ear). 
	
The second part is locating how far away you are from an instrument. This turned out to be really difficult and I only had limited success (very limited…). This is because most methods for determining local distance with sensors are very inaccurate (gps, integrating accelerometer data, blu tooth all do not work). So what I did was use the accelerometer to count your steps, paired with the direction you faced when stepping, to calculate how far in the x and y direction you are currently. I think this was the most challenging part of my patch and can be examined in the subpatch “xy-coords” and a little more in the instances within vbap. As well, I’m still not sure this is the best approach but it is good enough for a demo. I plan to work on this as a continued project for a while and am looking into some newer technology for calculating local position such as ibeacons. 
	
I used the app gyrOSC for iPhone. If you really want to test my patch it should be easy to set up just by opening it up and following some of the instructions I give. But the app is $1 and you may not have an iPhone!! Thus, I have also made a short demo video of the patch in action, which shows some features as well as 3 instrument sounds I created as examples. I plan to make my own basic iphone app for this someday in the future. I recorded the video and sound simultaneously and then synced them using final cut. In the video I put the iphone in my front pocket because that is where it works best from as far as recognizing steps.
	
	Thanks for reading!
	-John Sloan
