
Projects found at: https://www.shadertoy.com/results?query=kMiller



Implementation

Paw Metaballs:

I started by drawing a larger black circle in the middle and then assigning positions to the five small balls with an offset from the center. Then I rotated the ring of small balls about the center counter clockwise and once that looked ok, rotated the points again so that they were rotating about themselves clockwise. Then I used smooth min to make the balls blend in and out with the static ball in the middle

Spindle of Death:

First I drew one thin torus facing completely square with the z axis then took its position and successively rotated it by 22.5 degrees each time to get 8 rings. Then I went back and made it so that each ring was drawn with its own small white ball (so that the balls rotated around the correct axes). To make the balls move I created a z rotation matrix and rotated each ring/ball set at offset times for the appearnace that the balls were travelling around the rings but after messing with the time function a bunch still couldn't quite get the ball timing right for the affect in the example

Tri-colored cube:

After ray marching a plain cube, I split time into distinct intervals for color rotation, block rotation, and static scenes. For color rotation I defined the colors to be dependent on their angle from the origin and rotated them by 120 degrees based on time to get them to switch. The trickier part was getting the colors to move with the cube on the object's rotation so I tried mapping colors to the cube's normal in the hope that when the cube moved, the colors would move with it. This didn't seem to be working since the colors flop when the cube is rotated so I tried mapping the normals based on a static cube function (where the input pos wasn't dependent on time) but this gave an even weirder affect so I stuck with the original plan and have yet been able to figure out a way to fix that issue.