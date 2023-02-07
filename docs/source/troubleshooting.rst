#####
Troubleshooting
#####

Common Errors
===============


=================
How do I install this package
=================

If you have trouble installing the package, you can check out `this guide from Unity <https://docs.unity3d.com/Manual/upm-ui-import.html>`_.


=================
The image is glitched
=================
If it looks something like this 

.. image:: images/Glitch.jpeg
    :width: 500

when deploying to your device, then URP is not setup with AR Foundation.
Follow these `steps here to fix it <https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.0/manual/project-setup/universal-render-pipeline.html>`_.

=================
Stuff is pink
=================
When objects are rendered pink, you are probably not using the URP (Universal Render Pipeline). Starting the a new project with the 3D (URP) starting template will prevent this problem. But it is also possible to upgrade.
For more information `check out this guide <https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal@15.0/manual/InstallURPIntoAProject.html>`_.


=================
Threading error prevents building
=================
This is a Unity related error. Restarting the project seems to help.


=================
XCode Error requiring provising profile
=================
XCode requires a provising profile whenever you make an build. Setting XCode to automatically manage signing should work.

.. image:: images/XCodeSigning.png
    :width: 500

For further information make sure to check the Unity and or XCode docs.

=================
None of my errors is listed here
=================
Oh no! We do apologize for that. We try to support you as best and as quick as we can. Drop us a mail at support@ditached.de and we will try to help you out.
