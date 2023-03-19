>  Introduction to the Mixed Reality Toolkit & Setting up your Unity Project and Hand Interaction

# **1) Required Software**
1. 	**Unity Hub**: This application used to manage and download different versions of the Unity Editor (preferred latest version).
         https://store.unity.com/download
2.	**Unity Editor**: This is the main software used to develop Unity projects. In this tutorial version 2021.2.2f1 is used.(latest version will work fine).
3.	**Visual Studio**: This is the recommended code editor for Unity projects. In this tutorial  Visual Studio 2019 is used, (latest version will work fine).
        https://visualstudio.microsoft.com/vs/community/
4.	**Windows 10 SDK**: It is required for developing _**Universal Windows Platform**_ (UWP) apps, which includes MR applications for the HoloLens as well.
        https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/
5.	**Microsoft Mixed Reality Toolkit**: This is an open-source Toolkit that provides a collection of components and tools for developing MR applications, including HoloLens.
        https://www.microsoft.com/en-us/download/details.aspx?id=102778
6.	**Microsoft HoloLens emulator**:_(Optional)_ This emulator lets you run application on a HoloLens virtual machine without a physical HoloLens.
        https://learn.microsoft.com/en-us/windows/mixed-reality/develop/advanced-concepts/hololens-emulator-archive.

***

#  2) Step-by-Step Software Configuration Instructions!
## 1) UNITY HUB SETUP

* 	To Install the Tools required for XR development == **Unity 2021** 
* 	 Download Unity Hub and Unity — highly recommend the latest version of Unity and unity hub (in Tutorial 2021.2.7f1 and 3.0 respectively)
* 	 Click the **gear icon** -> **Add modules**


![Picture1](https://user-images.githubusercontent.com/120566924/217715271-a8521da1-23be-42d4-9a1a-531f67503126.png)


* 	All available and installed modules will be displayed  in that window, select **Universal Windows Platform Build Support** _[**REQUIRED** for HoloLens 2]_ 

![Picture2](https://user-images.githubusercontent.com/120566924/217717946-4cae2829-8b44-482b-8fa5-641492d825e0.png)
 

***
## 2) VISUAL STUDIO SETUP
* 	Run **Visual Studio Installer** -> click **Modify**

![Picture3](https://user-images.githubusercontent.com/120566924/217720179-257942ef-3cec-4b0f-ba4e-c2deca8fc6db.png)

* Required Modifications:-
     *  Desktop development with C++ 
     *  Universal Windows Platform development 
     *  Game development with Unity
     *  On the right hand side, make sure to check **USB Device Connectivity**

![Picture4](https://user-images.githubusercontent.com/120566924/217721932-1f878366-695c-4ce7-a4ba-dfee39c1e552.png)

* 	The **lasted version** Windows SDK  is **required** (currently 10.0.22000)
	https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/
* 	_I installed everything here, but you could potentially uncheck some of the options_

![Picture5](https://user-images.githubusercontent.com/120566924/217722607-703f694f-7187-424a-9df9-4d6e1d00d576.png)

***

# 3) XR Step-by-Step!
###  _Setting up HoloLens 2 Project in Unity 2021 + MRTK 2.7 + Visual Studio 2022_

## 1.  HOLOLENS 2 BUILD SETUP
* Click** New Project** -> 3D template -> name your project -> Click **Create Project**
![Picture6](https://user-images.githubusercontent.com/120566924/217725836-19338bf3-1281-4676-8470-19e4f00adcbc.png)

* (Toolbar) File -> **Build Settings**:-
     *  Add Open Scenes
     *  Switch Platform to Universal Windows Platform
     *  Architecture -> ARM 64-bit
     *  Minimum required Platform Version -> 10.0.18362.0 (or higher) — if you don’t see this version, then you need to update your Windows SDK 
	
![Picture7](https://user-images.githubusercontent.com/120566924/217726616-31bef876-54f7-43c6-898e-ca98614c636e.png)

***

### * Microsoft Mixed Reality Feature Tool
* 	 Unzip and open your **Mixed Reality Feature Tool** folder
* 	Click on the MixedRealityFeatureTool.exe
![Picture8](https://user-images.githubusercontent.com/120566924/217732600-ee68ba9d-efaf-4035-9d7e-40dcd9e6bd1c.png)

***

* Click Start

![Picture9](https://user-images.githubusercontent.com/120566924/217732852-3f4313d0-78a4-4f20-9477-98f6cab7ffb7.png)

***


* 	Set path of the Unity project -> Click Discover Features
![Picture10](https://user-images.githubusercontent.com/120566924/217733084-eb479187-2222-42c9-8c31-11b4d7a3fee9.png)

***


* **(Mixed Reality Feature Tool) Expand Platform Support** -> Check **Mixed Reality OpenXR Plugin** -> Click **Get Features**
![Picture11](https://user-images.githubusercontent.com/120566924/217734404-d6dc8bae-e7bf-47b7-b8be-5a98f7f99be0.png)

***


*  Click **Import**
![Picture12](https://user-images.githubusercontent.com/120566924/217734539-1608dbc1-9fb2-44ac-8a99-53ad5d3889a0.png)

***


* Click **Approve**
![Picture13](https://user-images.githubusercontent.com/120566924/217734725-9194593a-07d9-43c8-97e0-c1061b7b3414.png)

***

*Click **Exit**
![Picture14](https://user-images.githubusercontent.com/120566924/217734879-5f83d06f-44bb-4ff4-aa19-774993743c7f.png)

***

### * MIXED REALITY OPEN-XR PLUGIN

* 	Switch back to your Unity project – you will see that it’s importing the **Mixed Reality OpenXR Plugin**
![Picture15](https://user-images.githubusercontent.com/120566924/217735594-fe3df12b-8234-4e50-beef-fe19490d3b06.png)

***

* 	Click **Yes** to use the new input system, and **Unity** will restart

![Picture17](https://user-images.githubusercontent.com/120566924/217736037-363217a4-3943-485c-9d25-a75eb5b6a273.png)

***

* (Toolbar) Edit -> Project Settings:-
     * (**Project Settings**) Select **XR Plug-in Management** -> Click on the **UWP Settings** tab
     * (**UWP Settings**) Check **OpenXR** -> Check **Microsoft HoloLens feature group**
     * (**UWP Settings**) Next to **OpenXR** -> Click the **Warning Icon**

![Picture18](https://user-images.githubusercontent.com/120566924/217741792-c941f483-4c5b-40bd-9007-52aa05c5abf0.png)

***
     
* 	(**OpenXR Project Validation**) Click **Fix All**
* 	(**OpenXR Project Validation**) If you’re left with **“At least one interaction profile must be added.”** -> Click on Edit

![Picture19](https://user-images.githubusercontent.com/120566924/217743527-d9f07bbe-ec09-4489-8b81-1fd52a7d3f29.png)

***

* (**Project Settings**) OpenXR -> Interaction Profiles -> Click “+“:-
     * Add **Eye Gaze Interaction Profile**
     * Add **Microsoft Hand Interaction Profile**
     
![Picture21](https://user-images.githubusercontent.com/120566924/217743970-9a4be8de-9b52-46c7-8860-a8472546534c.png)

***

*   (**Project Settings**) Next to **Eye Gaze Interaction Profile**-> Click the **Warning Icon**

![Picture22](https://user-images.githubusercontent.com/120566924/217744399-1693674b-fe08-4fc8-bd73-451acc898787.png)

***

*  (**OpenXR Project Validation**) Click **Fix All**

![Picture23](https://user-images.githubusercontent.com/120566924/217744609-d36e9388-f98b-47f5-b443-f8fc34b2da4b.png)

***

* (**Windows Settings**) Check **OpenXR** -> Check **Microsoft HoloLens feature group**

![Picture24](https://user-images.githubusercontent.com/120566924/217744892-06917d0d-b9c8-46ca-8dba-36e003d2fedc.png)

***

* **(Toolbar) Mixed Reality -> Project -> Apply recommended project settings for HoloLens 2**

![Picture25](https://user-images.githubusercontent.com/120566924/217745083-73373be0-6ab4-40b7-a05d-343eafd38805.png)

***

* (Project)Assets -> Drag the unity packages into the Project window one at a time:-
     * [**Required**] Microsoft.MixedReality.Toolkit.Unity.Foundation.2.7.2.unitypackage
     * [**Recommended**] Microsoft.MixedReality.Toolkit.Unity.Tools.2.7.2.unitypackage
	
![Picture26](https://user-images.githubusercontent.com/120566924/217745546-8065ce32-192c-44a2-b20e-93b4f7ebe6a2.png)

***

*  (**Import Unity Package**) Click **Import**

![Picture27](https://user-images.githubusercontent.com/120566924/217745723-82585c6a-02cc-4f7a-a383-6db0167a5964.png)

* 	Once you’ve installed **MRTK** unity packages, switch back to Unity- it should bring up the **MRTK** Project Configurator
* 	(**MRTK Project Configurator**) Click Apply Settings -> Next
![Picture28](https://user-images.githubusercontent.com/120566924/217746148-a9049e3c-ce7f-4b15-894b-84c241d89d6e.png)

***

* (**MRTK Project Configurator**) Click **Apply**
![Picture29](https://user-images.githubusercontent.com/120566924/217746645-2014a10f-f47a-4010-9655-fce68d6aec3d.png)

***

* (**MRTK Project Configurato**r) Click **Apply** _[Unity will restart]_
![Picture30](https://user-images.githubusercontent.com/120566924/217746960-16d03403-619f-49e3-b9b1-6b97251933a5.png)

***

* _[Bonus Content] We officially configured your project! , Now let’s configure your scene!_
* (**Hierarchy**) Select your scene -> (**Toolbar**) Mixed Reality -> Toolkit -> Add to Scene and Configure****
![Picture31](https://user-images.githubusercontent.com/120566924/217747440-a544c81b-781b-4a46-a04b-8af1a01d32ad.png)

***

* You’ll now see the following in your scene!
![Picture32](https://user-images.githubusercontent.com/120566924/217747583-6044406e-bcde-44ba-9c2e-020c7fac4d13.png)

***

* (**Hierarchy**) Expand **MixedRealityPlayspace** -> **Main Camera -> (Inspector) Camera** -> Change **Background** to **Solid Color** -> Set to black
![Picture34](https://user-images.githubusercontent.com/120566924/217747893-7441972d-cff7-402c-a080-16ff7e287701.png)

***

* 	Let’s add a **3D cube** so we have something to look at…
* 	(**Hierarchy**) Right click ->** 3D Object** -> **Cube**

![Picture35](https://user-images.githubusercontent.com/120566924/217748186-f0c2eb46-e8a7-4f9c-940d-5057c2006d2b.png)

***

* (**Hierarchy**) Select **Cube **-> (**Inspector**) Set the Transform of the cube as shown below

![Picture36](https://user-images.githubusercontent.com/120566924/217748415-6e7bc5bc-8eae-49d5-b9a4-417f81a54173.png)

***

* (**Toolbar**) File -> Build Settings… -> Build
* Create a directory _[I generally create a folder named Install]_

![Picture37](https://user-images.githubusercontent.com/120566924/217748656-acb7603f-fa62-4602-927d-3ecad39c9f5a.png)

***

* (**Windows Explorer**) Click on the ***.sln file** in your **Install** folder _(assuming that’s what you named it)_

![Picture38](https://user-images.githubusercontent.com/120566924/217749005-6ba6a819-23be-43bd-934a-63905dbab9e8.png)

***

*  (**Visual Studio**) Change to **Release** -> Change to **ARM64 **-> Change to **Device **-> Click on **Device** to deploy _(make sure to have your HoloLens 2 connected to your computer)_

![Picture39](https://user-images.githubusercontent.com/120566924/217749409-3f34f3ff-de9f-4abd-abe1-3ee68d6b214d.png)

***

* Look at that! we have a **HoloCube** in Mixed Reality 

![Picture40](https://user-images.githubusercontent.com/120566924/217749681-384238bb-aeca-499e-8978-00fa86466274.gif)

***



#   
***
