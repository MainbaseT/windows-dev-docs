If you encounter errors after submitting your app to the Store, you must resolve them in order to continue the [certification process](../../../apps/publish/publish-your-app/app-certification-process.md). The error message will indicate what the problem is and what you might need to do in order to fix the issue. Here is some additional info that can help you resolve these errors.

## UWP apps

If you are submitting a UWP app, you may see an error during preprocessing if your package file is not a .msixupload or .appxupload file generated by Visual Studio for the Store. Be sure that you follow the steps in [Package a UWP app with Visual Studio](/windows/msix/package/packaging-uwp-apps) when creating your app's package file, and only upload the .msixupload or .appxupload file on the [Packages](../../../apps/publish/publish-your-app/upload-app-packages.md) page of the submission, not a .msix/appx or .msixbundle/appxbundle.

If a compilation error is displayed, make sure that you are able to build your application in Release mode successfully. For more info, see [.NET Native Internal Compiler Errors](https://github.com/dotnet/core/blob/master/Documentation/ilcRepro.md).

## Desktop application

If you plan to submit a package that contains both Win32 and UWP binaries, make sure that you create that package by using the Windows Packaging Project that is available in Visual Studio 2017 Update 4 and later versions. If you create the package by using a UWP project template, you might not be able to submit that package to the Store or sideload it onto other PCs. Even if the package publishes successfully, it might behave in unexpected ways on the user's PC. For more info, see [Package an app by using Visual Studio (Desktop Bridge)](/windows/msix/desktop/desktop-to-uwp-packaging-dot-net).

## Name/identity errors

If you see an error that says **The name found in the package is not one of your reserved app names. Please reserve the app name and/or update your package with the correct app name for this language**, it may be because you’ve entered an incorrect name in your package. This error can also occur if you are using an app name that you haven’t reserved in Partner Center. You can usually resolve this error by following these steps:

- Go to the [Product identity](../../../apps/publish/view-app-identity-details.md) page for your app (under **Product management**) to confirm whether your app has an assigned Identity. If it doesn’t, you’ll see an option to create one. You’ll need to reserve a name for your app in order to create the Identity. Make sure this is the name you’ve used in your package.
- If your app already has an identity, you might still need to reserve the name that you want to use in your package. Under **Product management**, click [Manage app name reservations](../../../apps/publish/partner-center/manage-app-name-reservations.md). Enter the name you’d like to use, and click **Reserve app name**.

> [!IMPORTANT]
> If the name you want to use is not available, another app might have already reserved that name. If your app is already published under that name, or if you think you have the right to use it, [contact support](https://go.microsoft.com/fwlink/?linkid=2224235).  
