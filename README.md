# HDRP Custom Post-Processing Test

With Unity 2019.3b4 and HDRP 7.1.1 it's finally possible to write your own custom post-processing effects. This project is a simple example.

It should all be working already but here (from memory) are the steps needed to create a custom post fx from scratch:

1. Right click and create a new Post processing script (it's a specific option in the create menu) and a PP shader (or use the scripts in my repo as an example). Check the shader references the script name correctly (see line 21 in mine)

2. Go to Project Settings/HDRP Defaults and scroll down to the bottom. Add the effect to the section (
Before Rendering/Before Transparent/Before PostProcess) that corresponds to what you put in your cs script (see line 16 in mine)

3. Add a Volume in your scene. Your effect should now appear in "Add overrides" as a new item under Post Processing/Custom
