:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/master/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/master/doc/classes/XRPositionalTracker.xml.

.. _class_XRPositionalTracker:

XRPositionalTracker
===================

**Inherits:** :ref:`XRTracker<class_XRTracker>` **<** :ref:`RefCounted<class_RefCounted>` **<** :ref:`Object<class_Object>`

**Inherited By:** :ref:`XRBodyTracker<class_XRBodyTracker>`, :ref:`XRControllerTracker<class_XRControllerTracker>`, :ref:`XRHandTracker<class_XRHandTracker>`

A tracked object.

.. rst-class:: classref-introduction-group

Description
-----------

An instance of this object represents a device that is tracked, such as a controller or anchor point. HMDs aren't represented here as they are handled internally.

As controllers are turned on and the :ref:`XRInterface<class_XRInterface>` detects them, instances of this object are automatically added to this list of active tracking objects accessible through the :ref:`XRServer<class_XRServer>`.

The :ref:`XRNode3D<class_XRNode3D>` and :ref:`XRAnchor3D<class_XRAnchor3D>` both consume objects of this type and should be used in your project. The positional trackers are just under-the-hood objects that make this all work. These are mostly exposed so that GDExtension-based interfaces can interact with them.

.. rst-class:: classref-introduction-group

Tutorials
---------

- :doc:`XR documentation index <../tutorials/xr/index>`

.. rst-class:: classref-reftable-group

Properties
----------

.. table::
   :widths: auto

   +----------------------------------------------------------+------------------------------------------------------------+--------+
   | :ref:`TrackerHand<enum_XRPositionalTracker_TrackerHand>` | :ref:`hand<class_XRPositionalTracker_property_hand>`       | ``0``  |
   +----------------------------------------------------------+------------------------------------------------------------+--------+
   | :ref:`String<class_String>`                              | :ref:`profile<class_XRPositionalTracker_property_profile>` | ``""`` |
   +----------------------------------------------------------+------------------------------------------------------------+--------+

.. rst-class:: classref-reftable-group

Methods
-------

.. table::
   :widths: auto

   +-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Variant<class_Variant>` | :ref:`get_input<class_XRPositionalTracker_method_get_input>`\ (\ name\: :ref:`StringName<class_StringName>`\ ) |const|                                                                                                                                                                                                                              |
   +-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`XRPose<class_XRPose>`   | :ref:`get_pose<class_XRPositionalTracker_method_get_pose>`\ (\ name\: :ref:`StringName<class_StringName>`\ ) |const|                                                                                                                                                                                                                                |
   +-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`bool<class_bool>`       | :ref:`has_pose<class_XRPositionalTracker_method_has_pose>`\ (\ name\: :ref:`StringName<class_StringName>`\ ) |const|                                                                                                                                                                                                                                |
   +-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                        | :ref:`invalidate_pose<class_XRPositionalTracker_method_invalidate_pose>`\ (\ name\: :ref:`StringName<class_StringName>`\ )                                                                                                                                                                                                                          |
   +-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                        | :ref:`set_input<class_XRPositionalTracker_method_set_input>`\ (\ name\: :ref:`StringName<class_StringName>`, value\: :ref:`Variant<class_Variant>`\ )                                                                                                                                                                                               |
   +-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                        | :ref:`set_pose<class_XRPositionalTracker_method_set_pose>`\ (\ name\: :ref:`StringName<class_StringName>`, transform\: :ref:`Transform3D<class_Transform3D>`, linear_velocity\: :ref:`Vector3<class_Vector3>`, angular_velocity\: :ref:`Vector3<class_Vector3>`, tracking_confidence\: :ref:`TrackingConfidence<enum_XRPose_TrackingConfidence>`\ ) |
   +-------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Signals
-------

.. _class_XRPositionalTracker_signal_button_pressed:

.. rst-class:: classref-signal

**button_pressed**\ (\ name\: :ref:`String<class_String>`\ ) :ref:`🔗<class_XRPositionalTracker_signal_button_pressed>`

Emitted when a button on this tracker is pressed. Note that many XR runtimes allow other inputs to be mapped to buttons.

.. rst-class:: classref-item-separator

----

.. _class_XRPositionalTracker_signal_button_released:

.. rst-class:: classref-signal

**button_released**\ (\ name\: :ref:`String<class_String>`\ ) :ref:`🔗<class_XRPositionalTracker_signal_button_released>`

Emitted when a button on this tracker is released.

.. rst-class:: classref-item-separator

----

.. _class_XRPositionalTracker_signal_input_float_changed:

.. rst-class:: classref-signal

**input_float_changed**\ (\ name\: :ref:`String<class_String>`, value\: :ref:`float<class_float>`\ ) :ref:`🔗<class_XRPositionalTracker_signal_input_float_changed>`

Emitted when a trigger or similar input on this tracker changes value.

.. rst-class:: classref-item-separator

----

.. _class_XRPositionalTracker_signal_input_vector2_changed:

.. rst-class:: classref-signal

**input_vector2_changed**\ (\ name\: :ref:`String<class_String>`, vector\: :ref:`Vector2<class_Vector2>`\ ) :ref:`🔗<class_XRPositionalTracker_signal_input_vector2_changed>`

Emitted when a thumbstick or thumbpad on this tracker moves.

.. rst-class:: classref-item-separator

----

.. _class_XRPositionalTracker_signal_pose_changed:

.. rst-class:: classref-signal

**pose_changed**\ (\ pose\: :ref:`XRPose<class_XRPose>`\ ) :ref:`🔗<class_XRPositionalTracker_signal_pose_changed>`

Emitted when the state of a pose tracked by this tracker changes.

.. rst-class:: classref-item-separator

----

.. _class_XRPositionalTracker_signal_pose_lost_tracking:

.. rst-class:: classref-signal

**pose_lost_tracking**\ (\ pose\: :ref:`XRPose<class_XRPose>`\ ) :ref:`🔗<class_XRPositionalTracker_signal_pose_lost_tracking>`

Emitted when a pose tracked by this tracker stops getting updated tracking data.

.. rst-class:: classref-item-separator

----

.. _class_XRPositionalTracker_signal_profile_changed:

.. rst-class:: classref-signal

**profile_changed**\ (\ role\: :ref:`String<class_String>`\ ) :ref:`🔗<class_XRPositionalTracker_signal_profile_changed>`

Emitted when the profile of our tracker changes.

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Enumerations
------------

.. _enum_XRPositionalTracker_TrackerHand:

.. rst-class:: classref-enumeration

enum **TrackerHand**: :ref:`🔗<enum_XRPositionalTracker_TrackerHand>`

.. _class_XRPositionalTracker_constant_TRACKER_HAND_UNKNOWN:

.. rst-class:: classref-enumeration-constant

:ref:`TrackerHand<enum_XRPositionalTracker_TrackerHand>` **TRACKER_HAND_UNKNOWN** = ``0``

The hand this tracker is held in is unknown or not applicable.

.. _class_XRPositionalTracker_constant_TRACKER_HAND_LEFT:

.. rst-class:: classref-enumeration-constant

:ref:`TrackerHand<enum_XRPositionalTracker_TrackerHand>` **TRACKER_HAND_LEFT** = ``1``

This tracker is the left hand controller.

.. _class_XRPositionalTracker_constant_TRACKER_HAND_RIGHT:

.. rst-class:: classref-enumeration-constant

:ref:`TrackerHand<enum_XRPositionalTracker_TrackerHand>` **TRACKER_HAND_RIGHT** = ``2``

This tracker is the right hand controller.

.. _class_XRPositionalTracker_constant_TRACKER_HAND_MAX:

.. rst-class:: classref-enumeration-constant

:ref:`TrackerHand<enum_XRPositionalTracker_TrackerHand>` **TRACKER_HAND_MAX** = ``3``

Represents the size of the :ref:`TrackerHand<enum_XRPositionalTracker_TrackerHand>` enum.

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Property Descriptions
---------------------

.. _class_XRPositionalTracker_property_hand:

.. rst-class:: classref-property

:ref:`TrackerHand<enum_XRPositionalTracker_TrackerHand>` **hand** = ``0`` :ref:`🔗<class_XRPositionalTracker_property_hand>`

.. rst-class:: classref-property-setget

- |void| **set_tracker_hand**\ (\ value\: :ref:`TrackerHand<enum_XRPositionalTracker_TrackerHand>`\ )
- :ref:`TrackerHand<enum_XRPositionalTracker_TrackerHand>` **get_tracker_hand**\ (\ )

Defines which hand this tracker relates to.

.. rst-class:: classref-item-separator

----

.. _class_XRPositionalTracker_property_profile:

.. rst-class:: classref-property

:ref:`String<class_String>` **profile** = ``""`` :ref:`🔗<class_XRPositionalTracker_property_profile>`

.. rst-class:: classref-property-setget

- |void| **set_tracker_profile**\ (\ value\: :ref:`String<class_String>`\ )
- :ref:`String<class_String>` **get_tracker_profile**\ (\ )

The profile associated with this tracker, interface dependent but will indicate the type of controller being tracked.

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Method Descriptions
-------------------

.. _class_XRPositionalTracker_method_get_input:

.. rst-class:: classref-method

:ref:`Variant<class_Variant>` **get_input**\ (\ name\: :ref:`StringName<class_StringName>`\ ) |const| :ref:`🔗<class_XRPositionalTracker_method_get_input>`

**Deprecated:** Use through :ref:`XRControllerTracker<class_XRControllerTracker>`.

Returns an input for this tracker. It can return a boolean, float or :ref:`Vector2<class_Vector2>` value depending on whether the input is a button, trigger or thumbstick/thumbpad.

.. rst-class:: classref-item-separator

----

.. _class_XRPositionalTracker_method_get_pose:

.. rst-class:: classref-method

:ref:`XRPose<class_XRPose>` **get_pose**\ (\ name\: :ref:`StringName<class_StringName>`\ ) |const| :ref:`🔗<class_XRPositionalTracker_method_get_pose>`

Returns the current :ref:`XRPose<class_XRPose>` state object for the bound ``name`` pose.

.. rst-class:: classref-item-separator

----

.. _class_XRPositionalTracker_method_has_pose:

.. rst-class:: classref-method

:ref:`bool<class_bool>` **has_pose**\ (\ name\: :ref:`StringName<class_StringName>`\ ) |const| :ref:`🔗<class_XRPositionalTracker_method_has_pose>`

Returns ``true`` if the tracker is available and is currently tracking the bound ``name`` pose.

.. rst-class:: classref-item-separator

----

.. _class_XRPositionalTracker_method_invalidate_pose:

.. rst-class:: classref-method

|void| **invalidate_pose**\ (\ name\: :ref:`StringName<class_StringName>`\ ) :ref:`🔗<class_XRPositionalTracker_method_invalidate_pose>`

Marks this pose as invalid, we don't clear the last reported state but it allows users to decide if trackers need to be hidden if we lose tracking or just remain at their last known position.

.. rst-class:: classref-item-separator

----

.. _class_XRPositionalTracker_method_set_input:

.. rst-class:: classref-method

|void| **set_input**\ (\ name\: :ref:`StringName<class_StringName>`, value\: :ref:`Variant<class_Variant>`\ ) :ref:`🔗<class_XRPositionalTracker_method_set_input>`

**Deprecated:** Use through :ref:`XRControllerTracker<class_XRControllerTracker>`.

Changes the value for the given input. This method is called by an :ref:`XRInterface<class_XRInterface>` implementation and should not be used directly.

.. rst-class:: classref-item-separator

----

.. _class_XRPositionalTracker_method_set_pose:

.. rst-class:: classref-method

|void| **set_pose**\ (\ name\: :ref:`StringName<class_StringName>`, transform\: :ref:`Transform3D<class_Transform3D>`, linear_velocity\: :ref:`Vector3<class_Vector3>`, angular_velocity\: :ref:`Vector3<class_Vector3>`, tracking_confidence\: :ref:`TrackingConfidence<enum_XRPose_TrackingConfidence>`\ ) :ref:`🔗<class_XRPositionalTracker_method_set_pose>`

Sets the transform, linear velocity, angular velocity and tracking confidence for the given pose. This method is called by an :ref:`XRInterface<class_XRInterface>` implementation and should not be used directly.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |required| replace:: :abbr:`required (This method is required to be overridden when extending its base class.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
.. |bitfield| replace:: :abbr:`BitField (This value is an integer composed as a bitmask of the following flags.)`
.. |void| replace:: :abbr:`void (No return value.)`
