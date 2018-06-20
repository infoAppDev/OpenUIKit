<img src="https://github.com/rizaanlakay/OpenUIKit/blob/master/uilogo.png" width="80">

**Important notice**
We have taken down the current version as we received a DMCA takedown notice from a company that felt we were infringing on their design rights. Please don't leave as we will be uploading version 2 in the upcoming weeks and we feel it will be better than version 1. Includes more Xamarin Forms 3 features, such as Flex Layout, CSS and Layout Compression.

Thank you for your support.

We will be back!

# Open UI Kit

**Version 1.0.0**

This is a cross-platform xaml ui kit for Xamarin Forms, that contains lots of ui templates for you to use in your projects. We have added a number of custom controls and also included a number of controls from other libraries to help users implement good looking user interfaces.

The project is written in Xamarin forms using the [Prism MVVM templates](https://github.com/PrismLibrary/Prism-Samples-Forms) by Brian Lagunas. You could use what ever pattern you would like as this is just XAML UI templates. We are adding documentation for using all of the controls as well as a sample project to see its use. The sample project will also be available in the Google Play store as well as the Apple Store.

**Some of the features included in this UI Kit:**
1. 48 UI Templates
2. Fully Themeable
3. Responsive Layout Helpers
4. Custom Tab Control
5. Custom UI Controls
6. MVVM Ready
7. Animation Support using Lottie

## Using Open UI Kit with an existing project.

**Things to note:**
* The OpenUIKit uses the Prism MVVM framework by Brian Lagunas.
*	Uses Xamarin Forms v3.0.0.550146
*	Android compiled against Android 8.1 SDK

**Steps for adding it to your existing Xamarin Forms project:**
1.	Create a Themes folder in your Xamarin Forms project. (If you don’t already have one.)
2.	Add LightTheme.xaml and DarkTheme files into your Themes folder. (Make sure you add the .xaml and .cs files)
3.	Open the App.xaml file in the CWUILibrary (OpenUIKit) Xamarin Forms project and do the following:
    * Add this to the xaml header: 
        - xmlns:ff="clr-namespace:FFImageLoading.Forms;assembly=FFImageLoading.Forms"
        - xmlns:cust="clr-namespace:CWUILibrary.CustomRenderers;assembly=CWUILibrary"
        - xmlns:local="clr-namespace:CWUILibrary.Themes;assembly=CWUILibrary"
  2.	Copy the entire Resource Dictionary from the CWUILibrary App.xaml file into your App.xaml file.
4.	Add a CustomRenderers folder to your Xamarin Forms project.
5.	Add all the .cs files from the CustomRenderes folder in the CWUILibrary (OpenUIKit) Xamarin Forms project, to your CustomRenderers folder. (Don’t add the CustomActivityIndicator for now as Lottie is breaking.)
6.	Do the same for the Android and iOS projects, also adding the corresponding .cs files from the CWUILibrary.Droid and CWUILibrary.iOS projects. (Including the Effects folder and its contents)
7.	Create a folder called Helpers in your Xamarin Forms project. Add the following files from the Helpers folder in the CWUILibrary project:
-	FontAwesome.cs
-	Ionicicons.cs
-	IToolbarController.cs
-	ShadowEffect.cs
8.	In the Android project add the following files to the Assets folder:
-	Fontawesome.ttf
-	Ionicons.ttf
-	Materialicons.ttf
9.	In the iOS project, in the Resources folder, add the following files:
-	Fontawesome.ttf
-	Ionicons.ttf
-	Materialicons.ttf
10.	Click on your solution file and click the Edit menu then select Find and Replace > Replace in Files. Replace CWUILibrary with YourNameSpace and select Entire Solution. (Uncheck Keep modified files open  after Replace All)                                     
11.	Right-click on the solution file and select Manage Nuget Packages for the Solution. Add the following Nuget Packages:
-	Xamarin.FFImageLoading to (Xamarin Forms, Android and iOS projects)
-	Xamarin.FFImageLoading.Forms to (Xamarin Forms, Android and iOS projects)
-	Xamarin.FFImageLoading.Transformations to (Xamarin Forms, Android and iOS projects)
-	I wouldn’t add Lottie references to your project for now as it’s breaking currently when adding the latest version.
-	Plugin.DeviceOrientation
-	AiForms.Effects
-	AiForms.Layouts
-	CarouselView.FormsPlugin
-	DevsDNA.XFParallax
12.	In the Android project, in the MainActivity.cs file, add the following code before the global::Xamarin.Forms.Forms.Init(this, bundle); in the OnCreate method:
- CrossCurrentActivity.Current.Activity = this;            
- CachedImageRenderer.Init(true);
- CarouselViewRenderer.Init();
13.	In the iOS project in the AppDelegate.cs file. Add the following code before the global::Xamarin.Forms.Forms.Init(); in the FinishedLaunching method: 
- CachedImageRenderer.Init();
- CarouselViewRenderer.Init();
14.	Now you can use any of the views on the Xamarin Forms project and modify as much as you need.

---
## Contributors
- Rizaan Lakay <rizaan@gmail.com>
- Muneem Waggie <m.waggie29@gmail.com>

## License
MIT Licensed.

## Donations
Please feel free to show the developers some love and support by donating some money. They will continue to evolve this project and add more features and templates to help the Xamarin Forms community.

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=4XNV47Z2KTVDL)
