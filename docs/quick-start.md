# Quick Start

This guide uses the template project provided for this package. If you want to integrate ARPlacementKit into an existing project, see [manual setup](../installation) instead.

![type:video](https://www.youtube.com/embed/g8V4sUp5q_Q)

!!! note

    This is the fastest way if you are starting from scratch. It is also the best way to make sure that everything is set up correctly.


## 1. Download the template project


We provide a ready-to-use template project on Github. Make sure you have Unity version 2021.2 or higher installed.

[Download: Unity ARFoundation Template](https://github.com/Ditached/Unity-ARFoundation-Template)

You can clone it using git but for this purpose, just download it as a zip from Github.
After downloading, open the project with Unity (usually via Unity Hub).

![Image title](images/Github.png){ align=left, width=300px , class="shaded" }

!!! note 

    As this is a public repo, the **AR Placement Kit is not included in the project**. You will need to download it using the Unity package manager.

## 2. Load the sample scene
Load the sample scene from `Assets -> Scenes -> SampleScene.unity`

## 3. Import TMP Essentials
A popup window will open asking you to import Text Mesh Pro into the project. Click `Import TMP Essentials`.


## 4. XR Environment
Select the XR Environment preset in the XR Environment window (e.g. `Kitchen -> Kitchen_17ftx16ft`). 

![Image title](images/XRSim_LoadEnv.png){ align=left, width=300px , class="shaded" }

If you don't see a window titled `XR Environment`, go to `Window -> XR -> AR Foundation -> XR Environment` to open it.

### Setting the Resolution in Game View
To simulate a realistic aspect ratio and resolution, set the resolution from the Game View drop-down menu. 

![Placeholder](images/GameView_Resolution_dark.png){ align=left, width=400px , class="shaded" }


### Navigation & Controls

Hold down the right mouse button to navigate the camera. Move with the W, A, S, D keys and rotate the camera by moving the cursor. Clicks are translated into touch events. Moving the camera triggers surface detection.


!!! note


    The two finger gestures for rotating and scaling will only work on a real mobile device. XR Simulation does not support them.


!!! note 


    In the example project, the simulated surface recognition is adjusted so that surfaces are recognized faster. See `Project Settings -> XR Plug-In Management -> XR Simulation`.

![Placeholder](images/XRSim_RecognitionSettings_dark.png){ align=left, width=400px , class="shaded" }

For more information see the [XRSimulation Docs](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.1/manual/xr-simulation/simulation-environments.html).

### If shaders are glitched
Sometimes, when opening an XR simulated environment for the first time, shaders are gliched. If that happens, restart the Unity Editor.

![Placeholder](images/XREnvGlitch.png){ align=left, width=200px , class="shaded" }

See also [Troubleshooting](./troubleshooting.md) and the [XRSimulation Docs](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.1/manual/xr-simulation/simulation.html).



## 5. Install ARPlacementKit
Select and install ARPlacementKit from the Unity Asset store.
A popup will appear, warning you about Package Manager dependecies. Click `Install/Upgrade`.
In the import dialog select everything and click `Import`.

Next, open the AR Placement Kit Sample Scene from `Assets -> AR Placement Kit -> Samples -> ARPlacingSample -> ARPlacementKitSample.untiy`.

After opening it, you should see the following hierarchy:

![Image title](images/Hierarchy_light.png#only-light){ align=left, width=400px }
![Image title](images/Hierarchy_dark.png#only-dark){ align=left, width=200px , class="shaded" }

!!! note

    If the XR Environment (e.g. the kitchen scene) is not visible in the XR Environment and/or Game window, restart the Unity Editor again.


## 6. Test the setup
Before customizing anything, make sure to press *Play* to see if everything works. Alternatively, create a build on your target device.
If you encounter any problems at this point, see the [troubleshooting](./troubleshooting.md) section.

After looking around and placing the object, it should look something like this:

![Image title](images/XRSim_WorkingExample_light.png#only-light){ align=left, width=200px }
![Image title](images/XRSim_WorkingExample_dark.png#only-dark){ align=left, width=200px , class="shaded" }

