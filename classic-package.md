## What is a classic package?

PWABuilder Windows platform generates 2 versions of your app: 

- Modern package that works on newer versions of Windows.
- Classic package that works on older versions of Windows, with fewer bells and whistles.

In particular, the modern package, `{app name}.msixbundle`, uses the [Hosted App Model](https://blogs.windows.com/windowsdeveloper/2020/03/19/hosted-app-model/) to install your PWA as a Windows app hosted by Edge. This app works only on Windows version 10.0.19041, May 2020 Update and newer. 

Meanwhile, the classic package, `{app name}.classic.appxbundle`, runs on older versions of Windows, versions prior to 10.0.19041, May 2020 Update. This version still uses the new Edge, but it doesn't rely on the Hosted App Model. Instead, it uses a bootstrapper app which instructs Edge to install the PWA on your behalf. The classic package doesn't include some nice-to-haves, such as [different app icons](/image-recommendations.md) for start menu, task bar, etc.

When you submit your app to the Microsoft Store, you'll upload both versions of the app. Users will be offered to download whichever version their OS can support.