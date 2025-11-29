# Library
> The _Library_ in Praisenter is where you store and manage all of your presentation assets - including Bibles, slides, song lyrics, images, and videos. Each [workspace]({{ page.relpath }}{{ page.workspaces_page }}#workspaces) manages a single library of assets.
{: .p-man-page-intro}

You access the library by clicking on the stacked squares icon in the left navigation.  The library allows you to import, create, update, delete, organize your assets.  You can also export, preview, tag, and rename your assets from here.

In the example below, we have a library with five assets: three slide templates, one bible, and one song lyrics.  The assets shown below are the [default assets]({{ page.relpath }}{{ page.home_page }}#default-content) imported when creating a new workspace.  The sample assests are there to help you get going quickly and to learn from.

![Library]({{ page.relpath }}assets/img/library.png){: .rounded .img-fluid}

## Searching, filtering, & sorting[#](#searching-filtering--sorting)
As you continue to collect assets, finding a specific asset can become challenging.  Use the library toolbar to search, filter, & sort your assets to find exactly what you are looking for.

![Library searching, filtering, and sorting]({{ page.relpath }}assets/img/library-search-filter-sort.png){: .rounded .img-fluid}

- The `search name/tags` box allows you to search the name of assets and their tags.
- The `filter by` dropdown allows you to filter by the type of asset.
- The `sort by` dropdown allows you to sort assets by name, type, etc.

Finally, the arrow at the end allows you to control the sort order.

## Selecting an asset[#](#selecting-an-item)
{: #selecting-an-item}
You can select assets using the left mouse button.  Once an asset is selected you can perform a few actions using the `File`, `Edit`, and context menus:

- `Edit` (only available on the context menu) will open the asset in the [editor]({{ page.relpath }}{{ page.editing_page }}#editing).
- `Duplicate` will create an identical copy of the selected asset, but with different name and id.  You cannot duplicate media assets.
- `Delete` will delete the selected asset (permanently).
- `Copy` will copy the asset to the clipboard.
- `Rename` will allow you to rename the asset.
- `Export` will prompt you to export the asset to a zip file.

![Library select single item]({{ page.relpath }}assets/img/library-select-item.png){: .rounded .img-fluid}

## Asset preview[#](#content-preview)
{: #content-preview}
When selecting an asset, a preview is shown on the right side of the library.  The preview will be different based on the asset type.  For some, you can only see basic information, while others may have additional options.  All assets will show the following details:

- The asset name
- The date created / modified
- Ability to add/remove tags

> **NOTE**: Some asset types like video have the ability to play them.  Be careful when previewing assets with audio.  Make sure your computer audio is muted, the asset is muted in the player, or the audio out from the computer is muted.

![Library video preview]({{ page.relpath }}assets/img/library-preview-video.png){: .rounded .img-fluid}

## Selecting multiple assets[#](#selecting-multiple-items)
{: #selecting-multiple-items}
You can select multiple assets using the mouse and keyboard.  Once an asset is selected, you can hold down <kbd>Shift</kbd> while using the left mouse button to select multiple assets in order.  Similarly, hold down the <kbd>Ctrl</kbd> / <kbd>Command</kbd> key to select _any_ set of assets with the left mouse button.  Finally, use the <kbd>&larr;</kbd> and <kbd>&rarr;</kbd> keys while holding <kbd>Shift</kbd> to select multiple assets in a row with the keyboard only.

When multiple assets are selected you can perform some of the same actions listed in the [Selecting an item](#selecting-an-item) section from `File`, `Edit`, and context menus:
- `Duplicate` will create an identical copy of the selected assets, but with different names (and ids).  However, you cannot duplicate media assets.
- `Delete` will delete the selected assets (permanently).
- `Copy` will copy the assets to the clipboard.
- `Export` will prompt you to export the assets to a zip file.

![Library select multple items]({{ page.relpath }}assets/img/library-select-items.png){: .rounded .img-fluid}

The last way to select multiple assets is to use the mouse and click + drag a rectangle over the assets you want selected.

![Library select multple items with mouse click + drag]({{ page.relpath }}assets/img/library-select-drag.png){: .rounded .img-fluid}

## Duplicate / copy[#](#duplicate--copy)
After [selecting an asset](#selecting-an-item) or [selecting multiple assets](#selecting-multiple-items) you can duplicate or copy &amp; paste them.

The `Duplicate` command immediately creates a copy of the asset and adds it to the library.  The duplicate will be renamed with a `Copy of...` prefix.

The `Copy` command copies the assets to the clipboard so you can `Paste` them elsewhere.  What happens when you paste will depend on where you perform the paste command:
- If you paste into a text document, the names of the assets will be pasted.
- If you paste into File Explorer, the files themselves will be pasted.
- If you paste into Praisenter, the assets will be duplicated in the same way as the `Duplicate` command.
- If you selected _one_ image/picture and you paste into a program that accepts image/picture content, the image/picture will be pasted

## Rename / Delete[#](#lib-rename-delete)
{: #lib-rename-delete}
After [selecting an asset](#selecting-an-item) or [selecting multiple assets](#selecting-multiple-items) you can rename or delete them.

The `Rename` command is only available when a single asset is selected.  When clicked you will be prompted to supply the new name for the asset.  Renaming an asset is a safe operation - any other asset like slides will continue to reference the renamed asset.  This also applies to any selected Bibles and song lyrics in the [display controller]({{ page.relpath }}{{ page.displays_page }}#display-controllers).

> **NOTE**: You can also rename the asset in the editor if it's a Bible, song lyrics, or a slide.

![Library rename item]({{ page.relpath }}assets/img/library-rename-prompt.png){: .rounded .img-fluid}

The `Delete` command will delete the selected assets _permanently_.  An "Are you sure?" notification is displayed first to confirm if you'd like to continue.  You will also see a confirmation message if the asset is used by another asset in the library (slides in particular).  If you choose to continue, the assets are deleted.  There is no way to recover deleted assets from the library, but you can always re-import them if you have the originals stored elsewhere.  Any assets like slides that reference the deleted assets will continue to work, but will not be able to show that asset when presented.

![Library delete confirmation]({{ page.relpath }}assets/img/library-delete-prompt.png){: .rounded .img-fluid}

## Create Slide[#](#create-slide)
Have you ever been tasked with quickly presenting a picture, image, or video?  Praisenter requires the asset to be placed on a [slide]({{ page.relpath }}{{ page.slides_page }}#slide-basics) before it can be presented.  Select the asset and use the `+ Create Slide` context menu command to create a slide with the media on it, save it, and then present it - just three steps.

This feature performs the following steps:
- Creates a new slide sized for your primary screen/output.
- Sets the slide name to "Untitled _the asset name_".
- Sets the slide background to black.
- Adds a [Media Component]({{ page.relpath }}{{ page.slidecomponents_page }}#media-component) to the slide with the selected asset.
- Sizes the media component to cover the entire slide.
- Configures the media component to keep the aspect ratio of the asset

![Library create slide]({{ page.relpath }}assets/img/library-create-slide.png){: .rounded .img-fluid}

## Importing assets[#](#importing-content)
{: #importing-content}
Importing assets is easy - just drag the file you want imported onto the Praisenter window.  In face, you can select multiple files and drag them onto the Praisenter window to import multiple assets at once!  Praisenter can also import `.zip` files containing any combination of supported files.

If you are running Praisenter full screen and don't want to drag-and-drop, you can use the `File` -> `Import` menu.

> **NOTE**: _What happens to the original files after import?_ Nothing!  The original files are left unchanged and in the place you found them.  This is because Praisenter _copies_ the files to the workspace.  You are free to move, delete, rename, or do anything with those original files.

> **NOTE**: Make sure to wait for the import to complete before moving, renaming, deleting, and/or updating the original files.  This is especially important for video and audio files.

![Library drag n drop import]({{ page.relpath }}assets/img/library-import-dnd.png){: .rounded .img-fluid}

## Supported import formats[#](#supported-import-formats)
Praisenter supports a large number of formats.  For Bibles and song lyrics, don't worry if you don't see the format you need - there are bulk edit options that can be used as an alternative to importing.

> **NOTE**: Looking for an import format that's not currently provided?  [Log an issue on the project page](https://github.com/praisenter/praisenter/issues).

**Bibles**
- Praisenter format
- [Unbound Bibles](https://github.com/wnbittle/unbound-bible-archive)
- [Zefenia Bibles](https://sourceforge.net/projects/zefania-sharp/files/Bibles/)
- [OpenSong Bibles](https://opensong.org/downloads/#bibles)

**Song lyrics**
- Praisenter format
- [OpenLyrics](https://docs.openlyrics.org/en/latest/)
- [ChordPro](https://www.chordpro.org/chordpro/home/) (as of 3.1.7)
- [SongSelect](https://songselect.ccli.com/) (as of 3.1.7)
- ChurchView
- Older versions of Praisenter

**Slides**
- Praisenter format

**Images & pictures**
- PNG
- JPG / JPEG
- BMP / WBMP
- TIFF
- WEBP
- GIF

**Audio / video**
Praisenter supports a huge number of audio & video container formats and codecs by [transcoding](https://en.wikipedia.org/wiki/Transcoding) them during import into a single optimized format.  Praisenter does this by packaging a static build of the [FFmpeg](https://ffmpeg.org/) library. Praisenter places the binary in the `media/tools` folder inside the workspace and communicates with it using shell commands.

You can determine all the formats supported for demuxing / muxing by using the following command.  Demuxers read audio / video data from a file and muxers write audio / video data to a file and are crucial to transcoding process.

```shell
ffmpeg -codecs
```

## Exporting assets[#](#exporting-content)
{: #exporting-content}
The primary function of export is to transfer assets from one computer to another.  The idea is that you have Praisenter installed on _many_ computers.  Having Praisenter on multiple computers allows you to build and collect assets on one and import them on another.

The export feature can also be used to convert assets to another format or to gain access to the raw asset itself.  Song lyrics is a good example - having a song in [ChordPro](https://www.chordpro.org/chordpro/home/) or [OpenLyrics](https://docs.openlyrics.org/en/latest/) formats allows you to transfer that asset to another application.  Another example is if you want access to a video you imported into the library and can't find the original anywhere.

To export, [select the assets](#selecting-multiple-items) you want to export, then use the `File` -> `Export` or context menu `Export` commands.  Before being able to complete the export, you must choose the export format for each asset type.  By default, the Praisenter format is chosen.

Finally, choose the export file name and location.

> **NOTE**: _What happens to the assets in the library after they are exported?_ Nothing.  The assets are left as-is.  The exported file(s) are copies of the assets in the workspace - you can rename, delete, move, etc. the file(s) contained within the `.zip` without impacting the assets in the workspace.

![Library export choose formats]({{ page.relpath }}assets/img/library-export-formats.png){: .rounded .img-fluid}

## Supported export formats[#](#supported-export-formats)
Praisenter supports a few different export formats in addition to it's native format.

> **NOTE**: Looking for an export format that's not currently provided?  [Log an issue on the project page](https://github.com/praisenter/praisenter/issues).

**Bibles**
- Praisenter format

**Song lyrics**
- [OpenLyrics](https://docs.openlyrics.org/en/latest/) (as of 3.1.7)
- [ChordPro](https://www.chordpro.org/chordpro/home/) (as of 3.1.7)
- Praisenter format

**Slides**
- Praisenter format

**Images, pictures, audio, & video**
- Praisenter format
- Raw format

The Praisenter format is optimized for _import_ into another Praisenter workspace.  Always choose this format when transferring assets between two Praisenter workspaces to ensure they are transferred properly.  Using a different format could cause assets to duplicate when imported.

The Raw format is used to export the raw file(s) from the workspace.  You can use this format if you are looking to get access to the raw file(s) or if you don't mind assets being duplicated during import into another Praisenter workspace.

## Indexing / Reindexing[#](#indexing--reindexing)
Praisenter uses [Lucene](https://lucene.apache.org/) to index everything added to the library.  Indexing is used to perform extremely fast searching on the content and tags of an asset.  This is especially true for Bibles due to their length and song lyrics due to the number of songs you may add to the library.

Another key benefit of indexing is _fuzzy matching_ content in Bible verses or song lyrics.  This is a very powerful feature when you don't know the exact phrase, words, or spelling to use.

Praisenter maintains the index in the background every time new assets are added, updated or deleted.  There's also a command to _reindex_ all content under the `File` -> `Reindex` menu.  In general, using this command is unnecessary, but in some cases it can be beneficial to perform a reindex.  Reindexing will delete the current index and reindex all assets from scratch.  If the library contains hundreds of assets or many songs or Bibles, this could have a minor performance benefit.
