# Orbital Camera

- [Orbital Camera](#orbital-camera)
  - [Teams](#teams)

## Teams

| No. | Name                      | NRP        |
| --- | ------------------------- | ---------- |
| 1   | Widian Sasi Disertasiani  | 5025201267 |
| 2   | Urdhanaka Aptanagi        | 5025211123 |
| 3   | Najma Ulya Agustina       | 5025211239 |

<h2>Unity Camera</h2>

<h2>Camera</h2>

Camera is a fundamental component that defines the viewpoint through which the game world is seen and rendered on the screen. It provides the perspective or orthographic view of the 3D scene and controls how the game objects are displayed to the player. The Camera component has several properties that define its behavior and how it interacts within the scene:

<h2>Camera Component Properties</h2>

<img src="https://media.discordapp.net/attachments/1170761960443347105/1171105595521237093/image.png?ex=655b7814&is=65490314&hm=25db500674308307c01a65fa24c8026b5d29957ab4bae15f73306a7cd2f0d897&=">

- ```Clear Flags```: Describes how the camera clears the background before rendering a frame. Options include Skybox, Solid Color, Depth Only, and Don't Clear.
1) Skybox:
Whenever a new frame has to be rendered; the old frame is cleared with given skybox on top it new captured frame of the scene is rendered.
<img src ="https://cdn.discordapp.com/attachments/1170761960443347105/1171123063744626718/image.png?ex=655b8858&is=65491358&hm=2dcb628753f104fb5423043b04b3f8cadbef130642de008bede08de090f13489&">

2) Solid color:
Whenever a new frame has to be rendered; the old frame is cleared with given background color on top it new captured frame of the scene is rendered.
<img src ="https://cdn.discordapp.com/attachments/1170761960443347105/1171123158896615424/image.png?ex=655b886f&is=6549136f&hm=a873fae02609686798fc45ccf9ca4df6e53cd59c9df0e3d693ca70f77c896cd9&">

3) Depth only:
Whenever a new frame has to be rendered; from the old frame only game objects with depth are cleared not the old frame itself. So you can clearly observe old frames will be still visible and game objects in the scene are rendered properly without intersecting.
<img src ="https://media.discordapp.net/attachments/1170761960443347105/1171123361309532232/image.png?ex=655b889f&is=6549139f&hm=9a10b8f12e879a2c31e611780f547d2b6ce21719bc6b7f9f251fbbd63d972800&=">

4) Don't clear:
Whenever a new frame has to be rendered; from the old frame nothing is cleared.
So you can clearly observe old frames will be still visible and game objects in the scene intersect with each other.

- ```Background```: Specifies the background color or texture when the camera clears the screen. It can be a solid color or a Skybox material.

- ```Culling Mask```: Defines which layers are visible to the camera, allowing control over what the camera can render.

<img src ="https://media.discordapp.net/attachments/1170761960443347105/1171122433785352253/image.png?ex=655b87c2&is=654912c2&hm=b42e8f9b9f02dcb290a90b0d7aa6f308d314498b79d5e27e222388c574b76f66&=">

<img src ="https://media.discordapp.net/attachments/1170761960443347105/1171122369096597635/image.png?ex=655b87b3&is=654912b3&hm=34af147c0f22f59cb452bb3f5ffe10420ae5621677a9802c5257d98a25587ee3&=">

- ```Projection```: Determines the type of projection used by the camera, which can be either Perspective or Orthographic. Perspective projection creates a sense of depth and distance, while Orthographic projection maintains the same object size regardless of the distance from the camera.
1) Prespective: 
<img src = "https://cdn.discordapp.com/attachments/1170761960443347105/1171121708342718534/image.png?ex=655b8715&is=65491215&hm=3fd318d0d909031b1b10cfe6b45422aa0e91cc5d865b8c085c6ba1bc354e2f82&"> 

1) Orthographic: 
<img src = "https://cdn.discordapp.com/attachments/1170761960443347105/1171122087864311928/image.png?ex=655b8770&is=65491270&hm=67396c030260425474c98d7024017a197a3404ae636406ac8e0838c73c2db8fb&"> 

- ```Field of View (FOV)```: For Perspective projection, it controls the angle of the camera's field of view. A wider FOV displays more of the scene, while a narrower FOV shows less but in more detail.
<img src = "https://media.discordapp.net/attachments/1170761960443347105/1171121110599876620/image.png?ex=655b8687&is=65491187&hm=289d2713f3fa43e345d00e1d41e3e650cf8a27aa6b3be97e84b98ab5ef93470c&=&width=1440&height=633">

- ```Depth ```: Indicates the drawing order of the camera on the screen (game view).

- ```X, Y, W and H```: indicate x position, y position, width and height of the viewport respectively.

<img src= "https://media.discordapp.net/attachments/1170761960443347105/1171116741095608340/image.png?ex=655b8275&is=65490d75&hm=c313060e90b69ff3ca515e8ef127e18d3e7678b702efb61b9c90666294e48201&=&width=1216&height=701">


