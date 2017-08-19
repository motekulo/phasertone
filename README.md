# Phasertone

Experiments mixing the web audio library [Tone js](https://tonejs.github.io/) with the game engine [Phaser.io](http://phaser.io/)

## What does it do?
Not much! Yet... Balls bounce around a game world, collide with various objects, and create music as they go.

## Why?
This is part of a larger research project exploring mobile phones and music - in particular changes being wrought in music scenes in Melanesia. There is some discussion about this [here](http://motekulo.github.io/phonestrument/), and more will be added soon.

Some of the questions we are exploring include:

- What are people doing with phones and music at the moment?
- How straightforward is it to make music on a phone?
- Can a game environment provide new ways of interacting with sound and music?

## How does it work?
There is a chord progression, passed in to the main game code in krungKrang.js. Tonality.js provides utilities to return arrays for scales and chord tones.
It's useful to imagine a grid (usually vertical)
When things collide, events are scheduled on the Tone js transport.
