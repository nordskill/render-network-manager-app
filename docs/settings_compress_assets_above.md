# Compress Scene Assets Above

This setting decides which large assets should be compressed during [Differential Upload](settings_differential_upload.md). Compression can reduce the amount of data you send, which is useful when your scene contains very large textures, caches, or other heavy assets

## How it works

Files larger than the chosen threshold are compressed before upload. Smaller files are sent as they are.

---
### Tradeoff:

Lower thresholds can save more bandwidth, but they also make the app spend more time preparing files before the upload begins. Which may not be convenient when you have thousands of very tiny files like lightweight VDB sequences.

---

![Compress Scene Assets Above setting](images/settings/Compress%20Scene%20Assets%20Above.png)
