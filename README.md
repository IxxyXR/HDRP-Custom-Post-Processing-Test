# HDRP-Custom-Post-Processing-Test

1. Edit manifest.json to reference 7.1.1 of "com.unity.render-pipelines.high-definition" and "com.unity.shadergraph" as that version doesn't currently show up in the package manager UI. After Unity finishes loaded those packages find there is an #if block in one of the scripts that might throw an error - I just commented it out for now as it was XR related

2. Right click and create a new Post processing script (it's a specific option in the create menu) and a PP shader (or use the scripts in my repo as an example). Check the shader references the script name correctly (see line 21 in mine)

3. Go to Project Settings/HDRP Defaults and scroll down to the bottom. Add the effect to the section (
Before Rendering/Before Transparent/Before PostProcess) that corresponds to what you put in your cs script (see line 16 in mine)

4. Add a Volume in your scene. Your effect should now appear in "Add overrides" as a new item under Post Processing/Custom
