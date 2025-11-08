---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Slide components
date: 2025-11-03 09:48:58 -0500
relpath: ../
---

# Slide components
> Slides are made up of the slide itself and it's _slide components_.  Adding components to your slides is how you add media, text, and other content.
{: .p-man-page-intro}

Now that you've reviewed the [basics]({{ page.relpath }}pages/slides.html), we will introduce each component type available in Praisenter.  Then we'll cover how to move, resize, and layer them.

## Text component[#](#text-component)
The text component is used to put static text on a slide and style that text.  You have all the options described in [Slide basics]({{ page.relpath }}pages/slides.html) to configure the font, color, borders, backgrounds and more.

To edit the text itself, you can find that in the [Side Pane]({{ page.relpath }}pages/editing.html#side-pane) on the right.

![Slides text component]({{ page.relpath }}assets/img/slides-text-component.png){: .rounded .img-fluid}

## Placeholder component[#](#placeholder-component)
The placeholder component is very similar to the text component - it's used to show text.  However, it's unique because the text is not directly editable.  Instead, the text that will show in the component will be determined during presentation.  It's a _placeholder_ for text.

A placeholder component is used for displaying bible and song verses.  More on this in the Presentation part of the manual.  If a slide has any placeholder components, then it's considered a slide _template_.

![Slides placeholder component]({{ page.relpath }}assets/img/slides-placeholder-component.png){: .rounded .img-fluid}

The placeholder component has two configuration options: the `Type` and the `Variant`.  

The `Type` is either `Title` or `Text`.  This would correlate to the _reference_ and _text_ of a bible verse or the _verse name_ and _text_ of a song.  For example, for Genesis 1:1, the `Title` would be "Genesis 1:1" and the `Text` would be "In the beginning God created the heaven and the earth."  As a song example, the `Title` might be "Verse 1" and the `Text` would be "Amazing grace how sweet the sound That saved a wretch like me I once was lost but now am found Was blind but now I see".

The `Variant` is one of 6 values.  At this time, Praisenter only uses `Primary` and `Secondary`.  This option represents whether to use the primary language/translation or secondary.  For example, if you want to show the _text_ of Genesis 1:1 from your primary bible, then you would choose `Primary`.  If you want to show the _text_ of Genesis 1:1 from your secondary bible, then you would choose `Secondary`.

Adding multiple placeholder components onto a single slide allows you to build a slide that can show multiple languages at one time.  In the example below, there are three placeholder components, one on the top, one the left, and one on the right.

1. The one on the top is configured with `Type` = `Title` and `Variant` = `Primary` so that it shows the bible reference from the primary bible (KJV in this case).
1. The one on the left is configured with `Type` = `Text` and `Variant` = `Primary` so that it shows the verse text from the primary bible (KJV in this case).
1. The one on the right is configured with `Type` = `Text` and `Variant` = `Secondary` so that it shows the verse text from the secondary bible (one in arabic).

![Slides placeholder component example]({{ page.relpath }}assets/img/slides-placeholder-component-ex.png){: .rounded .img-fluid}

## Date/time component[#](#datetime-component)
The date/time component is a special text component - it shows the current date and time.  You can configure all the properties just like a normal text component, but you cannot modify the text directly.  

![Slides date-time component]({{ page.relpath }}assets/img/slides-datetime-component.png){: .rounded .img-fluid}

Instead of specifying the text, you configure the date-time format.  Praisenter has a list of default formats you can choose from, but you can type in your own format as well.  Here's what each format my look like for the time `2025-11-08 11:40:25 AM EST`:

| Format | Output |
|---|---|
| EEEE MMMM, d yyyy | Saturday November, 8 2025 |
| EEEE MMMM, d yyyy h:mm a | Saturday November, 8 2025 11:40 AM |
| EEEE MMMM, d yyyy h:mm a z | Saturday November, 8 2025 11:40 AM EST |
| EEE MMM, d yyyy | Sat Nov, 8 2025 |
| EEE MMM, d yyyy h:mm a | Sat Nov, 8 2025 11:40 AM |
| EEE MMM, d yyyy h:mm a z | Sat Nov, 8 2025 11:40 AM EST |
| M/d/yyyy | 11/8/2025 |
| M/d/yyyy h:mm a | 11/8/2025 11:40 AM |
| M/d/yyyy h:mm a z | 11/8/2025 11:40 AM EST |
{: .table .w-auto}

You can also type in your own format.  Here are all the options available:

| Option | Description | Output |
|---|---|---|
| G | Era | AD |
| yy | 2-digit year | 25 |
| yyyy | 4-digit year | 2025 |
| M | 2-digit month | 11 |
| MM | 2-digit month (zero padded) | 25 |
| MMM | Abbreviated month name | Nov |
| MMMM | Month name | November |
| d | 2-digit day | 8 |
| dd | 2-digit day (zero padded) | 08 |
| EEE | Abbreviated day name | Sat |
| EEEE | Day name | Saturday |
| a | AM/PM | AM |
| H | 2-digit hour (0-23) | 11 |
| HH | 2-digit hour (0-23, zero padded) (0-23) | 11 |
| h | 2-digit hour (1-12) | 11 |
| hh | 2-digit hour (1-12, zero padded) | 11 |
| m | 2-digit minute | 8 |
| mm | 2-digit minute (zero padded) | 08 |
| s | 2-digit second | 5 |
| ss | 2-digit second (zero padded) | 05 |
| z | Timezone | EST |
| zzzz | Timezone | Eastern Standard Time |
| XXX | Timezone offset from UTC | 5:00 |
| 'any text' | Use single quotes `'` to add text | any text |
| '' | Use two single quotes `''` to output a `'` | ' |
{: .table .w-auto}

Here's a few examples of custom formats for the date/time `2025-11-08 11:40:25 AM EST`:

| Format | Output |
|---|---|
| EEEE MMMM d, yyyy hh:mm a | Saturday November 8, 11:40 AM |
| hh:mm a | 11:40 AM |
| 'Current Time:' hh:mm a | Current Time: 11:40 AM |
| 'It''s' EEEE 'folks!' | It's Saturday folks! |
| hh MMMM:mm yyyy EEEE | 11 November:40 2025 Saturday |
{: .table .w-auto}

## Countdown component[#](#countdown-component)
The countdown component is a lot like the date/time component, but where the date/time component always shows the current date and time, the countdown component _counts down_ to a specific or relative date/time.

![Slides countdown component]({{ page.relpath }}assets/img/slides-countdown-component.png){: .rounded .img-fluid}

The countdown component requires a _target_ date and time to countdown to.  This is great for events that may be upcoming on a specific date.  Just enter the date of the event (you can set the time to 00:00:00 to stop the countdown on the day of) and every time you show the slide, it will be counting down to that date.  No need to adjust the coundown, restart it, etc.

But what if I have a part of my service that we want to show a countdown for every time?  A good example of this is a countdown until 7 PM for when the service beings or a period of meet and greet.  To set a countdown for this use, toggle on the `Time only` setting and set the target time (the target date will be ignored).  Now the countdown component will countdown to the same time every time you show the slide.

Like the date/time component, you can format the output of the countdown component with one of the present formats or with your own.  For example, imagine it's 2025-11-08 12:34 PM and you are counting down to 2025-11-14 4:00 PM:

| Format | Output |
|---|---|
| YY:MM:DD:hh:mm:ss | 00:00:06:03:37:53 |
| MM:DD:hh:mm:ss | 00:06:03:37:53 |
| DD:hh:mm:ss | 06:03:37:53 |
| hh:mm:ss | 03:37:53 |
| mm:ss | 37:53 |
| ss | 53 |
{: .table .w-auto}

You can also type in your own format.  Here are all the options available:

| Option | Description | Output |
|---|---|---|
| Y | 2-digit years | 25 |
| YY | 2-digit years (zero padded) | 25 |
| M | 2-digit months | 11 |
| MM | 2-digit months (zero padded) | 25 |
| D | 2-digit days | 8 |
| DD | 2-digit days (zero padded) | 08 |
| h | 2-digit hours (1-12) | 11 |
| hh | 2-digit hours (1-12, zero padded) | 11 |
| m | 2-digit minutes | 8 |
| mm | 2-digit minutes (zero padded) | 08 |
| s | 2-digit seconds | 5 |
| ss | 2-digit seconds (zero padded) | 05 |
{: .table .w-auto}

> **NOTE**: Custom text is not supported in the countdown formats.  Only the options listed above are supported.

## Media component[#](#media-component)
Media components are used to place pictures, images, video and audio onto a slide.  

> **NOTE**: The _only_ way to add audio-only media to a slide is by using a Media component.  The other media types can be added as backgrounds on all components and slides.

Click the `Browse...` button to select a media item from the Library.  Another way to add a media component is to drag-n-drop a file from your computer onto the slide.  Praisenter will import that file, then create a media component for it.

> **NOTE**: When you drag-n-drop a file onto the slide it could take some time before the media component shows up on the slide - Praisenter has to process and optimize some media files like Video and Audio to ensure they can be played correctly.  Just be patient.

As described in [Slide basics - Media]({{ page.relpath }}pages/slides.html#media), depending on the type of media you add, you can adjust things like scaling, whether mute audio, color adjustments, and more.

## Moving components[#](#moving-components)
Once you add components to the slide, you'll probably want to move them around.  To move a component around, just hover the mouse over the component you want to move and wait for the mouse cursor to change to the Move icon.  Then, click and hold the mouse button while moving the mouse.  Release the mouse button when you are finished moving the component.

## Sizing components[#](#sizing-components)
Like moving components, sizing or resizing components uses the mouse.  In the corners and mid-points of the component you should see small white blocks.  Those white blocks are the sizing controls.  As you hover over a sizing control, the cursor will change to indicate what type of sizing operation it will do.  Then, click and hold the mouse button while moving the mouse to resize the component.  Release the mouse button when you are finished.

![Slides resize component]({{ page.relpath }}assets/img/slides-resize-component.png){: .rounded .img-fluid}

## Snap to grid[#](#snap-to-grid)
When moving and resizing components it's nice to be able to line things up perfectly.  To do that, you can can enable the `Snap to Grid` setting by using the toolbar or the menus.  Once enabled, you should see that resizing and moving components will _snap_ to specific grid points.

> **NOTE**: Unfortunately, Praisenter doesn't show the grid lines at this time.

## Layers[#](#layers)
As you add more components to your slide, they may overlap each other and being able to control what's on top is critical to getting the slide exactly the way you want it.  Praisenter has 4 commands to help with moving components up or down in the layers.

- `Move up` - This will move a component up one layer
- `Move down` - This will move a component down one layer
- `Move front` - This will move the component to the top layer
- `Move back` - This will move the component to the bottom layer

These options are availabe in the `Edit` and context menus and also in the toolbar.

## Copy / cut / paste[#](#copy--cut--paste)
Like with bibles, songs, and everything else, Praisenter supports copy, cut, and paste with slide components.  Just select a component by clicking on it, then copy/cut and paste.  You can paste into the same slide or into other slides.

## Deleting components[#](#deleting-components)
Deleting component is easy - select the component to remove and use the <kbd>Delete</kbd> key.  You can also use the options in the `Edit` and context menus to delete the component.