# Orbital Camera

- [Orbital Camera](#orbital-camera)
  - [Teams](#teams)

## Teams

| No. | Name                     | NRP        |
| --- | ------------------------ | ---------- |
| 1   | Widian Sasi Disertasiani | 5025201267 |
| 2   | Urdhanaka Aptanagi       | 5025211123 |
| 3   | Najma Ulya Agustina      | 5025211239 |

<h2>Unity Camera</h2>

<h2>Camera</h2>

Camera is a fundamental component that defines the viewpoint through which the
game world is seen and rendered on the screen. It provides the perspective or
orthographic view of the 3D scene and controls how the game objects are
displayed to the player. The Camera component has several properties that define
its behavior and how it interacts within the scene:

<h2>Camera Component Properties</h2>

<img src="https://media.discordapp.net/attachments/1170761960443347105/1171105595521237093/image.png?ex=655b7814&is=65490314&hm=25db500674308307c01a65fa24c8026b5d29957ab4bae15f73306a7cd2f0d897&=">

- `Clear Flags`: Describes how the camera clears the background before rendering
  a frame. Options include Skybox, Solid Color, Depth Only, and Don't Clear.

1. Skybox: Whenever a new frame has to be rendered; the old frame is cleared
   with given skybox on top it new captured frame of the scene is rendered.
   <img src ="https://cdn.discordapp.com/attachments/1170761960443347105/1171123063744626718/image.png?ex=655b8858&is=65491358&hm=2dcb628753f104fb5423043b04b3f8cadbef130642de008bede08de090f13489&">

2. Solid color: Whenever a new frame has to be rendered; the old frame is
   cleared with given background color on top it new captured frame of the scene
   is rendered.
   <img src ="https://cdn.discordapp.com/attachments/1170761960443347105/1171123158896615424/image.png?ex=655b886f&is=6549136f&hm=a873fae02609686798fc45ccf9ca4df6e53cd59c9df0e3d693ca70f77c896cd9&">

3. Depth only: Whenever a new frame has to be rendered; from the old frame only
   game objects with depth are cleared not the old frame itself. So you can
   clearly observe old frames will be still visible and game objects in the
   scene are rendered properly without intersecting.
   <img src ="https://media.discordapp.net/attachments/1170761960443347105/1171123361309532232/image.png?ex=655b889f&is=6549139f&hm=9a10b8f12e879a2c31e611780f547d2b6ce21719bc6b7f9f251fbbd63d972800&=">

4. Don't clear: Whenever a new frame has to be rendered; from the old frame
   nothing is cleared. So you can clearly observe old frames will be still
   visible and game objects in the scene intersect with each other.

- `Background`: Specifies the background color or texture when the camera clears
  the screen. It can be a solid color or a Skybox material.

- `Culling Mask`: Defines which layers are visible to the camera, allowing
  control over what the camera can render. Need to set the object layer.

<img src ="https://media.discordapp.net/attachments/1170761960443347105/1171122433785352253/image.png?ex=655b87c2&is=654912c2&hm=b42e8f9b9f02dcb290a90b0d7aa6f308d314498b79d5e27e222388c574b76f66&=">

<img src ="https://media.discordapp.net/attachments/1170761960443347105/1171122369096597635/image.png?ex=655b87b3&is=654912b3&hm=34af147c0f22f59cb452bb3f5ffe10420ae5621677a9802c5257d98a25587ee3&=">

- `Projection`: Determines the type of projection used by the camera, which can
  be either Perspective or Orthographic. Perspective projection creates a sense
  of depth and distance, while Orthographic projection maintains the same object
  size regardless of the distance from the camera.

1. Prespective:
   <img src = "https://cdn.discordapp.com/attachments/1170761960443347105/1171121708342718534/image.png?ex=655b8715&is=65491215&hm=3fd318d0d909031b1b10cfe6b45422aa0e91cc5d865b8c085c6ba1bc354e2f82&">

1. Orthographic:
   <img src = "https://cdn.discordapp.com/attachments/1170761960443347105/1171122087864311928/image.png?ex=655b8770&is=65491270&hm=67396c030260425474c98d7024017a197a3404ae636406ac8e0838c73c2db8fb&">

- `Field of View (FOV)`: For Perspective projection, it controls the angle of
  the camera's field of view. A wider FOV displays more of the scene, while a
  narrower FOV shows less but in more detail.
  <img src = "https://media.discordapp.net/attachments/1170761960443347105/1171121110599876620/image.png?ex=655b8687&is=65491187&hm=289d2713f3fa43e345d00e1d41e3e650cf8a27aa6b3be97e84b98ab5ef93470c&=&width=1440&height=633">

- `Depth`: Indicates the drawing order of the camera on the screen (game view).

- `X, Y, W and H`: indicate x position, y position, width and height of the
  viewport respectively.

<img src= "https://media.discordapp.net/attachments/1170761960443347105/1171116741095608340/image.png?ex=655b8275&is=65490d75&hm=c313060e90b69ff3ca515e8ef127e18d3e7678b702efb61b9c90666294e48201&=&width=1216&height=701">

<h2>Camera Target Texture Property</h2>

<h3>Target Texture</h3>
Indicates reference to Render Texture asset

- Render Texture is a special asset used to store the camera's output
  information

- Instead of rendering on screen: we can render the output of a camera on game
  object

Simple step to Create a Mirror:

1. `Create a camera, set positition and rotation according to the requirement`

   - Setup the scene: Game Object Menu -> 3D Object -> Cube

   - Scale it ( x = 10, y = 1, z = 10)

   - Create 2 more cube and scale it by (x = 2, y = 2, z = 2) and set the
     positition ( move it Up, Move it left side )

2. `Create a New Rener Texture, Asset - Create - Render Texture`

   - Go to asset menu -> create -> render texture

3. `Set the Target Texture of New Camera to New Rende Texture`

   - Going to Game Object Menu -> camera

   - Drag new render texture inside target texture property

     You should observe that in the game view you are going to see the output of
     the main camera not the output of newly created camera. So the camera lost
     the ability of displaying on screen. Understand when you setup the render
     texture what happened its going to lost capacity of rendering the scene on
     screen. so will put all the information inside New Render Texture.

4. `Create a New Material, set its Albedo property to New Render Texture`

   - Create Material

   - Drag New Render Texture to Albedo property

5. `Create a New Plane, and apply the New Material to it`

   - Game Object Menu -> 3D Object -> Plane

   - Move it Up and Rotate it around x axis and z axis

   - Drag new material to the plane and duplicate it

   - Rotate it around y axis

   - The Mirror is Created

   This is how we can create mirror. if we delete one of the cube its will
   deleted in mirror too. so that is the use for the render texture.

## Skybox

Skybox is a material that represent the skies and the ground. With skybox, we
can create the illusion of a distant horizon or sky. Because skybox creates the
illusion of distant horizon or sky, skybox is typically a 360-degree texture
wrapped around the scene. It provides the environment's overall ambience.

We will use
![This](https://assetstore.unity.com/packages/2d/textures-materials/sky/skybox-series-free-103633)
assets to implement skybox in our scene.

There are several ways to use skybox material:

- ### Use skybox material in the scene

When we use skybox material in the scene, the sky and the ground will change
according to the skybox material we use.

To use it, select Window -> Rendering -> Lighting

![image](https://gist.github.com/assets/46347836/f47c1128-576c-4bdc-a15e-8765024fa58d)

In Lighting window, select Environment and then select material for Skybox
Material

![image](https://gist.github.com/assets/46347836/34ef25f2-d0b6-44f5-ab09-d3bcb73e1ce3)

After you select one of the material from the skybox assets above, the sky and
the ground will change

![image](https://gist.github.com/assets/46347836/89114776-33e6-4561-b82c-b86feb4ee781)

- ### Use skybox material in the camera

When we use skybox material in the camera, the sky and the ground will only
change if we use the camera

To use it, select our main camera and then Add Component, then select Rendering
-> Skybox

![image](https://gist.github.com/assets/46347836/21c0a808-681a-4272-ad72-ad5138ff9e41)

![image](https://gist.github.com/assets/46347836/24219720-4d8e-4f4b-b974-5a02aee544ef)

![image](https://gist.github.com/assets/46347836/487ed218-e0a7-445a-802a-ae03794e1584)

![Screenshot 2023-11-27 204813](https://gist.github.com/assets/46347836/630046ae-6379-46cf-bd10-890b148fc707)

After that, select skybox material you want to use

![Screenshot 2023-11-27 204905](https://gist.github.com/assets/46347836/7aab4b2c-d697-4de2-be9c-cbf098c0d01e)

After you have done all of that, the skybox doesn't change, but if you see
through through the main camera, the skybox does change

![image](https://gist.github.com/assets/46347836/00e528c7-a808-4040-84f6-a2cb5c4c9fbd)

![image](https://gist.github.com/assets/46347836/2f736e1f-9886-4176-a101-dad99b8e8aba)
