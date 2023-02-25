# Manual setup

!!! note

    If you used the template project from Github, you can skip this page.

## Creating a Unity Project

It is recommended to start with a new project. The best option is to use the 3D (URP) starting template provided by Unity.

![Image title](images/3DCore.png){ align=left, width=300px }

## Installing AR Placement Kit
In order for the package to work, there a few important requirements:

- Your project needs to use URP (Universal Render Pipeline)
- No version of AR Foundation below 5.0 is installed (When no version is installed, the package will do it)
- You are using Unity 2021.2 or higher


When first installing the package from the package manager it might warn you that the new input system is used. Press *YES* to restart the editor.

![Image title](images/NewInputSystemPrompt.png){ align=left, width=300px }

After the editor has restarted, you can start using the package. If at this point there are any error related to the package, make sure to check it out the troubleshooting section. Again, a new project is the best way to make sure no conflicts with other packages are the problem.


## Setting up AR Foundation

If you have started with a new project, you need to set up AR Foundation. AR Foundation will automatically be installed by the Placement Kit as it is an dependecy.
But it is best to double check in the package manager that it is installed.

![Image title](images/ARFoundationPackage.png){ align=left, width=400px }

Follow the *Install AR Foundation* and *Scene setup* instructions provided in the [ARFoundation Docs](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.0/manual/project-setup/project-setup.html).
For package installation in Unity 2021, see [AR Foundation (Unity 2021)].

!!! note

    Make sure both ARFoundation and ARKit have the same version installed.

### Setup URP with AR Foundation

!!! note

    Skipping this step will result in a glitched image

AR Foundation does not work right away with URP.
You must add an "AR Background Renderer Feature" to the renderer.
Select **Assets -> Settings -> URP-Performant-Renderer.asset**. 

![Image title](images/RendererFile.png){ align=right, width=500px **

In the inspector click **Add Renderer Feature** and select **AR Background Renderer Feature**.

![Image title](images/RendererFeature.png){ align=left, width=380px }

Then, to make sure that the edited Renderer is used, go to **Edit -> Project Settings -> Quality** and set the default quality to "Performant" for all profiles and set "Performant" as the active renderer by clicking the name left of the checkboxes.

![Image title](images/QualitySettings.png){ align=right, width=230px, style="box-shadow: 2px 8px 20px 2px rgba(0, 0, 0, 0.4); margin: 10px; " }

Alternatively, follow [these steps](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.0/manual/project-setup/universal-render-pipeline.html) to set it up by creating the renderer from scratch.


### Setting up iOS (AR Kit)

First, enable ARKit in **Project Settings -> XR Plugin-Management -> iOS -> ARKit**.

![Image title](images/ARKitXRManagement.png){ align=left, width=500px }

Then, require support for it in iOS builds.

![Image title](images/ARKitSupport.png){ align=left, width=500px }

Detailed instructions in the [ARKit Docs](https://docs.unity3d.com/Packages/com.unity.xr.arkit@5.0/manual/project-configuration-arkit.html).

If you have any trouble setting up ARKit, meaning you can't build or get a black screen, take a look at the [Unity Manual for ARCore setup](https://docs.unity3d.com/Packages/com.unity.xr.arcore@5.0/manual/project-configuration-arcore.html).

Additionally, reduce code stripping for iOS by setting **_Project Settings -> Player -> iOS -> Managed Stripping Level** to "Minimal". For more info see [Unity Manual - Code Stripping](https://docs.unity3d.com/Manual/ManagedCodeStripping.html).

![Image title](images/CodeStripping.png){ align=left, width=500px }

### Setting up Android (AR Core)

Follow the instructions from the [ARCore Docs](https://docs.unity3d.com/Packages/com.unity.xr.arcore@5.0/manual/project-configuration-arcore.html).

If you have any trouble setting up ARCore, meaning you can't build or get a black screen, take a look at the [Unity Manual for ARCore setup](https://docs.unity3d.com/Packages/com.unity.xr.arcore@5.0/manual/project-configuration-arcore.html).

#### Optional: For testing inside the unity editor

- Add the **XR Environment** window from **Window -> AR Foundation -> XR**
- inside the **XR Environment**, install the Sample Environments from the drop-down

## Validation

It's recommended to validate the configuration. This can prevent running into errors later on.

![Image title](images/Validation.png){ align=left, width=550px }

You can check Android and iOS. Make sure everything is green before you proceed.

## Setting up Tags and Layers

For the placement guide to function, appropriate Tags and Layers must be set in the Project Settings. The easiest way is to import the preset from the package.
To do this, navigate to **Project Settings -> Tags and Layers**, then click on the preset icon in the top left of the window and choose "Tags&Layers PlacementKit".

![Image title](images/Tags&LayersPreset.png){ align=left, width=400px }

!!! note

    WARNING! This will replace any existing tags or layers.

Alternatively, you can manually add the layers to your Project. The order and index does not matter.

![Image title](images/Tags&Layers.png){ align=left, width=400px }

### Tags

- Placeable
- ReceiveShadows

### Layers

- RepositioningPlane
- Placeable
- SurfaceCollider
- PlaceableContactCollider
- CameraCollider
