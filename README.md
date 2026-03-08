# ACC - Procedural Liveries - Template

This project contains shader templates to bake procedurally generated patterns onto your meshes to create custom liveries for Assetto Corsa Competizione. (Works for other games aswell, depending on the workflow to get the textures in the game).


<details open><summary><b>Previews</b></summary>

---
<!-- Topography Pattern -->
<details open>
<summary><b>Topography Pattern</b></summary>

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

<!--
**Features**:<br>
&bullet; Opacity Mask Shader to generate an alpha mask to repack into the final texture. This allows to select a color for lines within the ingame editor.
-->
</details>
<!-- /Topography Pattern -->

<!-- Disruptive Pattern -->
<details open>
<summary><b>Disruptive Camo Pattern</b></summary>

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

</details>
<!-- /Disruptive Pattern -->

<!-- Pixel Pattern -->
<details open>
<summary><b>Pixel Camo Pattern</b></summary>

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
</details>
<!-- !Pixel Pattern -->

<!-- Splinter Pattern -->
<details open>
<summary><b>Splinter Camo Pattern</b></summary>

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

</details>
<!-- !Splinter Pattern -->

</details>

<br>

<details open>
<summary>&nbsp;&nbsp;<b>Usage</b></summary>

---
This is not a complete Guide to create a custom Livery. This Guide only describes how to generate a Texture for a UV-Mapped Mesh using the included Shaders and Materials. You will need to obtain the Object Files for the Vehicles exteriour Mesh from the Game to generate a Texture. 

- Download and Install Blender
(https://www.blender.org/download/)

- Download the Project from Github (Code -> Download ZIP)
![Download the Project](./Images/Usage/Usage_1_DownloadRepository.PNG)
Extract the Project Files and open the Blender Project

- Import the 3D-Object (File -> Import -> Select Format)
![Import Object](./Images/Usage/Usage_2_ImportObject.PNG "Import Object")
![Import](./Images/Usage/Usage_3_ImportObjectDialog.PNG "Import Object")
Make sure the imported Object is selected through the whole Process (Objectname highlighted orange)

- Adjust the Imported Objects Scale to roughly authentic Dimensions and Apply Scale (Object -> Apply -> Scale)
![Adjust the Object Scale](./Images/Usage/Usage_4_AdjustScale.PNG "Adjust the Object Scale")
This is necessary for proper Texture Scaling

- Switch to the 'Materials Tab' and remove the imported Materials from the Object
![Remove imported Material](./Images/Usage/Usage_5_RemoveMaterials.PNG "Remove imported Materials")

- In the 'Materials' Tab select one of the provided Template Materials
![Select a Material](./Images/Usage/Usage_6_SelectTemplate.PNG "Select a Material")

- With a Material selected open the Shader Editor (Editor Type -> Shader Editor)
![Open Shader Editor](./Images/Usage/Usage_7_OpenShaderEditor.PNG "Open Shader Editor")

- In the Shader Editor right click anywhere to add a new 'Image Texture' Node as Bake Texture with the required Texture Attributes
![Create Image Texture Node](./Images/Usage/Usage_8_CreateBakeTextureNode.PNG "Create Image Texture Node")
![Create Image Texture Node](./Images/Usage/Usage_9_CreateBakeTexture.PNG "Create Image Texture Node")

- With the new Image Texture selected (white outline) switch to the 'Scene Tab' and open the 'Bake' Menu. Set the Bake Type to Diffuse and Contributions to Color only. Then hit Bake
![Bake the Texture](./Images/Usage/Usage_10_Bake.PNG "Bake the Texture") 
Wait until the Bake Process finishes (Progress Bar in Status Bar at the bottom)

- Change to the Image Editor (Editor Type -> Image Editor) and select the newly baked Texture
![Select the baked Texture](./Images/Usage/Usage_11_OpenImageEditor.PNG "Select the baked Texture")
![Select the baked Texture](./Images/Usage/Usage_12_OpenImage.PNG "Select the baked Texture")

- Save the baked Image
![Save the baked Texture](./Images/Usage/Usage_13_ExportImage.PNG "Save the baked Texture")
![Save the baked Texture](./Images/Usage/Usage_14_SaveImage.PNG "Save the baked Texture")
You are done, now you can use the exported Pattern with your preferred Image Editor to create the custom Livery

</details>

<br>

<details open>
<summary>&nbsp;&nbsp;<b>Known Issues</b></summary>

---
&bullet; Distortion on Topography Pattern:<br>
The directional resampling along the axes to create the outline needs to be extended to clean up inconsistent sampling of corners 

&bullet; Warp on Pixel Camos:<br>
Its not possible to project uniform sqares onto complex non uniform geoetry without warp. This is visible on rounded areas of the geometry.
<br>

</details>