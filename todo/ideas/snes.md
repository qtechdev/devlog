# SNES graphics/emulator

I can implement a software renderer by mapping texture data to a full screen
rectangle as done in my chip8 renderer. For basic 2D graphics such as SNES I
think this should perform ok; Hardware acceleration would be nice but I am
currently uncertian how I would implement certain features of the SNES
rendering pipeline. Mixing software and hardware rendering would be one way of
proceeding but I think that may be more complicated.   
I will investigate this if a software based
approach does not perform adequately.

I would implement the rendering system in a somewhat generic way, allowing for
any combination of features, not limited to the specific configurations
supported by the SNES. Standard SNES graphics modes will be available as
presets.

---

The rendering pipeline can support up to four background layers with either 2-,
4-, or 8-bits per pixel of colour data; and three object/sprite layers. There
are various post-processing effect that are available: mosaic, windows, colour
maths, etc. Ther are two display options are available: "High-Res", which
double the horixontal resolution, and "interlaced", which doubles the vertical
resolution in addition to enabling interlaced video.

Mode 7 is a completely unique and different graphics mode in the original SNES
implementation, however much of this seemed to be due to hardware limitations.
This mode introduces a unique feature in affine transformations of the
background.

The most challenging part will likely be implementing the ability to change
graphcis modes mid-frame. I think I will leave this feature for the full SNES
emulator.
