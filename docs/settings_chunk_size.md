# Chunk Size

Large uploads are split into smaller parts, called chunks. This setting controls how large each part should be.

Chunk size affects upload behavior:

- smaller chunks can be more stable on weak or inconsistent connections
- larger chunks can be more efficient on a fast, stable connection

## How to choose a value

If uploads are failing or stalling often, try lowering the value.
If your connection is strong and stable, you can keep it higher to avoid unnecessary extra work.

---
## Good to know

This is an advanced setting. The default value is a good starting point for most users.

---

![Chunk Size setting](images/settings/Chunk%20Size.png)
