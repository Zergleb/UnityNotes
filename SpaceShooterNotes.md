
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
