# What is Scene Understanding?

Your mixed reality device is constantly integrating information about what it sees in your environment. Scene Understanding funnels all of these data sources and produces **one single cohesive abstraction**.

{% hint style="danger" %}
Note that Scene Understanding SDK is only available for **HoloLens 2**.
{% endhint %}

The goal of **Scene understanding** is to **transform** the **un-structured environment sensor data** that your Mixed Reality device captures and to convert it into a powerful but abstracted representation that is intuitive and easy to develop for. [The Scene Understanding SDK](https://aka.ms/UnitySceneUnderstandingSDK) acts as the communication layer between your application and the Scene Understanding runtime. It's aimed to mimic existing standard constructs such as 3d scene graphs for 3d representations and 2D rectangles/panels for 2d applications. While the constructs Scene Understanding mimics will map to concrete frameworks you may use, in general SceneUnderstanding is framework agnostic allowing for interop between varied frameworks that interact with it.

![Common spatial mapping usage scenarios: placement, occlusion, physics and navigation.](../../../.gitbook/assets/sceneunderstandingusage.png)

{% hint style="info" %}
The process of converting the raw sensor data into a Scene is a potentially **expensive operation** that could take seconds for **medium spaces \(~10x10m\)** to minutes for **very large spaces \(~50x50m\)** and therefore it is not something that is being computed by the device without application **request.**
{% endhint %}

