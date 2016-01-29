
Enabling Physics is done by adding a Rigid Body component to the Game Object.

Capsule collider can be used for varying shapes of objects and is more efficient than mesh collider.

Can create simplified mesh colliders to be more performant when using mesh collider.

Camera can be perspective or orthographic. It says an upright arcade game uses orthographic but why? Probably check a dictionary. My guess is that perspective renders the edges like eyeballs while orthographic renders the edge scene the same as the middle scene.

Perspective cameras have a Field Of View setting. Making it so your distance doesn't change but you can fit a wider angle in. 

With orthographic you can change the orthographic size which does something similar but probably doesn't give the camera a "wide lens" type of view by enlarging it.

Can click on the label of the field and drag the value and have it update in real time in the Inspector view(When I say label I mean the label "Z" for example in transform rather than the input box for "Z")

Unity 5 has a default skybox in the lighting tab, to remove the skybox you must go there rather than the camera.

Unity 5 Ambient light is now handled in the lighting tab. Ambient light gives a small amount of light on all things regardless of light settings.
