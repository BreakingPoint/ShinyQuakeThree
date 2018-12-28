# ShinyQuakeThree

A reshader of Quake 3 Arena to polish its looks. Uses ReShade and IoQuake3.

Adds:

* Bumpmapped reflective surfaces
* Aliasing
* Atmospheric/Volumetric lighting(-ish)
* Enhanced contrast and more vibrant colors
* Dithering

About the Game Q3A:
https://en.wikipedia.org/wiki/Quake_III_Arena

## Previews (before/after) ##

<img src="https://i.imgur.com/4aw8z7y.gif">

<img src="https://i.imgur.com/mLsIR8Y.gif">

<img src="https://i.imgur.com/whwO6el.gif">

<img src="https://i.imgur.com/iwIb3p8.gif">

<img src="https://i.imgur.com/jf3J2Tu.gif">

## Downloads

IoQuake3: https://ioquake3.org/get-it/

ReShade 3.4.1: https://reshade.me/downloads/ReShade_Setup_3.4.1.exe

Default-Shaders from 2016/10/16: https://github.com/crosire/reshade-shaders/archive/8e43e33234b810ffecf55c840177111d912eb718.zip

*You need ReShade 3.4.1 & the default shaders form that date! Newer versions are not compatible with these settings.*

... and the new ReShade settings for Q3A of coz: https://github.com/BreakingPoint/ShinyQuakeThree/archive/master.zip

## Installation ##

1. Download and install IoQuake3 and ReShade 3.4.1. Follow their setup instructions (ReShade: Use OpenGL + do not download default shaders but use the ones listed above!)

2. Put the `q3a_default.ini` file in the same folder as `quake3.exe`/`ioquake3.exe`.

3. Extract the content of the default-shaders ZIP with full pathnames into the folder of your 'quake3.exe'. After that rename the `reshade-shaders-8e43e33234b810ffecf55c840177111d912eb718` folder into `reshade-shaders`.

4. Run `ioquake3.exe`.

5. Open ReShade menu using Shift-F2 and select `q3a_default.ini` settings.

6. Close Q3A and open the `ReShade.ini` file in the same folder of `ioquake3.exe` and replace the following settings with these values in the `[GENERAL]` section of the INI file:

       PreprocessorDefinitions=RESHADE_DEPTH_LINEARIZATION_FAR_PLANE=1000.0,RESHADE_DEPTH_INPUT_IS_UPSIDE_DOWN=0,RESHADE_DEPTH_INPUT_IS_REVERSED=0,RESHADE_DEPTH_INPUT_IS_LOGARITHMIC=0
       EffectSearchPaths=.\reshade-shaders\Shaders
       TextureSearchPaths=.\reshade-shaders\Textures

      *If you don't, no effects and textures will be loaded and the reflections on surfaces will be upside down.*

7. Run `ioquake3.exe` again.
