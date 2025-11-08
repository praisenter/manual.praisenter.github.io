---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Workspaces
date: 2025-11-03 09:48:58 -0500
relpath: ../
---

# Library
> The _Library_ is the list of all content within a [workspace](workspaces.html)
{: .p-man-page-intro}

Access the library by using the left navigation.  Click on the stacked squares icon.  The library allows you to create, update, delete, organize all your assets.  That includes Bibles, Song Lyrics, Slides, pictures, videos, and so on.

In the example below, we have a library with five items, three slide templates, one bible, and one song lyrics.  These items are automatically created when creating a new workspace and should be used for learning how to edit and maintain your content.

![Library]({{ page.relpath }}assets/img/library.png){: .rounded .img-fluid}

## Searching, filtering, & sorting[#](#searching-filtering--sorting)
As you collect more and more content, being able to find what you need becomes more important.  Use the library toolbar to search, filter, & sort your content.

![Library searching, filtering, and sorting]({{ page.relpath }}assets/img/library-search-filter-sort.png){: .rounded}

- The `search name/tags` box allows you to search the name of items and their tags.
- The `filter by` dropdown allows you to filter by the type of content.
- The `sort by` dropdown allows you to sort the content by name, type, etc.

Finally, the arrow at the end allows you to control the sort order

## Selecting an item[#](#selecting-an-item)
You can select items using the mouse.  Once an item is selected you can perform a few actions using the `File`, `Edit`, and context menus:
- `Edit` will open the item in the content editor.
- `Duplicate` will create an identical copy of the selected item, but with different name (and content id).
- `Delete` will delete the selected item.
- `Copy` will copy the item to the clipboard.
- `Rename` will allow you to rename the item.
- `Export` will prompt you to export the item to a zip file.

![Library select single item]({{ page.relpath }}assets/img/library-select-item.png){: .rounded .img-fluid}

## Content preview[#](#content-preview)
When selecting an item, a preview of the item is shown on the right side of the library.  The preview will be different based on the content type.  For some types, you can only see basic information, but for others you may have additional options.  All content will show the following details:

- The item name
- The date created / modified
- Ability to add/remove tags

> **NOTE**: Some file types like video have the ability to preview them.  Be careful when previewing content with audio if you have your computer audio output on.

![Library video preview]({{ page.relpath }}assets/img/library-preview-video.png){: .rounded .img-fluid}

## Selecting multiple items[#](#selecting-multiple-items)
You can select items using the mouse.  Once an item is selected, you can hold down `Shift` to select multiple items in order or `Ctrl` / `Command` to select individual items.  You can also use the `Left Arrow` and `Right Arrow` keys while holding `Shift` to select multiple items.

When multiple items are selected you can perform some of the same actions listed in the [Selecting an item](#selecting-an-item) section using the same `File`, `Edit`, and context menus:
- `Duplicate` will create an identical copy of the selected items, but with different names (and content ids).
- `Delete` will delete the selected items.
- `Copy` will copy the items to the clipboard.
- `Export` will prompt you to export the items to a zip file.

![Library select multple items]({{ page.relpath }}assets/img/library-select-items.png){: .rounded .img-fluid}

Another way to select multiple items is to use the mouse and click + drag.

![Library select multple items with mouse click + drag]({{ page.relpath }}assets/img/library-select-drag.png){: .rounded .img-fluid}

## Duplicate / copy[#](#duplicate--copy)
After selecting item(s) (refer to the [Selecting an item](#selecting-an-item) and [Selecting multiple items](#selecting-multiple-items) sections) you can Duplicate or Copy the item(s).

`Duplicate` immediately creates a copy of the item(s), renaming them with a `Copy of...` prefix.

`Copy` copies the items to the clipboard in a few different ways:
- If you paste into a text document, you will see the name of the items pasted
- If you paste into File Explorer, you will see the files themselves get pasted there
- If you paste into Praisenter, the items will be copied in the same way `Duplicate` works
- If you selected _one_ image/picture and you paste into a program that accepts image/picture content, the image/picture will be pasted

## Rename / Delete[#](#rename--delete)
After selecting item(s) (refer to the [Selecting an item](#selecting-an-item) and [Selecting multiple items](#selecting-multiple-items) sections) you can Rename or Delete the item(s).

`Rename` is only available when selecting a single item.  When clicked you will be prompted to supply the new name for the item.

> **NOTE**: You can also rename the item in the editor if it's a Bible, Song Lyrics, or Slide.

![Library rename item]({{ page.relpath }}assets/img/library-rename-prompt.png){: .rounded .img-fluid}

`Delete` will delete the items selected.  You will get an "Are you sure?" notification first.  If you choose to proceed, the items are deleted _permanently_.  There is no way to recover deleted items at this time.

![Library delete confirmation]({{ page.relpath }}assets/img/library-delete-prompt.png){: .rounded .img-fluid}

## Importing content[#](#importing-content)
Since Praisenter comes with minimal content, it's a natural next step to need to import content.  Importing content is easy - just drag the item you want imported onto the Praisenter window.  Select multiple items and drag-n-drop them into Praisenter to import multiple files at once.  Finally, you can also import `.zip` files containing any combination of the supported formats to import multiple items.

If you have Praisenter full screen and don't want to drag-n-drop, you can use the `File` -> `Import` menu.

> **NOTE**: _What happens to the original files after import?_ Nothing.  The original files are left as-is.  When you import, the files are _copied_ to the Praisenter workspace, so you are free to move, delete, rename, etc. those original files.

![Library drag n drop import]({{ page.relpath }}assets/img/library-import-dnd.png){: .rounded .img-fluid}

## Supported import formats[#](#supported-import-formats)
Praisenter supports a large number of formats.  Don't worry if you don't see the format you need, you have some other options when it comes to Bibles and Song lyrics.

> **NOTE**: Looking for an import format that's not currently provided?  [Log an issue on the project page](https://github.com/praisenter/praisenter/issues).

#### Bibles
- Praisenter format
- [Unbound Bibles](https://github.com/wnbittle/unbound-bible-archive)
- [Zefenia Bibles](https://sourceforge.net/projects/zefania-sharp/files/Bibles/)
- [OpenSong Bibles](https://opensong.org/downloads/#bibles)

#### Song lyrics
- Praisenter format
- [OpenLyrics](https://docs.openlyrics.org/en/latest/)
- [ChordPro](https://www.chordpro.org/chordpro/home/) (as of 3.1.7)
- [SongSelect](https://songselect.ccli.com/) (as of 3.1.7)
- ChurchView
- Older versions of Praisenter

#### Slides
- Praisenter format

#### Images & pictures
- PNG
- JPG / JPEG
- BMP / WBMP
- TIFF
- WEBP
- GIF

#### Audio / video
For audio & video files Praisenter supports a huge number of formats by transcoding them into a single supported format when importing.  Praisenter does this by packaging a static build of the [FFmpeg](https://ffmpeg.org/). Praisenter places the binary in the `media/tools` folder inside the workspace and communicates with it using shell commands.

You can determine all the formats supported for demuxing / muxing by using the following command.  Demuxers read audio / video data from a file and muxers write audio / video data to a file.

```shell
ffmpeg -codecs
```

## Exporting content[#](#exporting-content)
The primary function of export in Praisenter is to transfer content from one computer to another.  The idea is that you have Praisenter installed on one computer where you author content and installed on the computer that runs your presentations for service.  Export from one computer, then import into another.  This allows you to build content from anywhere since Praisenter is free to use on any and all computers.

The export feature can also be used to transfer content to another format or to gain access to the raw content.  One key exmaple of this are song lyrics where having a song in [ChordPro](https://www.chordpro.org/chordpro/home/) or [OpenLyrics](https://docs.openlyrics.org/en/latest/) formats is desirable.

To export content, select the items in the library (refer to the [Selecting an item](#selecting-an-item) and [Selecting multiple items](#selecting-multiple-items) sections), then use the `File` -> `Export` or context menu `Export` options.

Before being able to complete the export, you must choose the format that each content type should be exported as.  By default, the Praisenter format is chosen so that you can import into another workspace or computer.

Finally, choose the export file name and location.

> **NOTE**: _What happens to the items after export?_ Nothing.  The items are left as-is.  The exported file(s) are copies of the items in the workspace - you can rename, delete, move, etc. the file(s) without impacting the items in the workspace.

![Library export choose formats]({{ page.relpath }}assets/img/library-export-formats.png){: .rounded .img-fluid}

## Supported export formats[#](#supported-export-formats)
Praisenter supports a few different export formats in addition to it's native format.

> **NOTE**: Looking for an export format that's not currently provided?  [Log an issue on the project page](https://github.com/praisenter/praisenter/issues).

#### Bibles
- Praisenter format

#### Song lyrics
- [OpenLyrics](https://docs.openlyrics.org/en/latest/) (as of 3.1.7)
- [ChordPro](https://www.chordpro.org/chordpro/home/) (as of 3.1.7)
- Praisenter format

#### Slides
- Praisenter format

#### Images, pictures, audio, & video
- Praisenter format
- Raw format

The Praisenter format for this type of content is optimized for import into another Praisenter workspace or computer.  Always choose this format when transferring content to ensure content is transferred properly.  Not using this format could cause content to duplicate on import.

The Raw format is used to export the raw file from the workspace.  You can use this format if you are looking to get access to the raw file or if you don't mind content getting duplicated when importing into another workspace or computer.

## Indexing / Reindexing[#](#indexing--reindexing)
Praisenter uses [Lucene](https://lucene.apache.org/) to index everything added to the library.  This indexing is used to perform extremely fast searching on the content and their tags, especially when it comes to Bibles and Song lyrics.

One of the key benefits of this index is fuzzy matching when searching for Bible or Song lyric content when presenting.  This is very powerful when you don't know the exact phrase or words to search on.

Praisenter maintains the index in the background and will update it every time new content is added, updated or deleted.  However, there is an option to _reindex_ all content under the `File` -> `Reindex` menu.  You should never need to perform this operation, but in some cases it can be beneficial to perform a reindex.  Reindexing will delete the entire index and index all content from scratch.  If you are up to hundreds of items or a lot of songs/bibles, this could have a minor performance impact.