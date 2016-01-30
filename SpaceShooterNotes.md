
Enabling Physics is done by adding a Rigid Body component to the Game Object.

Capsule collider can be used for varying shapes of objects and is more efficient than mesh collider.

Can create simplified mesh colliders to be more performant when using mesh collider.

Camera can be perspective or orthographic. Perspective are like most games while orthographic reminds me of 2d games. You can change x and z to change the position of the object on the view but changing y does not do anything other than layer the otehr 3d objects. Reminds me of how sprites only have x/y coords but using 3d models instead.

Perspective cameras have a Field Of View setting. Making it so your distance doesn't change but you can fit a wider angle in. 

With orthographic you can change the orthographic size which does something similar but probably doesn't give the camera a "wide lens" type of view by enlarging it.

Can click on the label of the field and drag the value and have it update in real time in the Inspector view(When I say label I mean the label "Z" for example in transform rather than the input box for "Z")

Unity 5 has a default skybox in the lighting tab, to remove the skybox you must go there rather than the camera.

Unity 5 Ambient light is now handled in the lighting tab. Ambient light gives a small amount of light on all things regardless of light sources.

Turn ambient light to black as you cannot turn ambient light off.

Feel free to use objects as folders

A quad is like 2 triangles making a square and is good for backgrounds(Remove colliders)

Images can be dragged on to components and it will create a material for you.

float moveHorizontal = Input.GetAxis("Horizontal");
float moveVertical = Input.GetAxis("Vertical");	

Check console after code changes to check for errors.

Mathf is a tool in unity for doing common math operations

Mathf.Clamp keeps a number between 2 other numbers.

This is a data object created for unity but cannot be seen until it is serializable. Must write this or it will not allow changes in unity. have it extend nothing.
[System.Serializable]
public class Boundary {
    public float xMin, xMax, zMin, zMax;
}

Quaternion.Euler(0f, 0f, rb.velocity.z); This creates a tilt amount I should look more into what Euler and Quaternion is.

Shaders affect how things are displayed in the game without a proper knowledge of all of the shaders it's possible I could run in to not being able to get the game to appear how I wish it to appear.

Diffuse Shader leaves a black box around our bolt shot. They use particales additive Unity 5 defaults to mobile/particles/additive.

Mobile shaders are more efficient and are mostly the same. By choosing to use the mobile additive instead of additive we lose the ability to change the tint on the lazer bolt.

(This fails kinematic makes the physics you are doing not work you should only use kinemetic if the object is completely still) Personal observation is that we should have the bolt be kinematic so that it does not interact with the physics in the game.

In order to get things like directions we can say things like transform.forward possibly getting other relative directions we can grab them from the transform.
