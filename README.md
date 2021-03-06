# CoffinLock (Remod original)

Current version 1.0.3 [Download](https://code.remod.org/CoffinLock.cs)

Adds an associated code lock to a deployed coffin (or dropbox).  This feature can be enabled or disabled to facilitate the placement of coffins/dropboxes normally without the lock.  The lock code must be set and the lock locked to lock the coffin.

![](https://i.imgur.com/aupMhSp.jpg)

On first use, the player must enable first via the chat command /cl on.  This setting will remain until the player enters /cl off.  They should only ever have to enable this once.

Coffins and dropboxes are placed normally via the Rust user interface.

When the user attempts to pickup the lock, access will be denied.  However, they can pickup the coffin as they would normally, and the lock will also be removed.   A player cannot pickup a locked coffin.

## Configuration

```json
{
  "Settings": {
    "Admin can bypass lock": false,
    "Owner can bypass lock": false
  }
}
```
- `Admin can bypass lock` - If true, a player with the coffinlock.admin permission can open a coffin/dropbox, even if locked.
- `Owner can bypass lock` - If true, the owner of the locked coffin/dropbox can open it without unlocking first.

## Permissions

- `coffinlock.use` -- Allows player to placed a locked switch
- `coffinlock.admin` -- Allows opening locked coffins/dropboxes.  Can also run the /cl who command to see who owns or placed the coffin/dropbox.

## Chat Commands

- `/cl` -- Display enable/disable status with instructions
- `/cl on` -- Enable locked coffin/dropbox placement (coffin with an associated lock)
- `/cl off` -- Disable locked coffin/dropbox placement (standard behavior without lock)
- `/cl who` -- Allows user with admin permission above to see who owns the coffin/dropbox they are looking at
