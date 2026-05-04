# Compress ORBX Files Before Upload

This option tells the app to compress ORBX files before sending them to the Render Network. Compression can reduce upload size, which may help if your internet connection is limited or your ORBX files are very large.

The app uses LZ4, one of the fastest compression algorithms available, so the extra step before upload takes very little time, even for scenes that are tens of gigabytes in size.

If you work with large scene files, we strongly recommend using [Differential Upload](settings_differential_upload.md) instead — it only uploads new or changed assets, which saves even more time and bandwidth.

![Compress ORBX Files Before Upload setting](images/settings/Compress%20ORBX%20Files%20Before%20Upload.png)
