# Miscellaneous
> Praisenter has a set of default behaviors that can be changed (called Settings) and provides some feedback on actions being performed that you can send/use for troubleshooting issues.
{: .p-man-page-intro}

Praisenter's default settings were chosen based on testing, experience, and most common usecase. You can change the behavior of the application using the settings and we'll walk you through each one below.  All settings are saved with the workspace, so each workspace can have different behavior.

> **NOTE**: Some settings are best left alone unless you really know what you are doing.  We'll call those out when we come to them.

![Miscellaneous settings]({{ page.relpath }}assets/img/misc-settings.png){: .rounded .img-fluid}

## General settings[#](#general-settings)
These settings apply to the application.  Currently there are a few options: `Theme`, `Accent color`, `Language`, and `Debug Mode Enabled`.  We'll walk through each one separately.

![Miscellaneous general settings]({{ page.relpath }}assets/img/misc-settings-general.png){: .rounded .img-fluid}

The `Theme` setting is used to change how you want Praisenter to look.  There are few themes available to choose from, each one having a light and dark mode.  Praisenter's default is `Primer Dark`.  We chose this to avoid eye strain and to reduce ambient light from the application.

> **NOTE**:  The `Reload styles` button is there for users who are brave enough to alter how Praisenter looks.  Praisenter is styled using a CSS-like language.  Clicking the button on accident has no effect, so don't worry if you don't want to use this feature.

The `Accent color` setting is used to highlight various elements within the application and draw your attention.  We recognize that some users may be color blind and using a fixed accent color could limit use.  Try the different accents and use whichever works best for you.  Currently, we offer `Blue`, `Purple`, `Pink`, `Orange`, `Green`, and `Yellow` accent colors.

The `Language` setting is used change the language of the Praisenter.  Today, Praisenter is distributed in English only, but with enough knowledge you can add your own translations.

> **NOTE**: To add your own translations, find the .Praisenter3 folder on your system and open the `locales` folder.  There's a `messages.properties` file there with all the English text that the application uses.  If you copy that document and translate the text after the `=` signs and place that file here, you can load it and run Praisenter in a different language.

The `Debug Mode Enable` setting allows you to get more feedback from the application as you are using it for troubleshooting.  For example, let's say you are having trouble importing a file or presenting a slide, turn this setting on to allow Praisenter to output more detail to the logs.  Then, upload or copy those logs in your error report.

## Slide settings[#](#slide-settings)
There are two settings for slide display.  These settings effect how slides are transitioned between each other when you are presenting slides to a display.

![Miscellaneous slide settings]({{ page.relpath }}assets/img/misc-settings-slide.png){: .rounded .img-fluid}

The `Wait for In-Progress Transitions to Complete` setting is used to control what you want to happen when you send slides to a display very quickly.  For example, imagine this scenario:

- You click the `Show` button to show `Slide A`.  Slide A has a slide transition that takes 5 seconds to complete
- You realize you didn't want to show Slide A, but instead want to show Slide B
- You click the `Show` button to show `Slide B`.  If the transition of Slide A hasn't completely finished, what should Praisenter do?

This setting has two options, either wait for Slide A's transition to complete, then show Slide B OR immediately stop Slide A's transition and start showing Slide B.  By default, Praisenter will stop Slide A and start showing Slide B.

The `Placeholder Transition Behavior` setting is used to control how placeholders, content, and the background of slides are transitioned when those slides include [placeholder components]({{ page.relpath }}{{ page.slidecomponents_page }}#placeholder-component).  For example, imagine this scenario:

You are showing a Bible verse using Slide A.  Slide A has placeholder components for the verse Reference and the verse Text.  It also has a video background and maybe one other _static_ component like an image or icon.  When you try to show the _next verse_, Praisenter has to decided _what_ to transition.  For example, should it stop the video background and slide in a new version of Slide A where the video has restarted?  Should Praisenter only swap out the placeholders or should it also swap out the image/icon?

That's where this setting comes in.  The behavior of each option is described below referencing the example described above:

- `Placeholders only` - Only the Bible reference and text are transitioned.  The video background stays where it is and continues to play.  The image/icon will stay where it is as well.
- `All content` - The Bible reference and text are transitioned, but the image/icon is as well.  However, the video background stays where it is and continues to play.
- `Entire slide` - Everything transitions, as if it was an entirely different slide.  The video will be stopped and restarted.

## Bible settings[#](#bible-settings)
The settings in this section control whether a confirmation window is shown when you use the `Sort by number` and `Number by order` features.  You are asked in the application if you want to see these confirmations in the future and you can come here to re-enable them if you find the confirmation a good way to avoid performing these commands accidentally.

![Miscellaneous bible settings]({{ page.relpath }}assets/img/misc-settings-bible.png){: .rounded .img-fluid}

## Media settings[#](#media-settings)
These settings apply to different types of media.  As of 3.1.7, these settings only apply to media with audio (audio and video).  These settings are here to help adjust the volume of audio and video files during the _import_ process.  Praisenter will use [FFmpeg](https://ffmpeg.org/) to detect the `mean_volume` and then adjust the volume during transcoding to the given target volume (in dB).  The volume adjustment will only happen if the `mean_volume` is greater than the target volume.

If you find you are having issues with volume, try turning this feature off and re-importing the media.

![Miscellaneous media settings]({{ page.relpath }}assets/img/misc-settings-media.png){: .rounded .img-fluid}

## Audio settings[#](#audio-settings)
These settings only apply to _Audio_ media.  While presenting audio-only media is rare (there are many other ways to play audio media outside of Praisenter that give you far better control), Praisenter does support audio playback.  Similarly to Video media, Praisenter will _transcode_ the audio file to a supported format during import.  The settings below control this behavior.

> **NOTE**: Praisenter supports many, many audio formats. It does this by _transcoding_ the format supplied into a standard format that Praisenter can natively play.  Praisenter natively supports the formats [listed here](https://openjfx.io/javadoc/25/javafx.media/javafx/scene/media/package-summary.html).

![Miscellaneous audio settings]({{ page.relpath }}assets/img/misc-settings-audio.png){: .rounded .img-fluid}

- `Transcode Audio` - You can turn off transcoding, but be aware that Praisenter doesn't support all audio formats.
- `Audio File Transcode Extension` - This setting is here if you have issues with transcoding to the Praisenter default format `m4a`.  Again, be careful what you change here - Praisenter doesn't support all audio formats.
- `Audio File Transcode Command` - This setting is here if you have knowledge of transcoding and [FFmpeg](https://ffmpeg.org/) and would like to alter how Praisenter transcodes the audio during import.

> **NOTE**: These settings are pretty dangerous so be very careful when changing these.  If you find you've messed something up or things are importing correctly, just revert to the defaults:

| Setting | Default Value |
|---|---|
| Audio File Transcode Extension | `m4a` |
| Audio File Transcode Command | `{ffmpeg} -v fatal -i {source} -y -ignore_unknown {volumeadjust} {target}` |
{: .table .w-auto}

## Video settings[#](#video-settings)
These settings only apply to _Video_ media.  During import of video media, Praisenter will _transcode_ the video file to a supported format to ensure the best video playback when used.  The settings below control this behavior.

> **NOTE**: Praisenter supports many, many video formats. It does this by _transcoding_ the format supplied into a standard format that Praisenter can natively play.  Praisenter natively supports the formats [listed here](https://openjfx.io/javadoc/25/javafx.media/javafx/scene/media/package-summary.html).

![Miscellaneous video settings]({{ page.relpath }}assets/img/misc-settings-video.png){: .rounded .img-fluid}

- `Transcode Video` - You can turn off transcoding, but be aware that Praisenter doesn't support all video formats.
- `Video File Transcode Extension` - This setting is here if you have issues with transcoding to the Praisenter default format `mp4`.  Again, be careful what you change here - Praisenter doesn't support all video formats.
- `Video File Transcode Command` - This setting is here if you have knowledge of transcoding and [FFmpeg](https://ffmpeg.org/) and would like to alter how Praisenter transcodes the video during import.
- `Video Thumbnail Extract Command` - When importing a video file, Praisenter will extract one frame from the video to use for as thumbnail and for previewing the video without playing it.  This setting can be used to adjust the [FFmpeg](https://ffmpeg.org/) command that is used to perform this task.

> **NOTE**: These settings are pretty dangerous so be very careful when changing these.  If you find you've messed something up or things are importing correctly, just revert to the defaults:

| Setting | Default Value |
|---|---|
| Audio File Transcode Extension | `mp4` |
| Audio File Transcode Command | `{ffmpeg} -v fatal -i {source} -y -ignore_unknown {volumeadjust} {target}` |
| Video Thumbnail Extract Command | `{ffmpeg} -v fatal -i {media} -vf fps=2 -frames:v 10 -vsync vfr {frame}` |
{: .table .w-auto}

## NDI® settings[#](#ndi-settings)
[NDI®](https://ndi.video/) stands for Network Device Interface, a software standard for transmitting video and audio over an IP network. This is especially useful for sending content to another application like [OBS](https://obsproject.com/) to combine, overlay, merge, etc. different content into a single or multiple displays.  Praisenter allows you to create NDI® displays and have content sent there. 

![Miscellaneous NDI settings]({{ page.relpath }}assets/img/misc-settings-ndi.png){: .rounded .img-fluid}

When you setup an [NDI®](https://ndi.video/) display you specify the frames per second for that display.  That setting defines the number of frames per second to _capture_.  The setting here is how many frames to _send_.  This setting needs to be set higher than the setting at the display level.  Adusting this setting can have a performance impact and the default value of `60` is usually the best balance of performance and quality.

The `Enable Render Optimizations` setting is here to control whether Praisenter performs render optimizations or not.  With this setting enabled, Praisenter will analyze the currently presenting content on the [NDI®](https://ndi.video/) display and determine whether it can skip _capturing_ of frames.  Praisenter will detect situations that require frames to be captured, when playing a video or a slide transitioning in or out, and situtations where the content is not changing like an image or text only slide.  This can have a large positive impact on performance so leaving it on is recommended, but you can disable this optimization if you are having trouble.

## Zoom[#](#zoom)
Under the `Window` menu, there are a few options for `Zoom`.  The zoom feature in Praisenter controls how small or big you want the application text, icons, buttons, spacing, and so on.  This can be helpful to fit more on your screen (by zooming out) or to make buttons and other interaction elements bigger for better visibility or touch screen use (by zooming in).  You can reset the zoom to the default using the `Reset Zoom` menu item.

![Miscellaneous zoom]({{ page.relpath }}assets/img/misc-zoom.png){: .rounded .img-fluid}

## Task log[#](#task-log)
As you are performing actions in Praisenter, some of those actions will be collected and reported in the `Task Log`.  The Task Log can give you feedback on any action you may have taken in the past or any actions that are currently pending.  A good example of this is audio / video imports - they can take a long time (a few minutes or more in some cases) and having some feedback that it's still in progress is important.  

![Miscellaneous task log]({{ page.relpath }}assets/img/misc-task-log.png){: .rounded .img-fluid}

The log will track a few key data points:

- `Name` - This can be anything that describes the task that occurred.
- `Operation` - This is the type of action that was performed.  Save, Import, etc.
- `Type` - This is the type of item the task operated on.  Bible, Song Lyrics, etc. or the mimetype of the file.
- `Status` - This is the current status / final status of the task.  There are only three options: In Progress, Success, or Failed.
- `Duration` - This is how long the task took to complete.
- `Description` - This is the friendly message for the operation.  Something like "Saving TEST Bible".
- `Error Message` - This is the error that occurred when the operation failed.

If a task fails, you should see a copy button.  You can use this button to copy the error message to report on the Praisenter discussions board.

![Miscellaneous task log]({{ page.relpath }}assets/img/misc-task-log-error.png){: .rounded .img-fluid}

> **NOTE**: The information stored in the Task Log is not saved and will be cleared when you close Praisenter.

## Log files[#](#log-files)
Under the `Help` menu item there are two options for logs: `Application Logs` and `Workspace Logs`.  These options will open a File Explorer window to where the log files are stored.  If you are having trouble with Praisenter, these file may contain more information about the issue and would be crucial to share when reporting an issue.

![Miscellaneous log files]({{ page.relpath }}assets/img/misc-help.png){: .rounded .img-fluid}

## Check for update[#](#check-for-update)
Found in the `Help` menu, the `Check for Update` option allows you to see if you have the latest version of Praisenter or not.  You must have internet connectivity for the check to succeed.  If installed Praisenter from the [Microsoft Store](https://apps.microsoft.com/detail/Praisenter/9PHHWB94W800?launch=true&mode=mini) or [Snap Store](https://snapcraft.io/praisenter), then you should always have the latest version, provided you have internet connectivity.  If you installed Praisenter manually using an MSI or DEB, then you will need to make sure you re-install to get the latest features and fixes.

![Miscellaneous check for update]({{ page.relpath }}assets/img/misc-check-for-update.png){: .rounded .img-fluid}

## About[#](#about)
The `About` menu under `Help` provides a little more detail on the version of Praisenter you have.  These details can be helpful when reporting an issue.

![Miscellaneous about]({{ page.relpath }}assets/img/misc-about.png){: .rounded .img-fluid}