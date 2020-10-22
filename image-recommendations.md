## Image recommendations for Windows PWA packages

Microsoft [recommends](https://docs.microsoft.com/en-us/windows/uwp/design/style/app-icons-and-logos#:~:text=Here%2C%20you%20can%20upload%203%20image%20sizes%20that,Display%20only%20uploaded%20logo%20images%20in%20the%20Store.) you have about ~50 images for your app, covering start menu tiles, different display scales, and smaller target sizes. Each of these images must be in PNG format.

PWABuilder makes this process easy for you: if you have an image with the right dimensions listed in your web manifest, we'll use that. And if you don't have such an image, we'll generate it for you based on a large square image from your manifest, typically 512x512 as a first choice and 192x192 as a fallback.

Below you'll find each recommended icon, its dimensions, and purpose in Windows. You can [jump down to the summary](https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/image-recommendations.md#summary) to find recommended icons sizes.

#### App icon
<img src="/images/windows-image-app-icon.png" />

Shown in start menu, task bar, task manager

- 44x44
- 55x55 (1.25x scale)
- 66x66 (1.5x scale)
- 88x88 (2x scale)
- 176x176 (4x scale)

#### Small tile
<img src="/images/windows-image-small-tile.png?" />

Shown in the start menu when the user set your app's tile to small size.

- 71x71
- 89x89 (1.25x scale)
- 107x107 (1.5x scale)
- 142x142 (2x scale)
- 284x284 (4x scale)

#### Medium tile
<img src="/images/windows-image-medium-tile.png" />

Shown in the start menu when the user sets your app's tile to medium size.

- 150x150
- 188x188 (1.25x scale)
- 225x225 (1.5x scale)
- 300x300 (2x scale)
- 600x600 (4x scale)

#### Wide tile
<img src="/images/windows-image-wide-tile.png" />

Shown in the start menu when the user sets your app's tile to wide size.

- 310x150
- 388x188 (1.25x scale)
- 465x225 (1.5x scale)
- 620x300 (2x scale)
- 1240x600 (4x scale)

#### Large tile
<img src="/images/windows-image-large-tile.png" />

Shown in the start menu when the user sets your app's tile to large size.

- 310x310
- 388x388 (1.25x scale)
- 465x465 (1.5x scale)
- 620x620 (2x scale)
- 1240x1240 (4x scale)

#### Store logo
<img src="/images/windows-image-store-logo.png" />

Shown in app installer, Windows Partner Center, the "Report an app" option in the Store, and the "Write a review" option in the Store. 

- 50x50
- 63x63 (1.25x scale)
- 75x75 (1.5x scale)
- 100x100 (2x scale)
- 200x200 (4x scale)

#### Splash screen
<img src="/images/windows-image-splash.png" />

Shown as the splash screen for your app. Currently supported only in classic package. In the future, we may add support for the modern hosted app package as well.

- 620x300 
- 775x375 (1.25x scale)
- 930x450 (1.5x scale)
- 1240x600 (2x scale)
- 2480x1200 (4x scale)

#### Target size images

In addition to the standard scale factor sizes described above, we also recommend creating "target-size" assets. We call these assets target-size because they target specific sizes, such as 16 pixels, rather than specific scale factors, such as 400. Target-size assets are for Windows surfaces that don't use the scaling plateau system.

Shown in start jump list, shortcuts, control panel:

<img src="/images/windows-image-target-size.png" />

Recommended sizes:

- 16x16 
- 24x24
- 32x32 
- 48x48 
- 256x256

Optional sizes:

- 20x20
- 30x30
- 36x36
- 40x40
- 60x60
- 64x64
- 72x72
- 80x80
- 96x96

#### Light theme icons

[Windows Light Theme assets](https://docs.microsoft.com/en-us/windows/uwp/app-resources/tailor-resources-lang-scale-contrast#shell-light-theme-and-unplated-resources) are currently unsupported in the PWABuilder Windows platform. Please [open an issue](https://github.com/pwa-builder/pwabuilder/issues) if light theme icon support is important to you.

#### Unplated icons

[Unplated assets](https://docs.microsoft.com/en-us/windows/uwp/design/style/app-icons-and-logos#unplated-assets) are currently unsupported in the PWABuilder Windows platform. Please [open an issue](https://github.com/pwa-builder/pwabuilder/issues) if unplated icon support is important to you.


## Summary

In summary, your PWA can be enhanced on Windows by supplying more images. We recommend choosing one of the options below:

#### Level 1: Basic image support

- 512x512 - base image from which to generate missing images

This is the easiest developer option, but it's also the most basic and won't stand out from other apps on Windows.

Your [web app manifest icons](https://www.w3.org/TR/appmanifest/#icons-member) should  include a square PNG image, ideally 512x512 or larger. It must be a PNG file and [purpose `any`](https://www.w3.org/TR/appmanifest/#purpose-member). PWABuilder will use this image to generate all of the other recommended images for your web app.

#### Level 2: Tiles

- 512x512 - base image from which to generate missing images
- 44x44 - app icon
- 71x71 - small tile
- 150x150 - medium tile
- 350x150 - wide tile
- 310x310 - large tile
- 50x50 - store logo
- 620x300 - splash screen

Your web app manifest contains [tile images](https://docs.microsoft.com/en-us/windows/uwp/design/style/app-icons-and-logos#icon-types-locations-and-scale-factors) for the default (1x) display scale, along with a 512x512 image which PWABuilder will use to generate missing images. Each of the images must be in PNG format and [purpose `any`](https://www.w3.org/TR/appmanifest/#purpose-member).

#### Level 3: Tiles with display scales

- 512x512 - from which to generate missing images
- 44x44 - app icon
- 55x55 - app icon 1.25x display scale
- 66x66 - app icon 1.5x display scale
- 88x88 - app icon 2x display scale
- 176x176 - app icon 4x display scale
- 71x71 - small tile
- 89x89 - small tile 1.25x display scale
- 107x107 - small tile 1.5x display scale
- 142x142 - small tile 2x display scale
- 284x284 - small tile 4x display scale
- 150x150 - medium tile
- 188x188 - medium tile 1.25x display scale
- 225x225 - medium tile 1.5x display scale
- 300x300 - medium tile 2x display scale
- 600x600 - medium tile 4x display scale
- 350x150 - wide tile
- 388x188 - wide tile 1.25x display scale
- 465x225 - wide tile 1.5x display scale
- 620x300 - wide tile 2x display scale
- 1240x600 - wide tile 4x display scale
- 310x310 - large tile
- 388x388 - large tile 1.25x display scale
- 465x465 - large tile 1.5x display scale
- 620x620 - large tile 2x display scale
- 1240x1240 - large tile 4x display scale
- 50x50 - store logo
- 63x63 - store logo 1.25x display scale
- 75x75 - store logo 1.5x display scale
- 100x100 - store logo 2x display scale
- 200x200 - store logo 4x display scale
- 620x300 - splash screen
- 775x375 - splash screen 1.25x display scale
- 930x450 - splash screen 1.5x display scale
- 1240x600 - splash screen 2x display scale
- 2480x1200 - splash screen 4x display scale

For level 3, your web app manifest contains a 512x512 image and tile images for all Windows display scale sizes. 

Display scales are user-configurable in Windows:

<img src="/images/windows-image-display-scales.png" />

Additionally, on Windows devices with high DPI and high resolution displays, Windows may enable a certain display scale by default. For example, on many Microsoft Surface laptops, a display scale of 200% or higher is enabled by default.

Having icons icons for these sizes becomes more important as more devices ship with high density and high resolution displays.

#### Level 4: Tiles, display scales, and target sizes

- 512x512 - from which to generate missing images
- 44x44 - app icon
- 55x55 - app icon 1.25x display scale
- 66x66 - app icon 1.5x display scale
- 88x88 - app icon 2x display scale
- 176x176 - app icon 4x display scale
- 71x71 - small tile
- 89x89 - small tile 1.25x display scale
- 107x107 - small tile 1.5x display scale
- 142x142 - small tile 2x display scale
- 284x284 - small tile 4x display scale
- 150x150 - medium tile
- 188x188 - medium tile 1.25x display scale
- 225x225 - medium tile 1.5x display scale
- 300x300 - medium tile 2x display scale
- 600x600 - medium tile 4x display scale
- 350x150 - wide tile
- 388x188 - wide tile 1.25x display scale
- 465x225 - wide tile 1.5x display scale
- 620x300 - wide tile 2x display scale
- 1240x600 - wide tile 4x display scale
- 310x310 - large tile
- 388x388 - large tile 1.25x display scale
- 465x465 - large tile 1.5x display scale
- 620x620 - large tile 2x display scale
- 1240x1240 - large tile 4x display scale
- 50x50 - store logo
- 63x63 - store logo 1.25x display scale
- 75x75 - store logo 1.5x display scale
- 100x100 - store logo 2x display scale
- 200x200 - store logo 4x display scale
- 620x300 - splash screen
- 775x375 - splash screen 1.25x display scale
- 930x450 - splash screen 1.5x display scale
- 1240x600 - splash screen 2x display scale
- 2480x1200 - splash screen 4x display scale
- 16x16 - OS surfaces like taskbar, start menu, task manager
- 20x20 - OS surfaces like taskbar, start menu, task manager
- 24x24 - OS surfaces like taskbar, start menu, task manager
- 30x30 - OS surfaces like taskbar, start menu, task manager
- 32x32 - OS surfaces like taskbar, start menu, task manager
- 36x36 - OS surfaces like taskbar, start menu, task manager
- 40x40 - OS surfaces like taskbar, start menu, task manager
- 48x48 - OS surfaces like taskbar, start menu, task manager
- 60x60 - OS surfaces like taskbar, start menu, task manager
- 64x64 - OS surfaces like taskbar, start menu, task manager
- 72x72 - OS surfaces like taskbar, start menu, task manager
- 80x80 - OS surfaces like taskbar, start menu, task manager
- 96x96 - OS surfaces like taskbar, start menu, task manager
- 256x256 - OS surfaces like taskbar, start menu, task manager

In level 4, you supply a base 512x512 image, images for tiles with display scales, and target size images for display in various surfaces in Windows, including taskbar, start menu, task manager, ALT+Tab task switcher, and more. 

This provides the best experience for your users, but also requires the most developer effort.