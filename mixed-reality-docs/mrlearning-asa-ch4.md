---
title: Azure Spatial Anchors tutorials - 1. Getting started with Azure Spatial Anchors
description: Complete this course to learn how to implement Azure Face Recognition within a mixed reality application.
author: jessemcculloch
ms.author: jemccull
ms.date: 02/26/2019
ms.topic: article
keywords: mixed reality, unity, tutorial, hololens
ms.localizationpriority: high
---

# 4. Build your Azure spatial anchors application for android/iOS device using AR Foundation

## **Section 1.0**

## Adding inbuilt Unity packages

To support Android device we have to import  below unity packages with specific versions 

a. **ARFoundation 2.1.4**

b.  **ARCore XR plugin 2.2.0 preview 2**

**Step 1:**

In the Unity menu, select **Window** > **Package Manager**:

![image-20200422075550526](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422075550526.png)

It might take a few seconds before the AR Foundation package appears in the list.

In the Package Manager window, select **AR Foundation** , select See all version and select version 2.1.4 and install the package by clicking the **Install** button:

![image-20200422075910777](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422075910777.png)

**Step 2:**

Repeat the same process of step 1 to import  **ARCore XR plugin 2.2.0 preview 2**

if you not able to find specific ARCore XR plugin , first install version 2.0.2  

![image-20200422080455672](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422080455672.png)

After installation we can  update specific version 2.2.0 preview 2

![image-20200422080652614](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422080652614.png)



## Section 1.1

## Customize MRTK to support ARFoundation (ARCore / ARkit) Camera

**Step 1:**

Select MixedRealitytToolKit in Hierarchy section and select clone button on Mixed Reality ToolKit (Script) at inspector section(Right side of Window)

![image-20200422083043653](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422083043653.png)

Here we are just taking the copy of setting to make it in editable format

After selecting clone button a new Clone Profile window will we opened , Rename Profile name with “UnityARConfigurationProfile” and click on Clone button

**Step 2:**

Similar to Step 1 clone the Camera settings at inspector window (Right bottom of window) 

![image-20200422085303818](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422085303818.png)

And Rename Profile name with “UnityARConfigurationProfile ”  2 and click on Clone button

**Step 3:**

While Selecting MixedRealitytToolKit in Hierarchy expand the camera setting providers in inspector window and  click on **+Add Camera Setting Provider** > expand **New data provider 1**> select Type **None** >select **Microsoft .MixedReality.Toolkit.Experimental.UnityAR**  > Select **UnityARCameraSettings**

![image-20200422092357030](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422092357030.png)

**Step 4:**

**Adding supporting scripts**

While Selecting MixedRealitytToolKit in Hierarchy click on Add component button at inspector window

And type **AR reference Point manager** in search bar and  select the script

![image-20200422093717471](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422093717471.png)

2 script **AR Session Origin** and  **AR reference Point manager** will be added to inspector window like below 

![image-20200422093845833](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422093845833.png)



## Section 2.0

## Build Application to Android Device

Go to File at top of window and select Build setting 

![image-20200422100920036](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422100920036.png)

A new window will be appear on screen,then select Android and click on switch platform

![image-20200422105815525](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422105815525.png)

It will take few minutes to switch 

Then click on **Add open scenes** and make sure your scene added correctly

![image-20200422103018560](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422103018560.png)

Click on Player setting to make changes for Android

In player settings expand XR setting and select **Virtual Reality Support**  and **None** by selecting "+" Symbol

![image-20200422103744879](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422103744879.png)

In player settings expand Other setting and select **Vulkan**  and remove it by selecting "-" Symbol

![image-20200422104317725](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422104317725.png)

Close player setting and click on Build button and save the Apk file 



## Section 3.0

## Build Application to ios Device

To support ios device we have to import below one more unity packages with specific versions 

**ARKit XR plugin 2.1.1**

To do this repeat the same procedure of  **Section 1.0** > **step 1** and install the package

![image-20200422113237530](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422113237530.png)

Go to File at top of window and select Build setting

![image-20200422100920036](C:\Users\Veeruby Technology\AppData\Roaming\Typora\typora-user-images\image-20200422100920036.png)

A new window will be appear on screen,then select iOS and click on switch platform and keep the same player settings like Android











## Overview

Welcome to the second series of the HoloLens 2 tutorials. In this three-part tutorial series, you will learn the fundamentals of Azure Spatial Anchors.

In this first tutorial, [Getting started with Azure Spatial Anchors](mrlearning-asa-ch1.md), you will explore the various steps required to start and stop an Azure session and create, upload, and download Azure anchors on a single device.

In the second tutorial, [Saving, retrieving, and sharing Azure Spatial Anchors](mrlearning-asa-ch2.md), you will learn how to save Azure Spatial Anchors across multiple app sessions by saving anchor information to the HoloLens 2's storage and how to share this anchor information to other devices for a multi-device anchor alignment.

In the third tutorial, [Displaying Azure Spatial Anchor feedback](mrlearning-asa-ch3.md), you will learn how to provide users with feedback about anchor events and statuses when using Azure Spatial Anchors.

## Objectives

* Learn the fundamentals of developing with Azure Spatial Anchors for HoloLens 2
* Create, upload, and download spatial anchors

## Prerequisites

>[!TIP]
>If you have not completed the [Getting started tutorials](mrlearning-base.md) series yet, it's recommended that you complete those tutorials first.

* A Windows 10 PC configured with the correct [tools installed](install-the-tools.md)
* Windows 10 SDK 10.0.18362.0 or later
* Some basic C# programming ability
* A HoloLens 2 device [configured for development](using-visual-studio.md#enabling-developer-mode)
* <a href="https://docs.unity3d.com/Manual/GettingStartedInstallingHub.html" target="_blank">Unity Hub</a> with Unity 2019.2.X installed and the Universal Windows Platform Build Support module added
* Complete the [Create a Spatial Anchors resource](https://docs.microsoft.com/azure/spatial-anchors/quickstarts/get-started-unity-hololens#create-a-spatial-anchors-resource) section of the [Quickstart: Create a Unity HoloLens app that uses Azure Spatial Anchors](https://docs.microsoft.com/azure/spatial-anchors/quickstarts/get-started-unity-hololens) tutorial.

> [!IMPORTANT]
> The recommended Unity version for this tutorial series is Unity 2019.2.X. This supersedes any Unity version requirements or recommendations stated in the prerequisites linked above.

## Creating the Unity project
<!-- TODO: Consider renaming to 'Creating and preparing the Unity project'-->

In this section, you will create a new Unity project and get it ready for MRTK development.

For this, first follow the [Initializing your project and first application](mrlearning-base-ch1.md), excluding the [Build your application to your device](mrlearning-base-ch1.md#build-your-application-to-your-device) instructions, which includes the following steps:

1. [Create new Unity project](mrlearning-base-ch1.md#create-new-unity-project) and give it a suitable name, for example, *MRTK Tutorials*

2. [Configure the Unity project for Windows Mixed Reality](mrlearning-base-ch1.md#configure-the-unity-project-for-windows-mixed-reality)

3. [Import TextMesh Pro Essential Resources](mrlearning-base-ch1.md#import-textmesh-pro-essential-resources)

4. [Import the Mixed Reality Toolkit](mrlearning-base-ch1.md#import-the-mixed-reality-toolkit)

5. [Configure the Unity project for the Mixed Reality Toolkit](mrlearning-base-ch1.md#configure-the-unity-project-for-the-mixed-reality-toolkit)

6. [Add the Mixed Reality Toolkit to the Unity scene](mrlearning-base-ch1.md#configure-the-mixed-reality-toolkit) and give the scene a suitable name, for example, *AzureSpatialAnchors*

Then follow the [How to configure the Mixed Reality Toolkit Profiles (Change Spatial Awareness Display Option)](mrlearning-base-ch2.md#how-to-configure-the-mixed-reality-toolkit-profiles-change-spatial-awareness-display-option) instructions to change the MRTK configuration profile for your scene to the **DefaultHoloLens2ConfigurationProfile** and change the display options for the spatial awareness mesh to **Occlusion**.

> [!CAUTION]
> As mentioned in the [Configure the Unity project for the Mixed Reality Toolkit](mrlearning-base-ch1.md#configure-the-unity-project-for-the-mixed-reality-toolkit) instructions linked above, it is strongly recommended to not enable MSBuild for Unity.

## Adding inbuilt Unity packages
<!-- TODO: Consider renaming to 'Installing AR Foundation' -->

In this section, you will install Unity's inbuilt AR Foundation package because it is required by the Azure Spatial Anchors SDK you will import in the next section.

In the Unity menu, select **Window** > **Package Manager**:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section2-step1-1.png)

> [!NOTE]
> It might take a few seconds before the AR Foundation package appears in the list.

In the Package Manager window, select **AR Foundation** and install the package by clicking the **Install** button:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section2-step1-2.png)

## Importing the tutorial assets

Download and **import** the following Unity custom packages **in the order they are listed**:

* [AzureSpatialAnchors.unitypackage](https://github.com/Azure/azure-spatial-anchors-samples/releases/download/v2.1.1/AzureSpatialAnchors.unitypackage) (version 2.1.1)
* [MRTK.HoloLens2.Unity.Tutorials.Assets.GettingStarted.2.3.0.2.unitypackage](https://github.com/microsoft/MixedRealityLearning/releases/download/getting-started-v2.3.0.2/MRTK.HoloLens2.Unity.Tutorials.Assets.GettingStarted.2.3.0.2.unitypackage)
* [MRTK.HoloLens2.Unity.Tutorials.Assets.AzureSpatialAnchors.2.3.0.0.unitypackage](https://github.com/microsoft/MixedRealityLearning/releases/download/azure-spatial-anchors-v2.3.0.0/MRTK.HoloLens2.Unity.Tutorials.Assets.AzureSpatialAnchors.2.3.0.0.unitypackage)

> [!TIP]
> For a reminder on how to import a Unity custom package, you can refer to the [Import the Mixed Reality Toolkit](mrlearning-base-ch1.md#import-the-mixed-reality-toolkit) instructions.

After you have imported the tutorial assets your Project window should look similar to this:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section3-step1-1.png)

## Creating and preparing the scene
<!-- TODO: Consider renaming to 'Preparing the scene' -->

In this section, you will prepare the scene by adding some of the tutorial prefabs.

In the Project window, navigate to **Assets** > **MRTK.Tutorials.AzureSpatialAnchors** > **Prefabs** folder. While holding down the CTRL button, click on **ButtonParent**, **DebugWindow**, **Instructions**, and **ParentAnchor** to select the four prefabs:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section4-step1-1.png)

With the four prefabs still selected, drag them into the Hierarchy window to add them to the scene:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section4-step1-2.png)

To focus in on the objects in the scene, you can double-click on the ParentAnchor object, and then zoom slightly out again:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section4-step1-3.png)

> [!TIP]
> If you find the large icons in your scene, for example, the large framed 'T' icons distracting, you can hide these by <a href="https://docs.unity3d.com/2019.1/Documentation/Manual/GizmosMenu.html" target="_blank">toggling the Gizmos</a> to the off position.

## Configuring the buttons to operate the scene

In this section, you will add scripts into the scene to create a series of button events that demonstrate the fundamentals of how both local anchors and Azure Spatial Anchors behave in an application.

### 1. Configure the Pressable Button Holo Lens 2 (Script) component

In the Hierarchy window, expand the **ButtonParent** object and select the first child object named **StartAzureSession**:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section5-step1-1.png)

In the Inspector window, locate the **Pressable Button Holo Lens 2 (Script)** component and add a new event listener to the **Button Pressed ()** event by clicking the **+** icon:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section5-step1-2.png)

With the StartAzureSession object still selected in the Hierarchy window, click-and-drag the **ParentAnchor** object from the Hierarchy window into the empty **None (Object)** field of the event listener you just added to make the ParentAnchor object listen for button pressed events from this button:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section5-step1-3.png)

Click the **No Function** dropdown of the same event listener, then select **AnchorModuleScript** > **StartAzureSession ()** to set the StartAzureSession () function as the action that is triggered when the button pressed events is fired from this button:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section5-step1-4.png)

### 2. Configure the Interactable (Script) component

With the StartAzureSession object still selected in the Hierarchy window, in the Inspector window, locate the **Interactable (Script)** component and repeat the same process as in step 1 above for the **OnClick ()** event:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section5-step2-1.png)

### 3. Configure the remaining buttons

For each of the remaining buttons, complete the process outlined in step 1 and 2 above to assign functions to both the **Button Pressed ()** and **OnClick ()** events:

* For the **StopAzureSession** object, assign the AnchorModuleScript > **StopAzureSession ()** function.
* For the **CreateAzureAnchor** object, assign the AnchorModuleScript > **CreateAzureAnchor ()** function,
  * then drag the **ParentAnchor** again into the empty **None (Game Object)** field.
* For the **RemoveLocalAnchor** object, assign the AnchorModuleScript > **RemoveLocalAnchor ()** function,
  * then drag the **ParentAnchor** again into the empty **None (Game Object)** field.
* For the **FindAzureAnchor** object, assign the AnchorModuleScript > **FindAzureAnchor ()** function.
* For the **DeleteAzureAnchor** object, assign the AnchorModuleScript > **DeleteAzureAnchor ()** function.

### 4. Connect the scene to the Azure resource

In the Hierarchy window, select the **ParentAnchor** object and in the Inspector window, scroll down to the **Spatial Anchor Manager (Script)** component.

Then, in the **Credentials** section, paste your Spatial Anchors Account ID and Key, which you created as part of this tutorial's [Prerequisites](mrlearning-asa-ch1.md#prerequisites), into the corresponding **Spatial Anchors Account Id** and **Spatial Anchors Account Key** fields:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section5-step4-1.png)

## Trying the basic behaviors of Azure Spatial Anchors

Now that your scene is configured to demonstrate the basics of Azure Spatial Anchors, it is time to deploy the app so you can experience Azure Spatial Anchors firsthand.

### 1. Add additional required capabilities

In the Unity menu, select **Edit** > **Project Settings...** to open the Player Settings window:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section6-step1-1.png)

In the Player Settings window, select **Player** and then **Publishing Settings**:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section6-step1-2.png)

In the  **Publishing Settings**, scroll down to the **Capabilities** section and double-check that the **InternetClient**, **Microphone**, and **SpatialPerception** capabilities, which you enabled when you created the project at the beginning of the tutorial, are enabled. Then, enable the **InternetClientServer**, **PrivateNetworkClientServer**, **RemovableStorage**, and **Webcam** capabilities:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section6-step1-3.png)

### 2. Deploy the app to your HoloLens 2

Azure Spatial Anchors can not run in Unity, so to test the Azure Spatial Anchors functionality, you need to deploy the project to your device.

> [!TIP]
> For a reminder on how to build and deploy your Unity project to HoloLens 2, you can refer to the [Build your application to your device](mrlearning-base-ch1.md#build-your-application-to-your-device) instructions.

### 3. Run the app on your HoloLens 2 and follow the in-app instructions

> [!CAUTION]
> Azure Spatial Anchors uses the internet to save and load the anchor data so make sure your device is connected to the internet.

When the application is running on your device, follow the on-screen instructions displayed on the Azure Spatial Anchor Tutorial Instructions panel:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section6-step3-1.png)

## Anchoring an experience

In the previous sections, you learned the fundamentals of Azure Spatial Anchors. We used a cube to represent and visualize the parent game object with the attached anchor. In this section, you will learn how to anchor an entire experience by placing it as a child of the ParentAnchor object.

### 1. Add the Rocket Launcher experience

In the Project window, navigate to the **Assets** > **MRTK.Tutorials.GettingStarted** > **Prefabs** > **RocketLauncher** folder and select the **RocketLauncher_Complete** prefab:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section7-step1-1.png)

With the RocketLauncher_Complete prefab still selected, drag it on top of the **ParentAnchor** object in the Hierarchy window to make it a child of the ParentAnchor object:

![mrlearning-asa](images/mrlearning-asa/tutorial1-section7-step1-2.png)

### 2. Reposition the Rocket Launcher experience

Position, rotate, and scale the **RocketLauncher_Complete** object to a suitable scale and orientation, while also ensuring the **ParentAnchor** object is still exposed, for example:

* Transform **Position** X = 0, Y = 0, Z = 3.75
* Transform **Rotation** X = 0, Y = 90, Z = 0
* Transform **Scale** X = 10, Y = 10, Z = 10

![mrlearning-asa](images/mrlearning-asa/tutorial1-section7-step2-1.png)

In the application, users may now reposition the entire Rocket Launcher experience by moving the cube.

> [!TIP]
> There are a variety of user experience flows for repositioning experiences including the use of a repositioning object (such as the cube used in this tutorial), the use of a button to toggle a bounding box that surrounds the experience, the use of position and rotation gizmos, and more.

## Congratulations

In this tutorial, you learned the fundamentals of Azure Spatial Anchors. The tutorial provided you with several buttons that let you explore the various steps required to start and stop an Azure Spatial Anchors session and create, upload and download Azure Spatial Anchors on a single device.

In the next lesson, you will learn how to save Azure anchor IDs to your HoloLens 2 for retrieval, even after the application is restarted, and how to transfer anchor IDs between multiple devices to achieve spatial alignment.

[Next Lesson: 2. Saving, retrieving and sharing Azure Spatial Anchors](mrlearning-asa-ch2.md)