
# Configuration

The two most important components of this package are the AR Placement Guide and the Placeable Generator. Both need to be on the same GameObject as the XR Origin.
It is best to check the sample scene for a working example.

![Image Title](images/XROrigin_Inspector_dark.png#only-dark){ width=400px , class="shaded"}
![Image Title](images/XROrigin_Inspector_light.png#only-light){ width=400px }

These two components contain most of the settings. In general, your hierarchy should look like this

![Image Title](images/Hierarchy_light.png#only-light){ width=400px, align=center }
![Image Title](images/Hierarchy_dark.png#only-dark){ width=200px, align=center, class="shaded" }

If you are not using the sample scene as a starting point, you will need to add the *AR Placement Guide* and *Placeable Generator* to the XR Origin GameObject.
As well as the *AR Kit Coaching Overlay* to the *AR Session* GameObject (although this is optional as it is an iOS only feature).


## Placeable Generator


### Use your own model/Prefab

By replacing the *Prefab* on the *Placeable Generator* in the inspector, you can use your own prefab.
Just drag in your model and everything should work out of the box. The transformation inside the Prefab will be preserved.
Use the scale setting to change the initial scale of the object. It can still be resized at runtime using gestures.

![Image Title](images/CustomPrefab.png){ width=400px, align=center , class="shaded"}

Ideally, this Prefab should only have a single *MeshRenderer* and *MeshFilter* attached to it.

If your model floats too high or is inside the ground, try adjusting the `Pivot Type` setting to match the pivot point of your model. (See [Pivot Type](#pivot-type) and [the troubleshooting section](../troubleshooting/#object-floats-is-in-the-ground))

A collider is also added automatically. If you are not sure how to create a Prefab, see the section below.
If you are looking for an example Prefab, check out the example prefab.


#### Creating a Prefab

!!! note

    If you know how to create a Prefab, you can skip this section.

If you have a model you want to use, you can create a Prefab from it.
First, import your model into Unity. Then select it in the hierarchy and drag it into the project window. This creates a Prefab from the model.
This Prefab can then be used in the Placeable Generator. Simply select the XR Origin GameObject and drag the Prefab into the *Prefab* field.

See also [Unity Manual - Creating Prefabs](https://docs.unity3d.com/Manual/CreatingPrefabs.html).


### Scale
The initial scale of the object in AR.
Change this if your object is either too large or too small at spawn.


### Pivot Type
The y-location of the pivot point in your custom model.
Options are center and bottom, default is center.

This option affects the position relative to the underlying surface and the transformation origin (e.g. for scaling and rotating).


### Advanced Parameters


#### Min Scale

The smallest possible scale for the placeable when using the pinch gesture. If the scale is less than or equal to this value, all instructions to reduce the scale of the placeable will be ignored.


#### Transition speed

The speed at which the placeable transitions between surfaces of different heights.

Higher numbers result in faster transitions.


#### Transition Threshold

The minimum distance for a transition to be triggered. If the distance to the target position is less than this value, the movement will be instantaneous.

Increase this value if the placeable lags behind when dragged with a finger gesture.

Higher values will result in fewer transitions.


## AR Placement Guide

![Image Title](images/ARPlacementGuideAdvanced_light.png#only-light){ width=400px, align=right, padding=30px }
![Image Title](images/ARPlacementGuideAdvanced_dark.png#only-dark){ width=400px, align=right, padding=30px, class="shaded" }


### Enable scaling

Enable scaling of the placeable with a pinch gesture.


### Enable Rotation

Enable rotation of the placeable by rotating the first 2 fingers that touch the screen.

### Advanced parameters

#### Debug Mode

Enables additional logging and visual debugging tools.

#### Rotation Speed

Sets the multiplier for translating finger rotation into placeable rotation.

#### AR Plane Prefab

The material used for planes recognized by the AR system. Uses the default if not set.


