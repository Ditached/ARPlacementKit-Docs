# Quick-start guide

```{eval-rst}
.. autosummary::
   :toctree: generated

```

## Using the template project

```{raw} html
<embed>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/g8V4sUp5q_Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    <div margin-bottom="50px">
    <div padding="50px" height="50px">
</embed>
```

:::{note}
This is the fastest way if you are starting from scratch. It is also the best way to make sure that everything is set up correctly.
:::

We provide a template project ready to use on Github. Make sure you have Unity Version 2021.2 or higher installed.

[Click here for the template project on Github](https://github.com/Ditached/Unity-ARFoundation-Template)

You can either download it using git but for this purpose, just download it as a zip from Github works perfectly fine.

```{image} images/Github.png
:width: 300
```

As it is a publicly accessible repo. The **AR Placement Kit is not included in the project**. You need to download it from the package manager.
You can skip the *Manually Setting up AR Foundation* section when using the template project. Just move on to the [SampleScenehttps://arplacementkit-docs.readthedocs.io/en/latest/installation.html#sample-scene](SampleScenehttps://arplacementkit-docs.readthedocs.io/en/latest/installation.html#sample-scene). section.

## Sample Scene

In the package there is a sample scene. It is located in the folder *Samples* in the package. It is called *ARPlacementKitSample*.
After opening it you should see the following hierachy:

```{image} images/Hierachy.png
:width: 400
```

Before customizing anything, make sure to press *Play* if you have the *XR Simulation* enabled. Otherwise, create a build on your target device to validate that everything works.
If you run into any troubles at this point, check out the {doc}`troubleshooting` section.

It should something like this.

```{image} images/XRSimulation.png
:width: 400
```

:::{note}
If this is your first time using the *XR Simulation* make sure to check out the [documentation](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.0/manual/xr-simulation/simulation-getting-started.html).
:::

The two finger gestures for rotating and scaling will only work on an actual device. The *XR Simulation* does not support it.

[ar foundation (unity 2021)]: https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.0/manual/project-setup/edit-your-project-manifest.html
[arcore docs]: https://docs.unity3d.com/Packages/com.unity.xr.arcore@5.0/manual/project-configuration-arcore.html
[arfoundation docs]: https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.0/manual/project-setup/project-setup.html
[arkit docs]: https://docs.unity3d.com/Packages/com.unity.xr.arkit@5.0/manual/project-configuration-arkit.html
[template project repo]: https://github.com/Ditached/Unity-ARFoundation-Template
[unity manual - code stripping]: https://docs.unity3d.com/Manual/ManagedCodeStripping.html
[unity manual for arcore setup]: https://docs.unity3d.com/Packages/com.unity.xr.arcore@5.0/manual/project-configuration-arcore.html
[unity manual for arkit setup]: https://docs.unity3d.com/Packages/com.unity.xr.arkit@5.0/manual/project-configuration-arkit.html