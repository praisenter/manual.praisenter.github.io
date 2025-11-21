# Quick start
> Welcome to the quick start guide!  Here we'll walk through the sets to get up and running quickly.  Links to other spots in the manual will be provided for more detailed information.
{: .p-man-page-intro}

After following this guide you should have Praisenter installed, displays configured, bible imported, and have presented a slide.  There's so much more you can do with Praisenter so be sure to try different things!

## 1. System configuration[#](#qs-configure-system)
{: #qs-configure-system}
Before you start Praisenter, you should make sure that your displays are configured properly on your system.  Make sure that you have all your devices connected (monitors, projectors, TVs, and so on) to your computer and set to `Extend` the desktop.  For more details, see the [display setup]({{ page.relpath }}{{ page.displays_page }}#display-setup) part of the manual.

Once you have your dislays connected and you can drag apps to each one, then continue to the next step.

> **NOTE**: You don't have to _have_ your system setup before launching Praisenter.  Praisenter will automatically detect when displays are changed, added, or removed.  However, having a complete setup _before_ starting Praisenter allows Praisenter to _auto-configure_ the displays and makes the quick start faster.

## 2. Install Praisenter[#](#install)
{: #qs-install}
To install Praisenter you have two options: Download from the store (don't worry it's free) or install manually (also called side-loading).  The recommended way is to download from the store.

> **NOTE**: Praisenter is released on the Microsoft Store and Snap Store, but don't worry, it's free.

For **Windows**:

<a href="https://apps.microsoft.com/detail/Praisenter/9PHHWB94W800?launch=true&amp;mode=mini">
    <img src="{{ page.relpath }}assets/img/windows-download-icon.svg" width="200">
</a>

For **Ubuntu**:

<a href="https://snapcraft.io/praisenter">
    <img alt="Get it from the Snap Store" src="{{ page.relpath }}assets/img/ubuntu-download-icon.svg" height="59">
</a>

You can manually download Praisenter as an `MSI` or `DEB` from the [project page](https://github.com/praisenter/praisenter/releases).  Installing manually is a lot more work.  If you need help, see [this article](https://praisenter.org/install).

> **NOTE**: Praisenter doesn't have a MacOS build at this time.  That said, if you are adventurous, you could clone the [repo](https://github.com/praisenter/praisenter) and build the project on MacOS.  Providing a MacOS build is on the roadmap, but there a few hurdles to overcome to get there.

Once you've completed the install, start Praisenter and continue.

## 3. Create a workspace[#](#qs-create-workspace)
{: #qs-create-workspace}
Everytime you start Praisenter you will be prompted to [create a workspace]({{ page.relpath }}{{ page.workspaces_page }}#creating-workspaces).  A workspace is just a folder on your computer that Praisenter will use to store all it's settings, Bibles, song lyrics, videos, and so on.  You can have many workspaces on one computer and [switch between them]({{ page.relpath }}{{ page.workspaces_page }}#switching-workspaces).

You must select a workspace to continue, so create a new folder and click `Launch`.

![workspace selection]({{ page.relpath }}assets/img/workspace-selection.png){: .rounded .img-fluid}

## 4. Setup displays[#](#qs-setup-displays)
{: #qs-setup-displays}
After selecting a workspace, the first screen you will see is the [Present tab]({{ page.relpath }}{{ page.present_page }}#present).  From here you can control all configured displays.  Each display is assigned a [_display controller_]({{ page.relpath }}{{ page.displays_page }}#display-controllers) that you will use to control them independently.  In the example below, Praisenter detected 3 displays and automatically created a _display controller_ for display #2.  If you aren't sure which display is which, use the [identify displays]({{ page.relpath }}{{ page.displays_page }}#identifying-a-display) feature.

You should have at least one display controller by default (Praisenter chooses one for you if it can).  If you want to [add more]({{ page.relpath }}{{ page.displays_page }}#adding-displays), you can do that now.

Once you have at least one display controller ready, move on to the next step.

![display controller example]({{ page.relpath }}assets/img/present-controller.png){: .rounded .img-fluid}

## 5. Import a Bible[#](#qs-download-bible)
{: #qs-import-bible}
Our next task is to download a Bible from one of the [supported sources]({{ page.relpath }}{{ page.bibles_page }}#bibles) and [import]({{ page.relpath }}{{ page.library_page }}#importing-content) it.  You can download as many as you need and import them all at once.  The quickest way is to use the `Help` menu and download an [Unbound Bible](https://github.com/praisenter/unbound-bible-archive).

![Bible download links]({{ page.relpath }}assets/img/misc-help.png){: .rounded .img-fluid}

After downloading, [drag and drop]({{ page.relpath }}{{ page.library_page }}#importing-content) the files onto the Praisenter window.  You can also use the `File` -> `Import` menu.  After importing, continue to the next step.

> **NOTE**: You can skip this step if you aren't using Praisenter to display Bible verses.

> **NOTE**: Can't find the version or translation you are looking for?  Use the [Bible editor]({{ page.relpath }}{{ page.bibles_page }}#books--chapters--verses) to create a new one.  Use the [bulk editor]({{ page.relpath }}{{ page.bibles_page }}#bulk-edit) to quickly enter a chapter or book.

## 6. Create slides[#](#qs-create-slides)
{: #qs-create-slides}
We're almost done!  Go to the `File` menu and choose `New Slide`.  From here you can create a slide with [placeholders]({{ page.relpath }}{{ page.slidecomponents_page }}#placeholder-component) or [media]({{ page.relpath }}{{ page.slidecomponents_page }}#media-component).  

Make sure to `Save`, then continue to the next step.

> **NOTE**: You can skip this step by using the sample slides provided.

## 7. Present slides[#](#qs-present-slides)
{: #qs-present-slides}
Now that we have our displays setup, Bible(s) imported, and slides created, we're ready to present.  Switch back to the Present tab and on the [Bible]({{ page.relpath }}{{ page.bibles_page }}#presenting-bible-verses) tab choose the [slide template]({{ page.relpath }}{{ page.slides_page }}#slide-basics).

![presenting bibles select template]({{ page.relpath }}assets/img/present-bible-verses-template.png){: .rounded .img-fluid}

Then choose the Bible you imported (if you didn't import a Bible, just use the sample bible), then click the `Find` button.

![presenting bibles select bibles]({{ page.relpath }}assets/img/present-bible-verses-bibles.png){: .rounded .img-fluid}

After clicking the `Find` button, you should see the slide preview update with the verse selected.  When you click the `Show` button the previewed slide will be presented onto the display.


