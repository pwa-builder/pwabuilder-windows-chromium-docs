## Image recommendations for Windows PWA packages

Microsoft [recommends](https://docs.microsoft.com/en-us/windows/uwp/design/style/app-icons-and-logos#:~:text=Here%2C%20you%20can%20upload%203%20image%20sizes%20that,Display%20only%20uploaded%20logo%20images%20in%20the%20Store.) you have a 12 images, plus 4 scaled versions (1.25x, 1.5x, 2x, 4x) of each image for different display scale factors.

PWABuilder makes this process easier for you: if you have an image with the right dimensions listed in your web manifest, we'll use that. And if you don't have such an image, we'll generate it for you based on a large square image from your manifest, typically 512x512 as a first choice and 192x192 as a fallback.

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

- 44x44
- 55x55 (1.25x scale)
- 66x66 (1.5x scale)
- 88x88 (2x scale)
- 176x176 (4x scale)

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

Shown as the splash screen for your app. Currently supported only only in classic package. In the future, we may add support for the modern hosted app package as well.

- 620x300 
- 775x375 (1.25x scale)
- 930x450 (1.5x scale)
- 1240x600 (2x scale)
- 2480x1200 (4x scale)

#### Target size images

In addition to the standard scale factor sizes described above, we also recommend creating "target-size" assets. We call these assets target-size because they target specific sizes, such as 16 pixels, rather than specific scale factors, such as 400. Target-size assets are for Windows surfaces that don't use the scaling plateau system.

<img src="/images/windows-image-target-size.png" />

Shown in start jump list, shortcuts, control panel.

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