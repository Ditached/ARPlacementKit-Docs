#####
Setup
#####

.. autosummary::
   :toctree: generated


Install packages
================

1. Start a new empty Unity Project using either the built-in pipeline or the URP.
2. Delete the main camera from the scene

AR Foundation 5
---------------

Follow the *installation* and *Project setup* instructions provided in the `ARFoundation Docs`_.
For Unity 2021, see `AR Foundation (Unity 2021)`_.

.. note::
   As stated in the Documentation, both ARFoundation and ARKit need to be set to the same version.

Optional: For testing inside the unity editor
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- Add the "XR Environment" window from Window -> AR Foundation -> XR 
- inside the "XR Environment", install the Sample Environments from the drop-down 



iOS Support via ARKit
---------------------
Follow the instructions from the `ARKit Docs`_.


ARPLacemetKit (this package)
-------------

- Install from the package manager
- Add the *Scripts/ARPlacementGuide* Component to XROrigin; a PlaceableGenerator Component will be added as well
- Choose the desired prefab in the PlaceableGenerator






.. _ARFoundation Docs: https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.0/manual/project-setup/project-setup.html
.. _ARKit Docs: https://docs.unity3d.com/Packages/com.unity.xr.arkit@5.0/manual/project-configuration-arkit.html

.. _AR Foundation (Unity 2021): https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.0/manual/project-setup/edit-your-project-manifest.html
