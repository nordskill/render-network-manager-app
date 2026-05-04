# Differential Scene Upload

Differential Upload is a smarter way to send scenes to the Render Network. It uploads only new or changed assets from your project folder, skipping everything that was already uploaded before. This saves a lot of time and bandwidth, especially for repeat uploads, versioned shots, and scenes with many large reusable assets.

For a detailed explanation of how Differential Upload works, see the [Differential Upload guide](differential_upload_guide.md).

## Good to know

Differential Upload uses local [cache](settings_cache_folder.md) space while preparing files. If you plan to use it regularly, make sure your cache drive has enough free space. For ORBX scenes, you also need to set the [Path to Octane Standalone](settings_path_to_standalone.md).

![Differential Scene Upload setting](images/settings/Differential%20Scene%20Upload.png)
