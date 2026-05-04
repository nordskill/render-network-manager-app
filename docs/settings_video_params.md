# Preview Video Parameters

This field lets advanced users override the default command used to build preview videos.

## When to use it

Use this only if you want custom FFmpeg behavior, such as different encoding options, filters, or output tuning.

For example, to overlay the frame number on each frame of the preview video, you can use:

`-vf "drawtext=text='FRAME = %{n}': start_number=0: x=(w-tw)/2: y=0: fontcolor=white: fontsize=24: box=1: boxcolor=black@0.5: boxborderw=5"`

You can learn more about available parameters in the [FFmpeg documentation](https://ffmpeg.org/ffmpeg.html).

## Good to know

Incorrect values can stop preview video creation from working properly. If preview videos fail after editing this field, clear it and try again.

![Preview Video Parameters setting](images/settings/Preview%20Video%20Parameters.png)
