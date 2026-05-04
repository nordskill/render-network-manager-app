# Use Staging Folder for Downloads

This option tells the app to download files into a temporary staging area first, and only then move them to the final destination.

## When to use it

This is useful when your final destination is watched by another app, such as Dropbox, OneDrive, Google Drive, or similar sync tools. These services tend to lock files as soon as they appear, which can prevent the app from finishing the download. The staging folder avoids this by moving files to the final location only after they are fully downloaded.

## Tradeoff

You need enough free space for the temporary copy as well as the final destination. If the staging drive is full, downloads can be blocked.

## Good to know

For ordinary local folders, you may not need this. It is mainly a safety option for cloud-synced or automation-heavy workflows.

![Use Staging Folder for Downloads setting](images/settings/Use%20Staging%20Folder%20for%20Downloads.png)
