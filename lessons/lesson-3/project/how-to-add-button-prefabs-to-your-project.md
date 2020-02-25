# How to Add Button Prefabs to Your Project

Mixed Reality Toolkit is equipped with a variety of button prefabs that you could add to your project. A prefab is a pre-configured GameObject stored as a Unity Asset and can be reused throughout your project.

You can find button prefabs available in MRTK by navigating to **MixedRealityToolkit.SDK** > **Features** > **UX** > **Interactable** > **Prefabs**.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/button_prefabs.PNG)

In this project, you will learn how to change the color of a cube when a button is pressed.

First, select the button of your choice from the Project window and drag into the Hierarchy window.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/drag_button_to_hierarchy.PNG)

Change the button's **Transform Position** so that it's positioned in front of the camera to x = 0, y = 0, and z = 0.5

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/button_transform_position.PNG)

Next, right click on an empty spot in the Hierarchy window and click **3D Object** > **Cube**.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/create_cube.PNG)

With the Cube object still selected, in the Inspector window, change the **Transform Position** so that the cube is located near but not overlapping the button. In addition, resize the cube by changing the **Transform Scale**.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/transform_cube.PNG)

In the Hierarchy window, select the button. In the Inspector window, navigate to the **Interactable (Script)** component.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/interactable_script_component.PNG)

In the **Events** section, expand the **Receivers** section.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/expand_events_receivers.PNG)

Click the **Add Event** button to create a new event receiver of **Event Receiver Type** **InteractableOnPressReceiver**.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/interactableonpressreceiver_new.PNG)

For the newly created **InteractableOnPressReceiver** event, change the **Interaction Filter** to **Near and Far**.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/near_and_far.PNG)

From the Hierarchy window, click and drag the **Cube** GameObject into the **Event Properties** object field for the **On Press()** event to assign the Cube as a receiver of the On Press () event.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/cube_receiver.PNG)

Next, click the action dropdown (currently assigned **No Function**) and select **MeshRenderer** > **Material material**. This action will set the Cube's material property to change when the button is pressed.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/material_material.PNG)

Now, assign a color for the Cube to change to when the button is pressed. Click the small **circle** icon next to the **Material** field (currently assigned **None (Material)**) to open the **Select Material** window.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/select_material.PNG)

MRTK provides a variety of materials that can be used in your projects. In the search bar, search for **MRTK_Standard** and select your color of choice.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/search_mrtk_standard.PNG)

Now that the event is configured for when the button is pressed, you now need to configure an event that occurs when the button is released. For the **On Release ()** event, click and drag the **Cube** GameObject into the **Event Properties**.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/on_release_assign_cube.PNG)

Next, click the action dropdown (currently assigned **No Function**) and select **MeshRenderer** > **Material material**. This action will set the Cube's material property to change when the button is released.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/on_release_material_material.PNG)

Now, assign a color for the Cube to change to when the button is released. Click the small circle icon next to the Material field (currently assigned None (Material)) to open the Select Material window and search for **MRTK_Standard**. Select your choice of color.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/on_release_color.PNG)

Now that both the On Press () and On Trigger () events are configured for the button, press **Play** to enter Game mode and test the button in the in-editor simulator.

To press the button, press the spacebar + mouse scroll forward.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/button_pressed_magenta.PNG)

To release the button, press the spacebar + mouse scroll backward.

![MRTK Button Prefabs](../../../.gitbook/assets/how_to_add_button_prefabs_to_your_project/button_release_green.PNG)