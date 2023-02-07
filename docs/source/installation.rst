#####
Setup
#####

.. autosummary::
   :toctree: generated


Getting Started
===============
**It is recommended to start with a new project. The best option is to use the 3D (URP) starting template provided by Unity when starting a new project.**

.. image:: images/3DCore.png
    :width: 300

In order for the package to work, there a few important requirements:

    - Your project needs to use URP (Universal Render Pipeline)
    - No version of AR Foundation below 5.0 is installed (When no version is installed, the package will do it)
    - You are using Unity 2021.2 or higher

When first installing the package from the package manager it might warn you that the new input system is used. Press *YES* to restart the editor.

.. image:: images/NewInputSystemPrompt.png
    :width: 300

After the editor has restarted, you can start using the package. If at this point there are any error related to the package, make sure to check it out the troubleshooting section. Again, a new project is the best way to make sure no conflicts with other packages are the problem.

=================
Setting up AR Foundation
=================

.. note::
   This following part is only related to AR Foundation. It is the same whether you use AR Placement Kit or not. If you have experience setting AR Foundation you can skip this part.

If you have started with a new project, you need to set up AR Foundation first. AR Foundation is will automatically be installed by the Placement Kit as it is an dependecy. 
But it is best to double check in the package manager that it is installed.

.. image:: images/ARFoundationPackage.png
    :width: 400

Follow the *installation* and *Project setup* instructions provided in the `ARFoundation Docs`_.
For Unity 2021, see `AR Foundation (Unity 2021)`_.

.. note::
   As stated in the Documentation, both ARFoundation and ARKit need to be set to the same version.


Setup URP with AR Foundation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
AR Foundation does not work right away with URP.
Follow these `steps here to set it up <https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.0/manual/project-setup/universal-render-pipeline.html>`_.

.. note::
   Skipping this step will result in a glitched image
   

Setting up for iOS (AR Kit)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Follow the instructions from the `ARKit Docs`_.

.. note::
   You can either install for iOS or Android or both. If you just need a single platform, you can skip the other one.
   The AR scanning guide at the beginning is only available for iOS.

If you have any trouble setting up ARKit, meaning you can't build or get a black screen. `This is a great reference <https://docs.unity3d.com/Packages/com.unity.xr.arkit@5.0/manual/project-configuration-arkit.html>`_.

Setting up for Android (AR Core)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Follow the instructions from the `ARCore Docs`_.

If you have any trouble setting up ARCore, meaning you can't build or get a black screen. `This is a great reference <https://docs.unity3d.com/Packages/com.unity.xr.arcore@5.0/manual/project-configuration-arcore.html>`_.

Optional: For testing inside the unity editor
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- Add the "XR Environment" window from Window -> AR Foundation -> XR 
- inside the "XR Environment", install the Sample Environments from the drop-down 

=================
Validate! Don't skip this
=================
.. note::
   Don't miss this quick step. AR Foundation validates that every thing is set up correctly. If you skip this step, you might get errors later on.

.. image:: images/Validation.png
    :width: 400

You can check Android and iOS. Make sure everything is green.

=================
Sample Scene
=================


.. _ARFoundation Docs: https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.0/manual/project-setup/project-setup.html
.. _ARKit Docs: https://docs.unity3d.com/Packages/com.unity.xr.arkit@5.0/manual/project-configuration-arkit.html
.. _ARCore Docs: https://docs.unity3d.com/Packages/com.unity.xr.arcore@5.0/manual/project-configuration-arcore.html
.. _AR Foundation (Unity 2021): https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.0/manual/project-setup/edit-your-project-manifest.html
