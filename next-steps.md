# Next steps for getting your PWA into the Microsoft Store
You've successfully generated a Microsoft Store app package for your PWA. 😎 

Your next steps:
1. **Test your app**: run `install.ps1` to install your app on your Windows machine.
2. **Submit your app packages to the Microsoft Store**: upload the `.appxbundle` and `.msixbundle` files to the Microsoft Store.

Each step is explained below.

## 1. Test your app on your Windows machine

Your zip file contains `install.ps1`. This is a PowerShell script that installs your app and lets you test it before submitting to the Store.

Right-click `install.ps1` and choose `Run with PowerShell`.

> 💁‍♂️ *Heads up*: 
> 
> If you get an error saying, *"install.ps1 cannot be loaded because running scripts is disabled on this system"*, you can fix this by opening PowerShell as Administrator, then entering the command `Set-ExecutionPolicy bypass` Once completed, you'll be able to run `install.ps1`.

The install script will install and launch your PWA app. Once complete, you'll find your app in the Start Menu.

## 2. Submit your app packages to the Microsoft Store

Your zip file contains `{app name}.msixbundle` file, the main app package. It also includes a `.{app name}.classic.appxbundle` package that allows users on older versions of Windows (below 10.0.19041, May 2020 Update) to run your app.

Both packages can be submitted directly to the Microsoft Store through the [Windows Partner Center](https://partner.microsoft.com/dashboard)

When you're ready to publish to the Store, you can either
- [Publish a new app in the Store](/publish-new-app.md) 
- [Update an existing app in the Store](/update-existing-app.md)

Once you submit your app, it will be reviewed. Once approved -- typically within 24 hours -- your PWA will be available in the Microsoft Store and accessible to ~1 billion Windows users worldwide. 😎

## Need more help?

We're here to help. You can [open an issue](https://github.com/pwa-builder/pwabuilder/issues) and we'll help walk you through it.