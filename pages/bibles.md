---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Bibles
date: 2025-11-03 09:48:58 -0500
relpath: ../
---

# Bibles
> Instead of searching, copying, pasting, or typing in bible verses into slides, Praisenter allows you to import, create, edit, and maintain any number of bibles and use that content when presenting.
{: .p-man-page-intro}

Praisenter doesn't come packaged with a bible, but you can import bibles from the following sources:

- [Unbound Bibles](https://github.com/wnbittle/unbound-bible-archive)
- [Zefenia Bibles](https://sourceforge.net/projects/zefania-sharp/files/Bibles/)
- [OpenSong Bibles](https://opensong.org/downloads/#bibles)

> **NOTE**: Praisenter does not endorse these bibles or their contributors. Praisenter cannot guarantee the bibles offered on these sites to be accurate and cannot verify their content. Also consider their individual copyright notices before using or distributing them.

## Books / chapters / verses[#](#books--chapters--verses)
Bibles are divided into books, and books are divided into chapters, and chapters are divided into verses.  This is a standard pattern instituted long ago to help with indexing, reference, research, studying, and so on.  This structure also helps when it comes to presenting Bible verses on the screen.

A Bible can have many Books.  A Book can have many chapters.  A Chapter can have many verses.  A verse is a simple paragraph of text.  Praisenter does not support styling, so red-letter, italics, or other study aids.

Each Bible should represent one _language_ or _translation_.  Doing so will allow you to show two bibles at once, provided you've created a slide template to support it.  For example, if you want to show both English and Spanish on one slide, create/import two bibles, one English and one Spanish.  This also works for translations.  Imagine you want to show both the KJV along side the NIV, create/import two bibles, one KJV and one NIV.

![Bible, book, chapter, verse structure]({{ page.relpath }}assets/img/bibles-structure.png){: .rounded .img-fluid}

The Bible is edited using a tree-like view (see the example above).  You can expand and collapse books and chapters to help find what you are looking for.  Clicking on each item in the view will allow you to edit it in the [Side Pane]({{ page.relpath }}pages/editing.html#side-pane) on the right.  As you click on each item in the view, toolbar and menu options will enable and disable.  For example, if you select a Chapter item, you can create a verse or a Chapter, but not a Book.  However, if you click on a book or the bible item, you _can_ create a book.

> **NOTE**: You can also copy, cut, & paste books, chapters, and verses within a single bible or between bibles.

## Bulk edit[#](#bulk-edit)
Editing a Bible by selecting and editing each item can be very tedious.  With that in mind Praisenter allows you to bulk edit Books and Chapters.  When bulk editing, the editor switches to a text view.  It's very important that you follow these guidelines when bulk editing to make sure that Praisenter can interpret your changes correctly.

You can trigger bulk editing by using the `Edit` -> `Bulk Edit` menu, the context menu, or by clicking the `Bulk Edit` button in the [Side Pane]({{ page.relpath }}pages/editing.html#side-pane).

![Bible book bulk edit]({{ page.relpath }}assets/img/bibles-bulk-edit.png){: .rounded .img-fluid}

> **NOTE**: You cannot bulk edit an entire `Bible`.

Here's an example of properly formatted text when bulk editing a `Book`:
```text
1 Genesis
1
1 In the beginning God created the heavens and the earth.
2 Now the earth was formless and empty, darkness was over the surface of the deep, and the Spirit of God was hovering over the waters.

2
1 Thus the heavens and the earth were completed in all their vast array.
2 By the seventh day God had finished the work he had been doing; so on the seventh day he rested from all his work.
```

Here's an example of properly formatted text when bulk editing a `Chapter`:
```text
1
1 In the beginning God created the heavens and the earth.
2 Now the earth was formless and empty, darkness was over the surface of the deep, and the Spirit of God was hovering over the waters.
```

Empty lines and extra spaces at the start and beginning of lines will be removed.

When you are done editing click the `Done` button in the bottom right corner of the editor.  You can also discard any changes you made by clicking the `Cancel` button.

### Bulk edit - Book definition
The definition of a Book starts with a number with their name after it.  There MUST be some empty space between the number and the name and they MUST be on the same line.  The book definition MUST be the first line in the editor.

Examples of accepted book definitions:
```text
1 Genesis
 2 Exodus
66    Revelation
5 Song of Solomon
  11      This is a book title   
```

Examples of invalid book definitions:
```text
Genesis
 Genesis
1Genesis
3Song of solomon
Genesis 1
```

Lines 1 & 2 are missing the book number.  Lines 3 & 4 are missing space between the book number and book name.  Line 5 has the book number at the end, it should be at the beginning instead.

### Bulk edit - Chapter definition
The definition of a chapter is easy, it's just a number!  However, if you are bulk editing a Book, it must come _after_ a Book definition.  If you are bulk editing a Chapter, then the chapter definition must be the first line in the editor.

Examples of accepted chapter definitions:
```text
1
 2   
```

Examples of invalid chapter definitions:
```text
 
Some text
```

The first line is invalid because nothing was provided.  The second line is invalid because a chapter only needs a chapter number, which is missing, and no name.

### Bulk edit - Verse definition
The verse definition is very similar to the Book definition - it's the verse number, some space, and the verse text.  The verse MUST be on one line.

Examples of accepted verse definitions:
```text
1 This is the verse text
 3 This is the verse text
5     This is the verse text
 7        This is the verse text    
```

Examples of invalid verse definitions:
```text
This is the verse text
 This is the verse text
1This is the verse text
```

The first and second lines are invalid because they are missing the verse number.  The last line is invalid because there's no space between the verse number and verse text.

## Reordering[#](#reordering)
At times you may have items that are out of order and reordering them manually can be a chore.  Praisenter offers a few ways to reorder books, chapters, and verses.

- Start bulk editing and copy/paste around as needed
- Click & drag items around with the mouse
- Copy, cut, & paste items with the mouse & [hotkeys]({{ page.relpath }}pages/editing.html#hotkeys)
- Use the `Sort by Number` menu item (see below)

## Sort by number[#](#sort-by-number)
Reordering using the `Sort by Number` menu item will do just that - it will reorder the items under the selected item based on their current number.  For example, in the screenshot below, we are reordering the verses inside Chapter 1.  Performing this action will reorder the verses based on their verse number from smallest to largest.

![Bible sort by number]({{ page.relpath }}assets/img/bibles-reordering.png){: .rounded .img-fluid}

In the screenshot below, notice how the verses were rearranged based on their verse number.

![Bible sort by number result]({{ page.relpath }}assets/img/bibles-reordering-result.png){: .rounded .img-fluid}

## Number by order[#](#number-by-order)
Number by order is the opposite of Sort by number.  Instead of _sorting_ the items (verses for example), this option will _re-number_ them in the order in which they appear.  

![Bible number by order]({{ page.relpath }}assets/img/bibles-renumbering.png){: .rounded .img-fluid}

Using the same example above, if we renumber Chapter 1, we would be left with the following.  Notice how the verse text stayed in the same order, but the verses were numbered in-order from 1 to 4.

![Bible number by order result]({{ page.relpath }}assets/img/bibles-renumbering-result.png){: .rounded .img-fluid}
