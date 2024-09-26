
# Image Compression Using Bézier Curve
## What is this project about?
This project demonstrates an image compression method for 600x600 RGB images by applying cubic Bézier curves. The technique significantly reduces storage space while maintaining visual quality, achieving a compression ratio of approximately 6:1.

## Overview
The compression works by dividing the image into blocks of 25 pixels and fitting a cubic Bézier curve to each block. For each block, only 4 control points (P₀, P₁, P₂, and P₃) are stored. These control points are used to reconstruct the pixel values by calculating the curve's t values, providing an efficient way to encode and decode the image.

## Methodology
- **Image Blocking:** The image is divided into 24x24 blocks, each containing 25 pixels.
  
  <div align = "center" >
  <img width = "500" src="demo/7.jpg"/>
  </div>


- **Curve Fitting:** For each block, a cubic Bézier curve is calculated by fitting 4 control points.
 <div align = "center" >
  <img width = "500" src="demo/8.png"/>
  </div>

- **Compression:** Only the 4 control points (P₀, P₁, P₂, and P₃) are stored instead of the pixel values.

- **Formulation of general equations from Cubic Bezier Curve**
 <div align = "center" >
 <img width = "500" src="demo/1.png"/>
 </div>
 <br>
   <div align = "center" >
  <img width = "500" src="demo/2.png"/>
  </div>
  
- **Decompression:** The pixel values are reconstructed using the stored control points and calculated t values.

 <div align = "center" >
  <img width = "500" src="demo/3.png"/>
  </div>

  ## Screenshots
<img width = "500" src="demo/4.png"/>
<img width = "500" src="demo/5.png"/>
<img width = "500" src="demo/6.png"/>

  

