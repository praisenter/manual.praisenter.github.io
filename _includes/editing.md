# Editing
> Praisenter allows you to edit Bible, slide, and song lyrics assets within the application. In this section of the manual, we'll discuss the features that are shared across all the editors.
{: .p-man-page-intro}

You can access the editor by clicking the pencil icon in the left-hand navigation bar. The editor supports editing of document-type assets like Bibles, song lyrics, and slides. Other assets (like media files) can only be renamed and tagged from the [Library]({{ page.relpath }}{{ page.library_page }}#library).

When you click on the editor without any documents open, you'll see a hint on how to start editing.  Here are a few ways to start editing:
- From the `File` -> `New...` menu commands.
- From within the Editor, click one of the first three buttons in the toolbar to create a new document.
- From within the Library, double click an asset.
- From within the Library, select an asset and use the `Edit` command in the context menu.

![Editor]({{ page.relpath }}assets/img/editor-start.png){: .rounded .img-fluid}

Each document you have open for editing appears as a tab in the Editor allowing you to work on multiple documents simultaneously. When you attempt to close a tab containing unsaved changes, you're prompted to save, discard, or cancel. If the tab's name appears in a different color, that signals that there are unsaved changes.

![Editor document tabs]({{ page.relpath }}assets/img/editor-document-tabs.png){: .rounded .img-fluid}

When you have a lot of documents open for edit, all the tabs may not be visible.  You can scroll the tabs left and right using the mouse scroll wheel or using the down arrow ![Editor tab list button]({{ page.relpath }}assets/img/editor-tab-arrow.png){: .rounded} at the end.

## Toolbar[#](#toolbar)
While editing an document, the toolbar displays commands applicable to the currently selected tab and the selected element within that tab.  For example, since a slide is being edited in the screenshot below, the commands that relate to slides appear - buttons to create new slide elements, reorder elements, and the ability to snap those elements to a grid.

![Editor toolbar]({{ page.relpath }}assets/img/editor-toolbar.png){: .rounded .img-fluid}

> **NOTE**: The ![Editor toolbar arrow]({{ page.relpath }}assets/img/editor-toolbar-arrow.png){: .rounded} button at the end of the toolbar will contain commands that can't fit onto the toolbar.

Many of the toolbar commands are available from the `File`, `Edit`, and context menus as well.

## Side pane[#](#side-pane)
The _Side Pane_ on the right of the editor is where you modify properties of the selected element.  In the example below, a slide has been selected, so properties like the name, width, and height are editable.  If a different element is selected, the properties for that element are displayed.  Changes made in the Side Pane are immediately applied to the document so you can see the effects of your changes right away.

> **NOTE**: The _document_ properties are always visible regardless of what you have selected.

![Editor side pane]({{ page.relpath }}assets/img/editor-side-pane.png){: .rounded .img-fluid}

## Saving changes[#](#saving-changes)
Be sure to save frequently.  Save using the `File` -> `Save`, `File` -> `Save All`, or `File` -> `Save as...` menu commands or their corresponding [hotkeys](#hotkeys).  If you try to close an editor tab with unsaved changes, you will be prompted to save, discard or cancel.  A similar confirmation is shown if you try to close the application or [switch workspaces]({{ page.relpath }}{{ page.workspaces_page }}#switching-workspaces) with unsaved changes.

![Editor unsaved changes prompt]({{ page.relpath }}assets/img/editor-unsaved-prompt.png){: .rounded .img-fluid}

> **NOTE**: If you are editing a slide that is currently showing on a display, the display content will remain unchanged.  However, if the slide is in a [queue]({{ page.relpath }}{{ page.presenting_page }}#queue-management), the queued slide be updated when you save.  If you have the slide selected as a template, the [slide preview]({{ page.relpath }}{{ page.presenting_page }}#slide-preview) will also reflect any saved changes the next time you preview it.

When using the `File` -> `Save as...` command, Praisenter will prompt you to name the new document.  The new document is saved to the library and opened as a _new tab_ in the editor.  The original document, and any edits you made, will still be available.  If you don't want to save the changes to the original document, you can discard your changes by closing the editor tab of the original document and choosing "No" when notified of unsaved changes.

## Copy / cut / paste[#](#copy--cut--paste)
When editing an document, you can copy, cut, and paste elements. For example, imagine you are entering song lyrics and verse 1 and verse 2 are nearly identical - don't create verse 2 from scratch - copy and paste verse 1 and then modify the copy.  Another example is when you are editing multiple slides and you want some elements from Slide 1 on Slide 2, just select the elements and copy & paste them to Slide 2.

## Rename / delete[#](#rename--delete)
As mentioned in [Rename / delete]({{ page.relpath }}{{ page.library_page }}#lib-rename-delete) section, you have the ability to rename documents in the editor from the right Side Pane.

Delete, however, works differently.  The `Delete` command now works on the element level instead of at the document level.  What this means is that if you use the <kbd>Delete</kbd> key or menu commands, it will delete the selected _element_.  For example, if you are editing a Slide and have an image selected, the delete command will delete the image, not the slide itself.

## Undo / redo[#](#undo--redo)
All editors support undo and redo.  Undo allows you to reverse the last change you made and redo allows you to reapply the last change you made.

> **NOTE**: Once you close an editor all the undo and redo history is lost.

## Hotkeys[#](#hotkeys)
You can do everything with the mouse, but some commands are easier with the keyboard.  With that in mind, Praisenter has hotkeys, or key combinations, to perform common actions:

| Action | Windows | Ubuntu | MacOS |
|--------|----------------|---------------|--------------|
| Save | <kbd><kbd>Ctrl</kbd> + <kbd>S</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>S</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>S</kbd></kbd> |
| Save All | <kbd><kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd></kbd> |
| Undo | <kbd><kbd>Ctrl</kbd> + <kbd>Z</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>Z</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>Z</kbd></kbd> |
| Redo | <kbd><kbd>Ctrl</kbd> + <kbd>Y</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Z</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>Shift</kbd> + <kbd>Z</kbd></kbd> |
| Copy | <kbd><kbd>Ctrl</kbd> + <kbd>C</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>C</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>C</kbd></kbd> |
| Cut | <kbd><kbd>Ctrl</kbd> + <kbd>X</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>X</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>X</kbd></kbd> |
| Paste | <kbd><kbd>Ctrl</kbd> + <kbd>V</kbd></kbd> | <kbd><kbd>Ctrl</kbd> + <kbd>V</kbd></kbd> | <kbd><kbd>Command</kbd> + <kbd>V</kbd></kbd> |
{: .table .w-auto}

You can find them all in the menus - the hotkeys are to the right of the action.