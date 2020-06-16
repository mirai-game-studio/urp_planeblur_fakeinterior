## Universal Render Pipeline Kawase Blur Renderer Extension

This is a experimental RenderFeature implementation aiming to show multiple things:
* post processing "like" effect in URP using ScriptableRenderFeatures
* how to render multiple passes using CommandBuffers in RenderFeatures
* how to do a simple yet effective blur, based on the Kawase blur as described in this [article](https://software.intel.com/en-us/blogs/2014/07/15/an-investigation-of-fast-real-time-gpu-based-image-blur-algorithms).


### Features
* flexible downscaling
* variable number of blur passes
* simple demo scene and materials


### Download
Download this project using the releases tab. The unitypackage contains all the files needed to setup the blur effect. The demo scene is not included.


### Video Tutorial
I've created a video tutorial on how to install and use this package. Check it out:
[![Tutorial Thumbnail](http://img.youtube.com/vi/BIKUSU7nz20/0.jpg)](http://www.youtube.com/watch?v=BIKUSU7nz20 "Blur / Frosted Glass in the Unity Universal Render Pipeline (URP) for Free!")


### Notice
This blur will work for both 3D objects and UI images. Please note however this implementation will not allow for the blurring of other UI elements, only 3D scene elements. Also, for UI blurring to work, the canvas must be set to 'Screen Space - Camera' or 'World Space', and not 'Screen Space - Overlay'.


### Demo scene
![A demo scene showing the effect in action](sample-blur.png)


### Masked shaders
Masked shader variants can be used to blur UI elements with rounded corners properly. To do this, simply attach a material using the masked shader onto a UI image component, and change the mask to an image with transparency. If the image has been sliced to allow for resizing, also set the sprite on the image component to the same mask.


Blur originally developed with Unity 2019.3.
Demo scene & project restructure done with Unity 2020.1.
