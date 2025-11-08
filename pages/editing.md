---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Editing Items
date: 2025-11-03 09:48:58 -0500
relpath: ../
---

# Editing
> Praisenter allows you to edit content within the application.  There are some features hidden in the editor that will be highlighted in this manual.
{: .p-man-page-intro}

You can access the editor by using the left navigation - click on the pencil icon.  The editor allows you to edit items (and multiple at a time) from within Praisenter. Items that can be edited include Bibles, Song Lyrics, and Slides.  Other assets can be renamed and allow tagging from the library.

When you click on the editor without any items open, you'll see a hint on how to start editing.  You have a few ways to start editing:
- From the `File` -> `New...` menu options to create new items
- From within the Editor, click one of the first three buttons in the toolbar to create a new item
- From within the Library, double click an item
- From within the Library, select an item and use the `Edit` option in the context menu

![Editor]({{ page.relpath }}assets/img/editor-start.png){: .rounded .img-fluid}

Each item you have open for editing will appear as a tab in the Editor.  This allows you to have multiple items open for editing at a time.  When you are finished editing an item, you can use the `x` on the tab to close the editor.  If you have unsaved changes you will be prompted to save or discard those changes.  When you see the item name in the tab a different color, there are unsaved changes.  

![Editor document tabs]({{ page.relpath }}assets/img/editor-document-tabs.png){: .rounded .img-fluid}

When you have a lot of items open for edit, all the tabs won't be visible.  You can scroll the tabs left and right using the mouse scroll wheel or using the down arrow ![Editor tab list button]({{ page.relpath }}assets/img/editor-tab-arrow.png){: .rounded} at the end.

## Toolbar[#](#toolbar)
When editing an item, the toolbar at the top of the Editor will display actions applicable to the currently selected tab and element within that tab.  For example, in this example, a Slide is being edited.  Because it's a slide, I get options that relate to slide editing like buttons to create new slide elements, reorder elements, and the ability to snap those elements to a grid.

![Editor toolbar]({{ page.relpath }}assets/img/editor-toolbar.png){: .rounded .img-fluid}

> **NOTE**: The ![Editor toolbar arrow]({{ page.relpath }}assets/img/editor-toolbar-arrow.png){: .rounded} item at the end of the toolbar will contain actions that can't fit onto the toolbar give the size of the window.

In addition to the toolbar, many of these same actions are available from the `File`, `Edit`, and context menus.

## Side pane[#](#side-pane)
While the Toolbar is primarily for actions, the right Side Pane is used to perform the editing.  The Side Pane, like the Toolbar, will change based on the selected element in the Editor.  For example, when you have a slide selected, you'll see something like this:

![Editor side pane]({{ page.relpath }}assets/img/editor-side-pane.png){: .rounded .img-fluid}

The Side Pane is a list of editable properties of the selected component.  For the example above, since we have the slide itself selected, we can change things like the Name, width & height, and tags.  When we select a different element, we'll get all the editable options for that element.

Changes made in the Side Pane are applied immediately to the item so you can see the affect of the change right away.

## Saving changes[#](#saving-changes)
As your editing your items, you'll want to make sure to save your work.  You can do this using the `File` -> `Save` or `File` -> `Save All` menu options or their [hotkeys](#hotkeys).  Praisenter does _not_ have an auto-save feature, but does go to great lengths to prevent any unsaved changes being lost.  As mentioned earlier, if you try to close the editor tab with unsaved changes, you will be prompted to save, discard or cancel.  If you try to close the application, a similar prompt is shown.

![Editor unsaved changes prompt]({{ page.relpath }}assets/img/editor-unsaved-prompt.png){: .rounded .img-fluid}

> **NOTE**: While editing, any item being presented will remain as-is.  The next _show_ action you take with that item should pick up any changes that have been saved.

> **NOTE**: A best practice with any application is to save often.

## Copy / cut / paste[#](#copy--cut--paste)
When editing an item, you can copy, cut, and paste content. For example, imagine you are entering Song Lyrics and verse 1 and verse 2 are nearly identical - don't recreate verse 2 from scratch - copy and paste verse 1 and then modify the copy.  Another example is when you are editing multiple slides and you want some elements from Slide 1 on Slide 2, just select the elements and copy & paste them to Slide 2 - no need to recreate them.

## Rename / delete[#](#rename--delete)
As mentioned in [Rename / delete]({{ page.relpath }}pages/library.html#rename--delete), you have the ability to rename items in the editor from the right Side Pane.

Delete, however, works differently.  The Delete action now works on the element level instead of at the item level.  What this means is that if you use the <kbd>Delete</kbd> key or menu option, it will delete the selected element.  For example, if you are editing a Slide and have an image selected, the Delete action will delete that element, not the slide itself.

## Undo / redo[#](#undo--redo)
All editors support undo and redo.  Undo allows you to back out the last change you made and redo allows you to reapply the last change you made.

> **NOTE**: Once you close an editor all the undo and redo history is lost.

## Hotkeys[#](#hotkeys)
You can do everything with a mouse, but some actions are just easier with the keyboard.  With that in mind, Praisenter has hotkeys, or key combinations, to perform common actions:

| Action | Windows | Ubuntu | MacOS |
|--------|----------------|---------------|--------------|
| Save | <kbd><kbd>Ctrl</kbd> + <kbd>S</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>S</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>S</kbd></kbd> |
| Save All | <kbd><kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd></kbd> |
| Undo | <kbd><kbd>Ctrl</kbd> + <kbd>Z</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>Z</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>Z</kbd></kbd> |
| Redo | <kbd><kbd>Ctrl</kbd> + <kbd>Y</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Z</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>Shift</kbd> + <kbd>Z</kbd></kbd> |
| Copy | <kbd><kbd>Ctrl</kbd> + <kbd>C</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>C</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>C</kbd></kbd> |
| Cut | <kbd><kbd>Ctrl</kbd> + <kbd>X</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>X</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>X</kbd></kbd> |
| Paste | <kbd><kbd>Ctrl</kbd> + <kbd>V</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>V</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>V</kbd></kbd> |
{: .table .w-auto}

You can find them all in the menus - the hotkeys are to the right of the action.