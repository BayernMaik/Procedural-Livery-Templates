# ACC - Procedural Liveries - Template

This project contains shader templates to bake procedurally generated patterns onto your meshes to create custom liveries for Assetto Corsa Competizione. (Works for other games aswell, depending on the workflow to get the textures in the game).


<details open><summary><b>Previews</b></summary>

<!-- Topography Pattern -->
<details open>
<summary>&nbsp;&nbsp;<b>Topography Pattern</b></summary>

---
<img 
    src="./Preview/Topography/Preview_NoiseTexture_Topography.png"
    title="Preview NoiseTexture Topography"
    alt="Preview NoiseTexture Topography"
    width="256"
/>
<img 
    src="./Preview/Topography/Preview_NoiseTexture_Topography_Shaderball.png"
    title="Preview NoiseTexture Topography"
    alt="Preview NoiseTexture Topography"
    width="455"
/>
<br>
This is a topography inspired pattern imitating the lines on maps to visualize elevation

**Features**:<br>
&bullet; Opacity Mask Shader to generate an alpha mask to repack into the final texture. This allows to select a color for lines within the ingame editor.

**Known Issues**:<br>
&bullet; The directional resampling along the axes to create the outline needs to be extended to clean up inconsistent sampling of corners 

---
</details>
<!-- /Topography Pattern -->

<!-- Disruptive Pattern -->
<details close>
<summary>&nbsp;&nbsp;<b>Disruptive Camo Pattern</b></summary>

---
<img 
    src="./Preview/DisruptiveCamo/Preview_NoiseTexture_DisruptiveCamo.png"
    title="Preview NoiseTexture DisruptiveCamo Generic"
    alt="Preview NoiseTexture DisruptiveCamo Generic"
    width="256"
/>
<img 
    src="./Preview/DisruptiveCamo/Preview_NoiseTexture_DisruptiveCamo_Shaderball.png"
    title="Preview NoiseTexture DisruptiveCamo Generic"
    alt="Preview NoiseTexture DisruptiveCamo Generic"
    width="455"
/>
<br>
Inspired by the most commonly used Type of disruptive Camo Patterns by Militaries around the Globe

---
</details>
<!-- /Disruptive Pattern -->

<!-- Pixel Pattern -->
<details close>
<summary>&nbsp;&nbsp;<b>Pixel Camo Pattern</b></summary>

---
<img 
    src="./Preview/PixelCamo/Preview_NoiseTexture_PixelCamo.png"
    title="Preview NoiseTexture PixelCamo Marpat"
    alt="Preview NoiseTexture SplinterCamo Marpat"
    width="256"
/>
<img 
    src="./Preview/PixelCamo/Preview_NoiseTexture_PixelCamo_Shaderball.png"
    title="Preview NoiseTexture SplinterCamo M90"
    alt="Preview NoiseTexture SplinterCamo M90"
    width="455"
/>
<br>
Inspired by Pixelated Camo Patterns used by North-American Militaries (Marpat, Cadpat, ACU...)

**Known Issues**<br>
&bullet; Its not possible to project uniform sqares onto complex non uniform geoetry without warp. This is visible on rounded areas of the geometry.
<br>

---
</details>
<!-- !Pixel Pattern -->

<!-- Splinter Pattern -->
<details close>
<summary>&nbsp;&nbsp;<b>Preview Splinter Camo Pattern</b></summary>

---
<img 
    src="./Preview/SplinterCamo/Preview_NoiseTexture_SplinterCamo.png"
    title="Preview NoiseTexture SplinterCamo M90"
    alt="Preview NoiseTexture SplinterCamo M90"
    width="256"
/>
<img 
    src="./Preview/SplinterCamo/Preview_NoiseTexture_SplinterCamo_Shaderball.png"
    title="Preview NoiseTexture SplinterCamo M90"
    alt="Preview NoiseTexture SplinterCamo M90"
    width="455"
/>
<br>
Inspired by the Swedish Army M90 Camo Pattern

---
</details>
<!-- !Splinter Pattern -->

</details>

## Usage
- Open the blender project<br>
- Import the Mesh Object (probably .obj or .fbx file):<br>
    - File
    - Import
    - 'select file format for object file'
    - 'select file in browser'
- Apply the Material to the Object
    - Outliner (dialog on the right screen)
    - Materials Tab
    - Select the Material in the Dropdown
- Bake the Texture:
    - Open the Shader Editor
    - Create a Bake Texture in the Shader Editor
    - Render Settings
    - Bake
