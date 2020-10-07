# Next steps for getting your PWA into the Microsoft Store
You've successfully generated a Microsoft Store app package for your PWA. 😎 

Your next steps:
1. **Test your app**: from a command prompt, run `install.ps1` to install your app on your Windows machine.
2. **Submit your `.msix` to the Microsoft Store**: upload the `.msix` file to the Microsoft Store.
3. **Submit your `.appx` to the Microsoft Store**: upload the `.appx` file to the Microsoft Store so that your app can be installed on older versions of Windows.

Each step is explained below.

## 1. Test your app on your Windows machine

Your zip file contains `install.ps1`. This is a PowerShell script that installs your app and lets you test it before submitting to the Store.

Right-click `install.ps1` and choose `Run with PowerShell`.

> 💁‍♂️ *Heads up*: 
> 
> Get an error saying, *"install.ps1 cannot be loaded because running scripts is disabled on this system"*? To fix this, open PowerShell as Administrator, then enter the command `Set-ExecutionPolicy bypass` Once completed, you'll be able to run `install.ps1`.

The install script will install and launch your PWA app. Once complete, you'll find your app in the Start Menu.

## 2. Submit your `.msix` to the Microsoft Store

Your zip file contains `{app name}.store.msix` file which can be submitted directly to the Microsoft Store through the [Windows Dev Center](https://partner.microsoft.com/dashboard).

This `.msix` file utilizes Microsoft's [Hosted App Model](https://blogs.windows.com/windowsdeveloper/2020/03/19/hosted-app-model/) to install your app as a PWA hosted by Chromium-based Edge, meaning your PWA can utilize modern web technologies.

Once you submit your app, it will be reviewed. Once approved -- typically within 24 hours -- your PWA will be available in the Microsoft Store and accessible to ~1 billion Windows users worldwide. 😎

> 💁🏻‍♀️ *Heads up*: 
> 
> Get an error saying, *"install.ps1 cannot be loaded because running scripts is disabled on this system"*? To fix this, open PowerShell as Administrator, then enter the command `Set-ExecutionPolicy bypass` Once completed, you'll be able to run `install.ps1`.

## 3. Submit your `.appx` to the Microsoft Store (optional)

While this step isn't strictly necessary, skipping it will prevent users on older versions of Windows from installing your app.

Users on newer versions of Windows (v10.0.19041 May 2020 Update) will be able to install the `.msix` you uploaded in step 2. 

To support users on old Windows versions, your zip file contains an `{app name}.legacy.appx` package. While this package doesn't take advantage of the new hosted app model, it runs on older Windows versions by instructing Edge to install your PWA.

> 💁🏾‍♀️ *Heads up*: 
> 
> If you get an error uploading your package to the Dev Center, make sure your [Publisher ID is correct](/find-publisher.md).

## Need more help?

We're here to help. You can [open an issue](https://github.com/pwa-builder/pwabuilder/issues) and we'll help walk you through it.