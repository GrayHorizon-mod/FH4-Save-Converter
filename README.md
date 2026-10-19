# GrayHorizon FH4 Save Converter

Move your **Forza Horizon 4** progress between the **Microsoft Store / Game Pass** version and the **Steam** version,
in either direction. For people who own both versions and want to take their profile across now that FH4 is
delisted.

**Download:** [Releases](../../releases/latest) → `GrayHorizon-FH4SaveConverter-<version>.zip`. Unzip it and run
`FH4SaveConverter.exe`. No install needed.

## Why copying the files doesn't work

Both versions write the same save data, but each encrypts it with its own keys. Copied straight across, the other
version refuses the save with "profile no longer available". This tool decrypts the save with the version it came
from and encrypts it again for the other one.

To do that it runs each version's own save encryption code, taken from the game **while it is running on your PC**.
That copy stays on your PC and runs only inside the tool's built-in emulator. The game is only read: nothing is
written to it or injected into it, and nothing is uploaded.

## What you need

- Both versions at their final versions: Store **1.478.564.2**, Steam **1.478.564.0**.
- The **same Xbox account** signed in on both. FH4 ties your profile to it.
- **Steam → Store:** start the Store version once first and play until it has created and saved a profile.
- **Expansions:** the version you convert *to* needs every expansion your profile has used (LEGO Speed Champions,
  Fortune Island). Otherwise the game quits right after the title screen. If that happens, use
  *Restore a backup...* to put the old save back.

## How to use it

1. **Read both games (once):** start one version, wait for the title screen, then click **Read running game**.
   Quit, and do the same with the other version.
2. **Quit the game.** The tool won't touch a save while FH4 is running.
3. Pick the direction, check the two save folders (found for you, or use **Browse...**), and click **Convert**.
4. Start the other version and load your profile.

## Safety

- The destination save is **backed up in full** before anything is written. **Restore a backup...** puts it back,
  and backs up the current save first, so a restore can be undone too.
- Every source file must pass the game's own integrity check first. Every converted file is decrypted again and
  read back from disk to prove it is correct. If any check fails, nothing is changed, or the backup is put back.
- If Steam Cloud or the Xbox app asks which save to keep afterwards, choose the one on this PC.

## Windows warnings

The exe isn't code-signed, so Windows SmartScreen may say "Windows protected your PC". Click **More info → Run
anyway**. Some antivirus programs flag Python programs packaged like this one by mistake. The SHA-256 of each
release is listed in its release notes, so you can check your download.

## Source code

Coming soon.

---

Not affiliated with Microsoft, Playground Games or Valve. Forza Horizon is a trademark of Microsoft.

GrayHorizon · also see [GrayHorizon VR for Forza Horizon 4/5/6](https://github.com/GrayHorizon-mod/Forza-Horizon-VR)
