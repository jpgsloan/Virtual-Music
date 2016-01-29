Virtual-Music
=============

An attempt at making music more tangible.

DEMO VIDEO: http://www.youtube.com/watch?v=NtcoviDCCwQ&feature=youtu.be

Listening to music on headphones is a static experience. The music is always at your ears even when you turn your head, and that’s the only way you get to hear it. But for many musicians, like the members of a choir, they get a whole different experience of what music sounds like. They are immersed in the sound, and hear it differently depending on where they stand in the room. For this project, I attempted to bring this organic and tangible quality to recorded music. I wanted to make it possible to walk around inside a piece of music to listen from different perspectives. This also opened the door for making music that interacts with its listeners. Here's what I came up with:
  
With this Max patch, you can “place” an instrument using any of 3 buttons on your iphone (one for each instrument I made for this demo). When an instrument is placed it will always remain there even if you walk away from it. The idea is that if you had several different instruments or tracks (like guitar, keys, or drums) you could place them all relative to each other so that you could walk from one to the other to hear what that sounds like. For this demo, I chose to make the instruments more interactive, and they each change as the user moves in different ways.

To do this, I have two parts in my patch. The first takes into account which direction you are facing using the iPhone's compass. If you are looking directly at a placed instrument, it sounds like it. If you turn away, it sounds like the instrument is still coming from its original direction rather than following your ears like conventional headphones (you look to the right, the sound is more in your left ear). 
	
The second part is locating how far away you are from an instrument. This turned out to be more difficult and I only had limited success. Most methods for determining local distance with sensors are very inaccurate (gps, integrating accelerometer data, blu tooth are all fairly inaccurate for small distances). I chose to use the iPhone's accelerometer data to count steps, paired with the direction you faced when stepping. Using this data, it is possible to calculate how far in the x and y direction you currently are from the placed sound. In the future this approach could be replaced by computer vision to more accurately calculate local distance. But for the purposes of this demo, I did not want to introduce more hardware. 

For sending iPhone sensor data to Max, I used the gyrOSC app. For the demo, I recorded the video and audio simultaneously and then synced them using final cut. 
	
	Thanks for reading!
	-John Sloan
