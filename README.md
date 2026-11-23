<p align="center">
  <img src="https://i.postimg.cc/TY2DW6FJ/banner.png" alt="QuickSave Snapshot Vault — Global F5 Quick-Save & F9 Restore Tool for Any PC Game" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-F5%2FF9%20Save%20Snapshot%20Vault-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-quicksave--vault--v1.3-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# QuickSave Snapshot Vault — Global F5 Quick-Save & F9 Restore Tool for Any PC Game

**Playing an Ironman / Permadeath campaign, testing a risky boss build in a Souls-like, or modding a game with only a single autosave slot? Press a global hotkey (F5) to archive your game's save folder into a rolling ZIP vault and restore any snapshot in seconds.**

QuickSave Snapshot Vault brings universal save-state slots to any Windows PC game: **compressing your selected save directory into timestamped `.zip` archives on hotkey press or every N minutes, with audio chime feedback and safe one-click restoration**.

This project is aimed at **Windows 10 and Windows 11 (64-bit) PC gamers** playing single-player RPGs, roguelikes, survival builders, and modded games who want reliable multi-slot save backups.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Game only gives 1 autosave slot that overwrites right before a softlock | Single-slot save design traps players in bugged quests or bad builds | Press `F5` (or `Ctrl+F5`) before major choices to keep 25 rolling `.zip` snapshots |
| Crash during autosave corrupts your 50-hour save file | Abrupt power loss or CTD leaves a `0 KB` truncated save file | Enable **Automatic Timed Snapshots (Every 10 Minutes)** in background |
| Want to practice a specific boss fight repeatedly without running back | Long boss runbacks waste time when learning patterns | Snapshot outside the boss fog gate and restore cleanly from the main menu |
| Restoring a save while the game is loaded in a level fails | Active in-memory level state overwrites disk files on quit | Exit to the game's **Title / Main Menu** before clicking **Restore Snapshot** |

## Download for Windows

[**Download QuickSaveVault.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/QuickSaveVault.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `QuickSaveVault.exe`? (Key features)

- Global customizable hotkey (`Ctrl+F5` default) zips your active game's save folder in under 0.2 seconds with a subtle confirmation chime.
- Optional **Auto-Snapshot Timer** (`Every 5 / 10 / 15 mins`) keeps rolling backups while the game process is running.
- Maintains up to **25 rolling `.zip` snapshots** per game with custom notes (e.g., `'Before Final Boss'`).
- One-click **Restore Selected Snapshot** (with automatic safety backup of current files first).

### Sample Output

```text
[QuickSaveVault] Active Profile: KingdomCome2_Hardcore (Hotkey: Ctrl+F5 | Auto: 10m)
[OK]   Snapshot #14     : Saved 4.2 MB -> Vault\KCD2_2026-11-23_20-14-05.zip (Chime Played)
[INFO] Rolling Vault    : 14 / 25 snapshots stored (Oldest auto-pruned at 25)
```

The release ZIP is named `QuickSaveVault.zip`; the Windows executable inside is named `QuickSaveVault.exe`.

1. Close QuickSave Vault before updating or replacing executable files.
2. Click **Download QuickSaveVault.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `QuickSaveVault.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit).

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `QuickSaveVault.exe` runs locally without uploading your personal files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Instant multi-slot save history for single-slot games

Turns any single-save game into a 25-slot quicksave vault.

### Protection against save-file corruption on crashes

Timed background snapshots ensure you never lose more than a few minutes of progress.

### Custom labels on milestone saves

Rename any snapshot (`'Act 2 Start'`, `'Pre-Respec'`) so you always know which slot to load.

### 100% local `.zip` archives

Standard ZIP files you can keep forever or copy to another PC.

## Default folders and configuration paths

QuickSave Vault stores compressed `.zip` save snapshots in `Documents\QuickSaveVault`:

```text
%USERPROFILE%\Documents\QuickSaveVault\
```

Typical directory layout:

```text
%USERPROFILE%\Documents\QuickSaveVault\
└── <GameProfile>\
    ├── 2026-11-23_20-10-00_Auto.zip
    └── 2026-11-23_20-14-05_Manual.zip
```

Always exit to the game's **Main Menu** (or close the game) before restoring a snapshot so the game reloads the restored files from disk cleanly.

## Quick start guide

Follow these steps to get started:

1. **Extract `QuickSaveVault.zip` and launch `QuickSaveVault.exe`.** Click **+ Add Game** and select your game's save folder.
2. **Configure your **Manual Snapshot Hotkey** (`Ctrl+F5`) and optional **Auto-Backup Interval**.** Play your game normally and press `Ctrl+F5` before major moments.
3. **To restore a snapshot, exit to the game's **Main Menu**, select the snapshot in QuickSave Vault, and click **Restore**.** Click Load / Continue in-game.

### Data safety note

QuickSave Vault automatically backs up your current save folder before overwriting it during a restore.

## What the status summary shows

QuickSave Vault displays **active game profile, save folder path, snapshot count, hotkey binding, and auto-backup timer**.

## FAQ

**Should I restore a save while actively standing inside a level in-game?**

No—exit to the game's Main Menu (or desktop) first so the game reads the restored save files cleanly when you click Load.

**Does QuickSave Vault slow down my game when taking a snapshot?**

No—zipping typical 1 MB–20 MB save folders takes under 150 milliseconds in a background thread.

**Can I use it for any PC game?**

Yes—any game that stores saves in a local Windows folder (`AppData`, `Documents`, `Saved Games`, or Steam `userdata`).

## Useful reading

- [PCGamingWiki — Save Game Data Locations Index](https://www.pcgamingwiki.com/wiki/Glossary:Game_data)

## More Windows Gaming Utilities

- [CloudSave-UniversalGameSync](../CloudSave-UniversalGameSync) — Automatic save folder synchronizer for non-Steam Cloud games
- [EldenRing-FPSUltrawideUnlocker](../EldenRing-FPSUltrawideUnlocker) — ELDEN RING offline 120+ FPS unlocker, 21:9 fix & save backup
- [BG3-ModPakLoadOrderSorter](../BG3-ModPakLoadOrderSorter) — Baldur's Gate 3 .pak mod load order & modsettings.lsx sorter
- [DiskMap-FastStorageAnalyzer](../DiskMap-FastStorageAnalyzer) — 3-second NTFS MFT disk space analyzer & large file finder

*Independent open-source desktop utility for Windows.*
