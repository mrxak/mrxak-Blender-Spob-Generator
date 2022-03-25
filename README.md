# mrxak's Blender Spob Generator
This is mrxak's spob (SPace OBject) generator for Blender. The license is CC0, so go nuts with it, but it'd be nice if you shared what you learned how to do with others so we can all make better planets, moons, etc. for our own artwork, games, and game mods. I spent many hours working on this generator so that I could make planets for mods in a game called Cosmic Frontier, and the Escape Velocity game series that preceded it. I'm releasing it now, and continuing to work on it periodically, so that other modders in the EV and CoFro communities can have one less thing to worry about. But I can imagine other people will find uses for it beyond what I'm using it for, and I hope this will meet your needs or give you a nice jumping off point.

The project consists of a .blend file, for use in Blender 3.0 or later. In it you will find a light source representing a sun, several objects making up a spob, and a camera that has been set up for rendering the planet. There are numerous materials embedded in the file which you may apply to the spob objects, to give your spobs different appearances as desired, and of course you are encouraged to change these and make your own. You may wish to adjust render settings, but I have set them to what seemed like reasonable values that create nice results in not too much time on my computer. Use the Cycles render engine for best results.

## Using the File
You can change what appears in your final render by turning on and off the spob objects in the outliner. You can show or hide the Atmosphere, Clouds, or Ring, and you can represent especially deep opaque clouds with the Shroud World object which obscures the Terrain object.

Each object has a material, and several alternate materials are included with reasonable values in their respective shader node trees. Use the shading tab at the top of your Blender window to select between these, and adjust their values. These materials are presented as examples, and inspiration, and you may find some of them useful for your projects as-is. If you want to change something, I recommend copying an existing material first, and making sure to click the shield icon to give your new materials a "fake user" to ensure it gets saved even when you're not using that material on any objects when you close Blender.

Some of the included terrain materials have sections of nodes for adding cities that will glow on the night side of a spob and appear gray on the day side. You'll need to attach the Emission shader node to the emission field in the Principled BSDF node, make sure the Color node next to the Principled BSDF is plugged into the base color field, and finally set the emission strength to 1.000. If you don't want cities, don't connect these, or disconnect them if they already are connected. It's rather beyond the scope of this readme to explain in detail how all of the various materials work, but I wanted to at least give you a head's up on this.

To change where the shadow falls on your spob, rotate the Sun on the X axis. By default it is set to 37.5 degrees.

To change the tilt of the spob's axis, rotate the Camera on the Y axis. By default it is set to -45 degrees.

To change the rotation of the spob on its axis, change what frame you're looking at in the viewport, or what frame(s) you render. Frames 1-95 are meant for a planet with no ring. Frames 96-190 are for a planet with a ring, as the camera is moved back. If the spob you're rendering has a 24 hour day, each frame represents 15 minutes of time.

## Tutorial Videos
You can find tutorials on using the .blend file in [this YouTube Playlist](https://www.youtube.com/playlist?list=PL9hpqkEu_NGwUlD44fzNJs9FBwmdky8ce).
