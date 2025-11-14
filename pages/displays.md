---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Display setup
date: 2025-11-03 09:48:58 -0500
relpath: ../
---

# Display setup
> Before you present, you'll want to make sure that your displays are setup the way you want. Displays represent the devices or outputs where content will be presented.
{: .p-man-page-intro}

To get started, you should confirm that your displays are configured on your system first.  See the following articles for how to setup multiple displays:
- [Windows](https://support.microsoft.com/en-us/windows/how-to-use-multiple-monitors-in-windows-329c6962-5a4d-b481-7baa-bec9671f728a#category=windows_11) - set your display to "Extend"
- [Ubuntu](https://help.ubuntu.com/stable/ubuntu-help/display-dual-monitors.html.en) - set your display to "Join Displays"
- [MacOS](https://support.apple.com/guide/mac-help/connect-an-external-display-mchl7c7ebe08/mac) - set your display to "Extend"

Provided your system is configured properly, display setup in Praisenter is handled from the Present tab on the left navigation.  It's the first place you will see after selecting a workspace.  Here you will be able to add and remove displays, name them, and more.  To get a better understanding of how to setup your displays, consider the following example:

![multi-monitor setup]({{ page.relpath }}assets/img/multi-monitor-setup.png){: .rounded .img-fluid}

In the example above, there are 3 displays (these can be monitors, TVs, projectors, etc.).  The first display is the _controller_ display where your operating system taskbar will be and where the Praisenter application will be.  The other two displays are empty because we have configured our system to _extend_ the desktop onto these displays.  With a setup like this, Praisenter can be configured to send content to the other two displays.

> **NOTE**: It's recommended that you have at least 2 displays.  Praisenter can present content onto any number of displays provided you have them configured properly and have the hardware to support it.  You only need 1 display if you plan to present to [NDI®](https://ndi.video/) only.

> **NOTE**: The configuration above, where the first display is the _controller_ display, is not required.  You could have the _controller_ display in the middle or all the way to the right.  In the next few sections you'll see how to configure the displays in Praisenter.

> **NOTE**: Unlike the example above, the displays do not have to be the same size or resolution.

## Display controllers[#](#display-controllers)
When Praisenter loads the first time, it will detect the number of displays and try to determine a basic setup.  Praisenter is looking for at least one display that's not the _controller_ display to use as the primary display for presenting.  For example, in the screenshot below, Praisenter detected 3 displays.  Because one of those displays (display 1) has the taskbar on it, and it detected more than one display, it designated Display 1 the _controller_ display and _hid_ it.  Since displays 2 & 3 are available, Praisenter chooses the next one in order of display number (display 2) as the _primary_ display and shows a _display controller_ for it.

> The _controller_ display is the display where the Praisenter application and other applications will be used and content will _not_ be presented there.  Think of this as your desktop from where you will control all other displays.

The _display controller_ is the set of buttons, options, and features that allow you to _control_ the display it's bound to.  In the top left corner of the display controller, you can see the name that was assigned to the display: `# ID=2 (-1920,0) 1920x1080`.  The default naming is as follows:

- `ID=2` - The _display controller_ is controlling the second display
- `(-1920,0)` - The display is positioned at `x` = `-1920` and `y` = `0`
- `1920x1080` - The display has resolution of `width` = `1920` and `height` = `1080`

There's a lot features on the display controller, but don't get too overwhelmed, we'll be covering all of it in the [Presenting]({{ page.relpath }}pages/presenting.html) section of the manual.  For now, let's focs on adding, hiding, renaming, and other display management features.

> **NOTE**: Praisenter monitors your systems' display configuration and will react to changes.  When it reacts, it will clear anything being presented on that display.

> **NOTE**: Make sure your system is configured correctly for multiple displays.

> **NOTE**: You can override the Praisenter detected displays and configure them manually.  We'll go through that process in the next few topics.

![presentation controller]({{ page.relpath }}assets/img/present-controller.png){: .rounded .img-fluid}

## Adding displays[#](#adding-displays)
As described above, Praisenter tries to figure out what displays should be used and creates _one display controller_ for what it decides is the _primary_ display.  If you have more displays that you want to present to, no problem, you can add displays using the `Add Display` button in the top right corner of the presentation area.  You can also change which display is the primary.

Using the example above, we have the option to add screens and [NDI®](https://ndi.video/) outputs.  For now, let's only focus on screen management.  A screen is really any type of display: a monitor, TV, projector, and so on.  In this example, Praisenter detected 2 other screens (so 3 three screens in total).  As described above, it designated display 1 as the _controller_ screen and display 2 as the _primary_.  We have the option to add both display 1 and display 3 if we don't like what Praisenter defaulted to.  Your changes will automatically be saved when you close Praisenter.

> **NOTE**: Because we already have a _display controller_ for display 2, it's not available to _add_.

To add a display, just click the display you want to add - in this case, we'll click display 3.  A new _display controller_ has now appeared with the name `# ID=3 (1920,0) 1920x1080`.  In the screenshot below, you can see there are now two _display controllers_, one for display 2 and one for display 3.  We can now control the displays independently, showing different content on each.  This is nice if you have a display for a minister and a different display for the congregation.

> **NOTE**: You can _link_ displays if you want the same content to go to different displays.  You can accomplish the same goal by configuring your system (not Praisenter) to have some displays mirrored or by taking one video output cable and splitting it to go to multiple displays.

> **NOTE**: Once you have multiple displays, you'll probably want to maximize the Praisenter window to avoid having to scroll left and right. Having an ultra-wide _controller_ display can be super useful when you are trying to control more than one display.

Now that we've added display 3, the `Add Display` button only shows display 0 (the _controller_ display).  As mentioned earlier, you can control as many displays as your system can handle.

![presentation controller - 2 displays]({{ page.relpath }}assets/img/present-controller-changed.png){: .rounded .img-fluid}

## Identifying a display[#](#identifying-a-display)
Now that you have a basic understanding of displays and how Praisenter detects and uses them, you probably have a burning question - How do I know which display is which?  This is a great question with an easy answer.  For each display you add, you can use the `Identify` feature in the `Actions` button to identify it.  Using this option will show the display number on the display for a few seconds.  

> **NOTE**: To identify all displays, you need to add them and identify each one. 

> **NOTE**: Praisenter will warn you and ask you a second time if you are sure before showing the number on the screen.

![presentation controller identify display]({{ page.relpath }}assets/img/present-controller-identify.png){: .rounded .img-fluid}

## Naming a display[#](#naming-a-display)
Praisenter applies a default naming to all detected displays.  The pattern is `# ID=n (x,y) wxh` where `n` is the display number, `x` is the position of the display on the x-axis, `y` is the position of the display on the y-axis, `w` is the width of the display, and `h` is the height of the display.  An example of a default name is  `# ID=2 (-1920,0) 1920x1080`.

While this naming can help with setting up or identifying displays, it's not as useful once you've completed that process. To help with this, Praisenter allows you to `Rename` the displays to better identify them going forward.  For example, imagine I have 3 displays, the _controller_ computer monitor, a projector that displays to the church, and a small TV on the stage.  I could rename the projector to something like "Main" and the TV to "Stage" to better identify which display you are presenting to.

> **NOTE**: You can rename a display at any time.

![presentation controller rename display]({{ page.relpath }}assets/img/present-controller-rename.png){: .rounded .img-fluid}

![presentation controller rename display]({{ page.relpath }}assets/img/present-controller-renamed.png){: .rounded .img-fluid}

## Primary display[#](#primary-display)
The _primary_ display represents the display that you present to most often.  Designating a display at the _primary_ allows Praisenter to choose the correct default width and height for slides.  If your slides are built with the correct width and height, Praisenter doesn't have to adjust them to the display size.  If the slides are built against a different width and height, Praisenter performs a adjustment called _fitting_ to the slide before presenting the slide.

Fitting is the process of adjusting a slide width and height to the display width and height.  Praisenter tries to fit the slides in the least destructive way, but things like font sizes can cause things to change if the difference in height/width are large.  The good thing is that you can set the slide width and height when you creating it as well to make 100% sure it's a perfect fit for the desired display.

## Hiding a display[#](#hiding-a-display)
In addition to adding displays, you can also _hide_ them.  Hiding means you don't want to present anything on that display.  This is useful if Praisenter detected the wrong display to use or if you are swapping, adding, or removing displays.  Hiding a display does NOT remove it permanently - you can always add it back as described above.

To hide a display, use the `Hide` option under the `Actions` menu.

> **NOTE**: When you hide a display, anything currently presenting on the display will be cleared.

![presentation controller hide display]({{ page.relpath }}assets/img/present-controller-hide.png){: .rounded .img-fluid}

## Linking displays[#](#linking-displays)
Praisenter creates a _display controller_ for every display you choose to present to.  This allows you to control the displays independently - you could have a Bible verse showing on one display and a Song on another display.  That flexiblity is great, but can be difficult to manage if you want two displays to show the _same_ content.  This is where display _linking_ comes in.  To link to displays use the `Actions` -> `Link` option.

![presentation controller link display]({{ page.relpath }}assets/img/present-controller-link.png){: .rounded .img-fluid}

Linking one display to another allows you to update the content on both displays with _one_ display controller.  You link the displays from the display controller you want to use.  For example, in the example below, I'm linking display 2 to display 3.  Display 3 now shows that it's being _controlled_ by display 2.

> **NOTE**: You can unlink the displays by performing the same steps.

![presentation controller linked displays]({{ page.relpath }}assets/img/present-controller-linked.png){: .rounded .img-fluid}

Even if you have displays linked, you still have the option to send different content to the displays.  When you linked, you'll notice that the display controller for the linked display is still visible and enabled.  This allows you to send content from one display controller to both displays, then replace the content on the linked display only.  For example, if you have `display A` controlling `display B`, when you send a slide from `display A`'s controller, it will present on both `display A` and `display B`.  Now if you send a slide from `display B`'s controller, it will _only_ go to `display B` and replace the previous content sent from `display A`.  If you send another slide from `display A` after this, it will again send to both `display A` and `display B` and replace the content on both displays.

Some things to keep in mind when linking displays:
- You _can_ have one display link to multiple displays - For example, a configuration like `display A` controls both `display B` and `display C` _IS_ possible.
- You _can't_ build a hierarchy of links - For example, a configuration like `display A` controls `display B` which controls `display C` _IS NOT_ possible
- You _can't_ control a display from multiple displays - For example, a configuration like `display A` controls `display B` AND `display C` controls `display B` _IS NOT_ possible.

## Adding an NDI® display[#](#adding-an-ndi-display)
[NDI®](https://ndi.video/) stands for Network Device Interface, a software standard for transmitting video and audio over an IP network. This is especially useful for sending content to another application like [OBS](https://obsproject.com/) to combine, overlay, merge, etc. different content into a single or multiple displays.  Praisenter allows you to create NDI® displays and have content sent there.  To create an NDI® display, use the `Add display` button and choose the `Create a new NDI® display`.

![presentation add NDI® display]({{ page.relpath }}assets/img/present-add-ndi-display.png){: .rounded .img-fluid}

When adding an NDI® display, you must specify a few options:
- `NDI® Source Name` - This will be used by other programs to find your display and connect to it.
- `FPS` - The number of frames per second to send to the NDI® display from Praisenter.
- `Size` - The desired width and height for the display.

> **NOTE**: Each NDI® display should have a unique name on the network.

> **NOTE** - The `FPS` option can have a large impact on system performance.  In most cases 24 FPS is the lowest you can go for smooth output.  Praisenter will attempt to improve performance when the presenting content is not animating (slide transitions or video).

![presentation add NDI® display options]({{ page.relpath }}assets/img/present-add-ndi-display-options.png){: .rounded .img-fluid}

NDI® displays can be linked and hidden just like physical displays, but they can also be deleted.  Deleting an NDI® display will clear the content and remove the display from the network.
