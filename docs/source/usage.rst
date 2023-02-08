#####
Usage
#####

.. _usage:

Getting Started
===============
The two most important components of this package are the *AR Placement Guide* and the *Placeable Generator*. Both have to be on the same GameObject as the XR Origin.
It is best to check the sample scene for a working example.

.. image:: images/Inspector.png
    :width: 400

Most settings can be found on those two components. In general your hierachy should look something like this:

.. image:: images/Hierarchy.png
    :width: 400

If you are not using the sample scene as a starting point, you will have to add the *AR Placement Guide* and the *Placeable Generator* to the XR Origin GameObject.
As well as *AR Kit Coaching Overlay* to the *AR Session* GameObject (though this is optional as it is an iOS only feature).

Using your own model
==========
By replacing the *Prefab* on the *Placeable Generator* in the inspector you can use your own prefab.
Just drag in your model and everything should work out of the box.

.. image:: images/CustomPrefab.png
    :width: 400

This prefab should ideally only have a single *MeshRenderer* and a *MeshFilter* attached to it.
A collider will also be added automatically. If you are unsure how to create a prefab, see the section below.
If you are looking for an example prefab check out the sample one. 

Creating a prefab
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. note::
   If you know how to create a prefab, you can skip this section. 

If you have a model that you want to use, you can create a prefab from it.
First import your model into Unity. Then select it in the Hierarchy and drag it into the Project window. This will create a prefab from the model.
This prefab can then be used in the *Placeable Generator*. Just select the XR Origin GameObject and drag the prefab into the *Prefab* field.

`More info on creating prefabs <https://docs.unity3d.com/Manual/CreatingPrefabs.html>`_.

Customizing UI
==========




Parameters
==========

Prefab
----------
A prefab containing the Mesh for the object. The tranform inside the prefab is preserved.


