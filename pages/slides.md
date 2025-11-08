---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Slide basics
date: 2025-11-03 09:48:58 -0500
relpath: ../
---

# Slide basics
> Slides are the backbone of presenting content in Praisenter - you can't present anything without a slide.
{: .p-man-page-intro}

Slides are canvases where you can add content like bible verses, song lyrics and media.  Slides fall into two categories in Praisenter, _slides_ and _slide templates_.  Slides are just what you would imagine, a canvas to place static text and media, very similar to PowerPoint or similar applications.  Slide templates have all the same features as slides, but allow for placeholder content that will be replaced on-the-fly when you are presenting.

> **NOTE**: Praisenter doesn't support import of slides from another application at this time.

A slide is made up of the slide itself and components.  Components are things like blocks of text or images and video.  Slides and components share some common properties like backgrounds, but components have a little more customizability.

For this part of the manual, we'll introduce building blocks of slide editing like understanding opacity and how to choose a color.  Then we'll build on those concepts to introduce things like backrounds and borders.  Finally, we'll end with text editing.

A slide has a few properites that you can configure:
- `Name` - The name of the slide for reference in the library
- `Time` - The time a slide show would stay on this slide before moving onto the next slide.  Not currently used, but will be in the future.
- `Opacity` - How transparent is the slide as a whole.
- `Size` - The target size of the slide - use this to ensure the slide looks exactly they way you want it on the output it will be presented on.
- `Standard size` - An easier way to set the size to a common output size.

Another important property of a slide is the transition - what animation (if any) should be played when changing slides.  Praisenter supports 8 transition animations to choose from and allows you to choose the duration, easing, and easing type of the animation.  The best way to learn how these different settings work is to try them out!

![Slides transition]({{ page.relpath }}assets/img/slides-transition.png){: .rounded .img-fluid}

## Opacity / transparency[#](#opacity--transparency)
Opacity is the measure of how transparent something is.  Here's a good way to think of opacity:
- A wall in your house has an opacity of 100% because you cannot see through it at all, it's completely opaque.
- A window in your house has an opacity of 0% because you can see right through it, it's completely transparent.
- A tinted window on your car has an opacity somewhere between 0% and 100% because you can see through it, but it's _tinted_ or colored.

You can use opacity to achieve blending of content like components, media, and colors.  When making something fully or partially transparent, you will see something like the following.  The checkerboard pattern of grey and white squares show to indicate that the element is partially or completely transparent.

> **NOTE**: Praisenter allows you to create slides that are completely transparent.  The content of that slide will blend with whatever is in the background, whether that be a desktop background, another application, a video playing, and so on.

![Slides transparency]({{ page.relpath }}assets/img/slides-transparency.png){: .rounded .img-fluid}

## Colors[#](#colors)
Many options of a slide involve choosing a color - backgrounds, text color, borders, and so on.  Color is a fundamental element of slide editing so knowning how to select a color is important.  When selecting a color, Praisenter gives you a default palatte of colors to choose from. To choose a color, click on the color you want to use.

You aren't limited to the colors in the default palette.  Click the "Custom Color" link to open the custom color dialog.  The custom color dialog allows you to create your own color in HSB, RGB, or Web mode.  You can also specify the (also known as transparency).  Use the mouse to drag the circle around in the large square on the left to choose the saturation and brightness.  Drag the vertical slider to change the hue.

![Slides color palette]({{ page.relpath }}assets/img/slides-color-palette.png){: .rounded .img-fluid .float-start .pe-4}
![Slides custom color selector]({{ page.relpath }}assets/img/slides-custom-color.png){: .rounded .img-fluid}

## Gradients[#](#gradients)
A gradient is type of coloring that uses two or more colors and blends those colors into each other.  Praisenter supports two-stop linear or radial gradients.  When configuring the gradient you can specify the color locations using the mouse to click and drag the circles in the preview square.  

The `Cycle` option allows you have the gradient repeat.  To see the effect, move one of the circles in the preview square.

The `Offset` controls determine how long to use 100% of the color of the stop before starting to blend.

![Slides gradient selector]({{ page.relpath }}assets/img/slides-gradient.png){: .rounded .img-fluid}

## Media[#](#media)
Media is general term used in Praisenter to group images, pictures, audio, and video.  To use media on a slide, you must _import_ that media first.  To import media drag-n-drop the file onto the Praisenter application or use the `File` -> `Import` menu option.  Some media (audio and video) will be converted to a supported format during the import.  You can see the progress of the import in the bottom bar of the application or on the Tasks tab.

When choosing a media item, you have additional settings depending on the type of media:

| Option | Image | Audio | Video | Notes |
|---|---|---|---|---|
| `Tile image` | ✓ | | | Repeat the image to fill the whole space |
| `Scaling` | ✓ | | ✓ | None (don't change size), stretch, or keep aspect ratio |
| `Adjust color` | ✓ | | ✓ | Adjust the color of the content |
| `Loop?` | | ✓ | ✓ | Whether to restart the media when it finishes playing |
| `Mute?` | | ✓ | ✓ | Whether to mute the audio |
{: .table .w-auto}

### Media - color adjust
Color adjustment is available to both images and video.  This feature allows you to alter the colors of an image on the fly without using an image or video editor.  Want the content darker or lighter?  Use the brightness and contrast sliders.  Found the perfect asset, but you want it green instead of purple?  Use the hue slider.

![Slides color adjust]({{ page.relpath }}assets/img/slides-color-adjust.png){: .rounded .img-fluid}

## Backgrounds / borders[#](#backgrounds--borders)
Both the slide itself and every component supports a background.  Backgrounds are painted under the content.  A background can be None (transparent), a Color, a Gradient, an Image, or a Video.  Slides and components can only have one background.

> **NOTE**: An extremely important point to make is that the background of a slide works a little different than the backgrounds of components when it comes to slide transitions.  When transitioning from one slide to another Praisenter attempts to avoid animating the background of the slide if the two slides have the same background configuration.  Praisenter does NOT do this for components.  A good best practice is to use the background of the slide first before adding a Media component to a slide as the background.

Similarly, both the slide and every component supports borders.  Borders wrap around the edge of the element.  Borders are also available on text.  Borders can be None (no borders), a Color, or a Gradient.  You can adjust the border width, style, and radius.

- `Line cap` - The style of the border when the border ends
- `Line join` - The style of the border when the border turns
- `Dash pattern` - The style of the border lines themselves.  This will scale with the border width.

![Slides border]({{ page.relpath }}assets/img/slides-border.png){: .rounded .img-fluid}

## Shadow / glow[#](#shadow--glow)
Shadow and glow are two sides of the same coin.  They both use a color and spread it from the element outward to transparency.  Shadowns and glow can create the illusion of depth and texture.  When you enable shadow or glow, you can control these properties to produce the effect you are looking for.

> **NOTE**: Only components and text support shadow and glow.

- The Type allows you to create an inner or outer shadow/glow.
- The `X` and `Y` offset determine how far from center
- The Radius controls how far from the element to end
- The Spread controls how much radius will be 100% of the chosen color

![Slides shadow and glow]({{ page.relpath }}assets/img/slides-shadow-glow.png){: .rounded .img-fluid}

## Font / fill / padding[#](#font--fill--padding)
Font formatting should be pretty familiar if you used other word processing applications before.  In Praisenter you can choose the font from the list of all installed fonts on your system.  You can specify the font weight - normal, bold, light, etc. Finally, you can set the style as well - either normal or italic.

> **NOTE**: Not all font weights and styles are supported by every font, so don't be surprised when you choose Italic or Bold and the font doesn't change.

The font size is in points and can be increased and decreased as desired.  The minimum font size is 0.  In addition to changing the font size, you can use the `Font scaling` property to do some really interesting things.

- `None` - Use the font size specified only.  If text spills over the component's bounds, don't do anything.
- `Reduce size only` - Use the font size specified, but reduce it if the text spills over the component's bounds.
- `Best fit` - Use the font size specified, but increase and decrease to fill the component's bounds.

This is extremely useful for placedholder components where you can't predict the size of the content being placed there.  Some bible verses are long and some are short so picking the font size and setting the Font scaling to Reduce size only is a great way to ensure the whole verse always fits on the slide.

> **NOTE**: At this time text formatting is applied to all the text of the component - there isn't a way to style text within a component.

![Slides font]({{ page.relpath }}assets/img/slides-font.png){: .rounded .img-fluid}

For text to be visible, it must be _filled_ or colored.  In Praisenter you can color text using a single color or a gradient.

One last setting for text is padding around it.  When you create a component and fill it with text, the text will fill the whole width and height of the rectangular area.  This may not be desirable if you have a background, borders, or shadow/glow effects.  To make sure there's enough space between those effects and the text, you can increase the padding on each edge of the component to add space between the edges and the text.

![Slides padding]({{ page.relpath }}assets/img/slides-padding.png){: .rounded .img-fluid}
