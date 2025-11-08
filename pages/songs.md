---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Song Lyrics
date: 2025-11-03 09:48:58 -0500
relpath: ../
---

# Song Lyrics
> Praisenter provides the ability to use song lyrics as part of a presentation and show multiple lyrics at one time.
{: .p-man-page-intro}

Praisenter doesn't come with any song lyrics or songbooks, but you can import lyrics from other sources.  A popular source for song lyrics is [SongSelect](https://songselect.ccli.com/).  Supported file formats include:

- [OpenLyrics](https://docs.openlyrics.org/en/latest/)
- [ChordPro](https://www.chordpro.org/chordpro/home/) (as of 3.1.7)
- [SongSelect](https://songselect.ccli.com/) (as of 3.1.7)

Later in the manual you can find a few other ways to add song lyrics.

## Lyrics / sections[#](#lyrics--sections)
In Praisenter, song content is split into two distinct categories: Lyrics and Sections.  A Section is simply a paragraph of text representing _verse_ of a song - something like verse 1, bridge, or chorus.  A group of Sections is called a Lyric.  The Lyric can also include Authors and Song Book references.

What's interesting is that each song in Praisenter can have multiple Lyrics.  That means you could have two different translations of lyrics in the same song.  In the example below, notice how there are multiple _Lyrics_ under the song: "My Special Song" and "Mi Canción Especial".  Also notice that each _Lyric_ has it's own _Authors_, _Song Books_, and _Sections_.

> **NOTE**: Praisenter does not support styling, chords, music notation, or other markup.

![Song lyrics and sections]({{ page.relpath }}assets/img/songs-structure.png){: .rounded .img-fluid}

> **NOTE**: As mentioned earlier, since the song above is structured this way, we would be able to show both the English Verse 1 _and_ the Spanish Verse 1 on a single slide during a presentation.

A song is edited using a tree-like view (see the example above).  You can expand and collapse lyrics, authors, and song books.  Clicking on each item in the view will allow you to edit it in the [Side Pane]({{ page.relpath }}pages/editing.html#side-pane) on the right.  As you click on each item in the view, toolbar and menu options will enable and disable.  For example, if you select a Lyric item, you can create a Section, Author, and Song Book.  However, if you click on the Song, you can only create a Lyric.

> **NOTE**: You can also copy, cut, & paste lyrics, sections, authors, and song books within a single song or between songs.

## Bulk edit[#](#bulk-edit)
Editing a Song by selecting and editing each item can be very tedious.  With that in mind Praisenter allows you to bulk edit Lyrics.  When bulk editing, the editor switches to a text view.  It's very important that you follow these guidelines when bulk editing to make sure that Praisenter can interpret your changes correctly.

You can trigger bulk editing by selecting a Lyric and using the `Edit` -> `Bulk Edit` menu, the context menu, or by clicking the `Bulk Edit` button in the [Side Pane]({{ page.relpath }}pages/editing.html#side-pane).

![Song lyric bulk edit]({{ page.relpath }}assets/img/songs-bulk-edit.png){: .rounded .img-fluid}

> **NOTE**: You cannot bulk edit an entire `Song`.

Here's an example of properly formatted text when bulk editing:
```text
My lyric title

Verse 1
Amazing grace how sweet the sound
That saved a wretch like me
I once was lost but now am found
Was blind but now I see

Chorus
'Twas grace that taught my heart to fear
And grace my fears relieved
How precious did that grace appear
The hour I first believed
```

The first line should be the title of the lyrics - generally it's same as the name of the song.  Then there MUST be an empty line like on line 2 above.  After the first empty line, you can being writing the song verses.  Start with the verse type or name - in the example above it's `Verse 1`.  Immediately after the verse type/name, continue with the lines that make up that verse.  To start a new verse, create an empty line and repeat the process.  For example, the empty line on line 8 signifies that a new section is starting.

When you are done editing click the `Done` button in the bottom right corner of the editor.  You can also discard any changes you made by clicking the `Cancel` button.

### Incorrect Examples

This lyric is incorrectly formatted because it's missing the blank line after the lyric title `My lyric title`.
```text
My lyric title
Verse 1
Amazing grace how sweet the sound
That saved a wretch like me
I once was lost but now am found
Was blind but now I see
```

This lyric is incorrect because there's a blank line in between `Verse 1` and `Amazing grace how sweet the sound`:
```text
My lyric title

Verse 1

Amazing grace how sweet the sound
That saved a wretch like me
I once was lost but now am found
Was blind but now I see
```

This lyric is incorrect because there's no blank line between `Was blind but now I see` and `Chorus`:
```text
My lyric title

Verse 1
Amazing grace how sweet the sound
That saved a wretch like me
I once was lost but now am found
Was blind but now I see
Chorus
'Twas grace that taught my heart to fear
And grace my fears relieved
How precious did that grace appear
The hour I first believed
```

## Reordering[#](#reordering)
At times you may have sections that are out of order and reordering them manually can be a chore.  Praisenter offers a few ways to reorder them:

- Start bulk editing and copy/paste around as needed
- Click & drag items around with the mouse
- Copy, cut, & paste items with the mouse & [hotkeys]({{ page.relpath }}pages/editing.html#hotkeys)

## PDF import[#](#pdf-import)
A feature specific to Song editing is PDF Import.  This feature only shows up during bulk editing.  You can find a button for it in the bottom right corner of the editor.  Praisenter will load the PDF, read the text from it, and place it into the bulk editor.

> **NOTE**: The PDF import process is primarily used to extract text from a PDF.  It will NOT format that the text it extracts to match the requirements of the Bulk Editor, so make sure you review the text that was extracted and format it properly before saving.

As an example, in the screenshot below I've imported a rather nasty PDF document called "Above All".

![Song PDF import pdf sample]({{ page.relpath }}assets/img/songs-pdf-import-ex.png){: .rounded .img-fluid}

You can see that the text from the document was extracted, but it's not formatted very well.

![Song PDF import after import]({{ page.relpath }}assets/img/songs-pdf-import.png){: .rounded .img-fluid}

After a minute of manual clean up:

![Song PDF import after clean up]({{ page.relpath }}assets/img/songs-pdf-import-ex2.png){: .rounded .img-fluid}
