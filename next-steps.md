# Next steps for getting your PWA into the Microsoft Store
You've successfully generated a Microsoft Store app package for your PWA. 😎 

Your next steps:
1. **Test your app**: from a command prompt, run `install.ps1` to install your app on your Windows machine.
2. **Submit your `.msixbundle` to the Microsoft Store**: upload the `.msixbundle` file to the Microsoft Store.
3. **Submit your `.appxbundle` to the Microsoft Store**: upload the `.appxbundle` file to the Microsoft Store so that your app can be installed on older versions of Windows.

Each step is explained below.

## 1. Test your app on your Windows machine

Your zip file contains `install.ps1`. This is a PowerShell script that installs your app and lets you test it before submitting to the Store.

Right-click `install.ps1` and choose `Run with PowerShell`.

> 💁‍♂️ *Heads up*: 
> 
> If you get an error saying, *"install.ps1 cannot be loaded because running scripts is disabled on this system"*, you can fix this by opening PowerShell as Administrator, then entering the command `Set-ExecutionPolicy bypass` Once completed, you'll be able to run `install.ps1`.

The install script will install and launch your PWA app. Once complete, you'll find your app in the Start Menu.

## 2. Submit your `.msixbundle` to the Microsoft Store

Your zip file contains `{app name}.store.msixbundle` file which can be submitted directly to the Microsoft Store through the [Windows Dev Center](https://partner.microsoft.com/dashboard).

This `.msixbundle` file utilizes Microsoft's [Hosted App Model](https://blogs.windows.com/windowsdeveloper/2020/03/19/hosted-app-model/) to install your app as a PWA hosted by Chromium-based Edge, meaning your PWA can utilize modern web technologies.

Once you submit your app, it will be reviewed. Once approved -- typically within 24 hours -- your PWA will be available in the Microsoft Store and accessible to ~1 billion Windows users worldwide. 😎

> 💁🏾‍♀️ *Heads up*: 
> 
> If you get an error uploading your package to the Dev Center, make sure your [Publisher ID is correct](/find-publisher.md).

## 3. Submit your `.appxbundle` to the Microsoft Store (optional)

While this step isn't strictly necessary, skipping it will prevent users on older versions of Windows from installing your app.

To support users on old Windows versions, your zip file contains an `{app name}.classic.appxbundle` package. While this package doesn't take advantage of the new hosted app model, it runs on older Windows versions by instructing Edge to install your PWA.

You should upload this package as a additional version of your app. Same app, different versions. The Store will offer whichever supported version they can run: if the user is on a newer version of Windows, they'll be offerred main package,the `.msixbundle` you uploaded in step 2. If they're on an older version of Windows, they'll be offerred this classic package, the `.appxbundle`.

> 💁🏻‍♂️ *Heads up*: 
> 
> Your classic app package has a lower version than the main app package. So if you packaged your PWA as version 2.0, the classic app package will be version 1.9. This way you can submit both packages as a single app.

## Need more help?

We're here to help. You can [open an issue](https://github.com/pwa-builder/pwabuilder/issues) and we'll help walk you through it.