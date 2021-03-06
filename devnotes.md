# Notes for Mapaga

A series of experiments linking together Phaser.io, a javascript game engine, with Tone.js, a javascript music library.

Watched a bit of Bit Trip runner for inspiration after a tip from Alex last Thursday (27 April, 2017)

World moves under p2 physics - camera and large world

Tilemap gravity good for world and camera too

sprites/out of bounds.js has example of onOutOfBounds on sprites

## May 1, 2017

exp\_6 tagged; the most effective rhythm was in fact when balls were sent out straight, and bounced back against themselves in various ways. A possible variation on this:

The paddle just returns the balls; if it's not there, then the beats are removed by going out of the world.

Pressing a key adds more beats
tagged as exp\_7

## May 3, 2017

exp\_8 at the moment; paddle deletes balls. Adjusted the speed of the ball to match a bar across (or up and down) the screen. Different speeds likely to mean bounces have a different phase surely? Try snares with one speed (say 75% of current) versus the bass part. Could even scale it across the screen horizontally for experiments.

Next steps:

Just bounce off the walls. Doesn't sound as easy as initially thought; need to add some sort of rectangle around the edge that acts as a sprite. Look up how an image can be scaled to the size of the screen.

Feels like time to make a game. Balls with different velocities at a speed around the current one (a full screen width or height per bar) can make the best sounds, especially if the pitch grid is set to a particular set of chord tones (tried C6, C7).

Patrick saw the balls in motion and seemed interested; he wanted to move the paddles around and dodge balls.

That's the game idea. Move a square (modified paddle) from bottom left to top right. Dodge balls. Get hit by a normal ball, square gets bigger (and ball disappears?). Things get a bit more active every 2 bars. Every now and again a random ball flies through. If that hits the square, it's game over.

One thing - I've done a few days now without testing on mobile. From past experience that's not smart, so get back to it. Always test on mobile. Every day. Build for mobile.

### Towards exp_9

* Add movement buttons or joystick, buttons for adding balls, and test on mobile devices. See how many balls before it all wigs out.

* If all ok, remove vertical paddle, and start on game initial ball creation. Start button. Randomize balls, and increase intensity every 2 or 4 bars.

* Get the square (need a name for it) moving through the field

* On collision increase player sprite size and delete ball

* Try adding nexusUI controls for testing purposes in the browser (underneath, maybe)

### May 5 2017

Some performance problems on the Samsung Tab A. Audio in Tone barely working at
all. Tried latency fixes on Tone.context.latencyHint to no avail. The only
thing that seemed to make a difference was getting rid of the PolySynth
(converting back to MonoSynth). Leave it for now, and return later to solve it.
Things to try might be just setting up a Tone project without Phaser, trying
samples as ogg or mp3, using parts instead of quantized scheduled evetns on the
timeline, trying to schedule events further in the future. Bear in mind,
though, that not even the click track was working. That's odd in itself. Should
also try as many other devices I have to hand as well - Mareta's tablet,
Patrick's, other phones.

#### Plan:
Try timing with Tone.Player synced to transport. No matter what happens, move on with game idea:
- Initial ball creation
- increase of intensity
- square moving
- collision


### Mon 8 May 2017 

Tried on Rob's Nexus 7 and performance good.

Tagged as exp\_9. Can now move on to making the game aspect of it more
complete. Some sort of explosion or effect when the paddle hits the edge, then
a popup screen after a short period that resets and starts again. Could even
start with a popup screen that has instructions? Then a pause button (smaller)
on the bottom right that actually pauses Tone.js and ball movement and movement
of main player sprite. Reduce the volume, and turn off metronome for now, too.
Can then tweak the sounds and game settings to make it more playable. Get a
complete game going at the moment though.


