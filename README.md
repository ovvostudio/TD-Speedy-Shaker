# TD-Speedy-Shaker
GLSL multi-blending compositor
latest version 1.11

***


This is the 2nd instalment in a serie of post-processing tools.

***
changelog:

*v1.11:
  - bug fix: level wasn't working on 2+ layers
  - added external Exemples file for some use case scenarios
***

*V1.1:
  - correct alpha handling
  - performance optimizations
  - better layer reordering
***

*V1.01:
  - clamped illegal color values
  - readme and attributions
  - universally tested 088/099
***

### Why Speedy Shaker?

Simply put, because it is a multi-layer mixer/shaker/blender on steroides without actual steroides :stuck_out_tongue_winking_eye: And it is fast! Like really fast.





I wanted to have a tool that provides the same functionnalities as Photoshop/AFter Effects but expands on them with deep integration in TouchDesigner with the minimum CPU/GPU footprint. 

This component is based on the super-excellent GLSL mover-comper by [**archo-p**](http://namethemachine.com/) that he made available on [TD forums](http://derivative.ca/Forum/viewtopic.php?f=22&t=5537&hilit=multi). Thank you!

I wanted to expand it extensively to include an essential kit of color-correction tools as well as some extras. The GUI was made with custom parameters so it would be self-explicite.

Please, bear in mind it is version 1.0 and almost certainly quite buggy. At the end of this readme there's a list of features/bugs to expand/debug.

So, let's get on with it, shall we?



### What can it do for you?


1. Up to 16 layers (not a physical, but more practical limitation) with full control on transform/scale (from original component by [**archo-p**](http://namethemachine.com/))
2. Pixel or fractional translate (from original component by [**archo-p**](http://namethemachine.com/))
3. Top Left mode origin (from original component by [**archo-p**](http://namethemachine.com/))
4. Background can be TOP or color
5. Resolution can be set from Background TOP (no translate/scale)

6. Matte per Layer
   - can be alpha or luma matte
   - can be inverted
   - can be translated/scaled
   - lower and upper range that alternates how matte alpha reacts (kind of contrast control but for matte)
   - can be linked/stretched to layer
   - if non-existent - considered as alpha=1

7. Per layer control:
   - tint to color
   - basic bloom with advanced control (it looks pretty bad now, more like box-blur because I wanted to use only 1 pass instead of 2-pass gaussian blur). For now it works as pre-effect, before any color correction happens.
   - blending modes - these are based on Photoshop Math (25 modes)
   - blending strength
   - level - alpha control
   - perceptual desaturation - truly black&white filter based on color weights
   - brightness/saturation/contrast/gamma
  
8. Advanced layer control:
   - on 'Layer control page' you can change the order of layers
   - Solo/Mute
   
9. GUI Control:
   - Add/Remove Layer
   - Reset Layer
   
   
That's it folks!

Be strange

Shandor
