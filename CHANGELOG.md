# Changelog

## [0.3.2] - 2026-10-27

F4SE package only. The standalone leader pack remains **1.0.0**.

### ✨ Additions

- The log now shows the installed PrismaUI F4 version.
- A warning is written to the log when the installed PrismaUI F4 is older than 2.2.1.2.

### 🔄 Changes

- Works with PrismaUI F4 **2.2.1.2**, now the recommended version.
- The panel does less background work while open.

## [1.0.0] - 2026-10-20 - Leader Pack

Leader Pack **1.0.0** (ESP + Papyrus scripts). First stable Leader Pack release; available on Nexus Mods, GitHub Releases and Bethesda.net (Xbox and PC).

### 🛠️ Fixes

- Vault-Tec Workshop leader setup (Clem, Henry Brown and Overseer Barstow) no longer stacks up running scripts. Every save load restarted the NBL3 quest and launched the setup up to three times at once, and the overlapping calls could pile up in `ApplyVault88LeaderFlags()` and stay active in the save. The setup now runs once per load, skips repeated triggers, and only writes Workshop Framework flags that are not already set.
- Existing saves keep any instances already stuck; no new ones are started after updating.

## [0.3.1] - 2026-10-20

F4SE package. Bundles Leader Pack **1.0.0**; the native module and PrismaUI panel are otherwise unchanged.

### 🛠️ Fixes

- Includes the Leader Pack 1.0.0 fix for stacking Vault-Tec Workshop scripts (`ApplyVault88LeaderFlags()`).

## [Bethesda.net] - 2026-10-12

Leader Pack **0.1.0** only; no version change. The F4SE package is unchanged.

### ✨ Additions

- The Leader Pack (ESP + Papyrus scripts, no F4SE components) is now available on Xbox and PC through [Bethesda.net](https://creations.bethesda.net/en/fallout4/details/02a52796-4dac-4399-8f5a-0016cfe82d2c/Nobody__39_s_Leaders_3).
- The F4SE + PrismaUI package remains PC-only and is distributed only through Nexus Mods and GitHub Releases.

## [0.3.0] - 2026-09-26

F4SE package only. The standalone leader pack remains **0.1.0**.

### 🔄 Changes

- The F4SE module no longer requires the NBL3 plugin to be enabled for the panel to work. The plugin is treated like any other addon or leader pack, and stays independent of the panel.
- An internal timer now improves the fallback to SS2's normal picker when the panel fails, never finishes loading, or another menu is blocking it.

### 🛠️ Fixes

- Fallout 4 **1.10.163** no longer freezes on the main menu.
- Fixed occasion where the desk option was being swallowed once the panel exists, with SS2 only started later on a path that often never ran. If the panel then failed to appear, nothing opened.

## [0.2.1a] - 2026-09-21

### 🛠️ Fixes

- Choosing Assign Leader at the City Planner's Desk no longer crashes the game.

## [0.2.1] - 2026-09-21

F4SE package only. The standalone leader pack remains **0.1.0**.

### 🔄 Changes

- The Panel is now built against **PrismaUI F4 2.1.1**.
- When using a controller, the left-stick now uses Prisma UI's new controller cursor.
- Due to the new left-stick cursor support, controller default sensitivity is now 5 instead of 3.

### 🛠️ Fixes

- Prisma Dock now properly shows NBL3 logo.

## [0.2.0] - 2026-09-09

F4SE package only. The standalone leader pack remains **0.1.0**.

### ✨ Additions

- Added full controller support for the leader panel. Xbox and PlayStation button prompts follow the controller style set in PrismaUI.
- D-pad moves through leader cards and settings. Shoulder buttons jump between search, the list, settings, Assign, and Close. Triggers switch leader packs.
- The left stick moves an on-screen cursor; confirm clicks what is under it or uses the highlighted control. The right stick scrolls the list or settings. Cancel closes the panel.
- Added a Controller cursor speed setting for the left stick. Mouse speed is unchanged.
- NBL3 now appears in the Prisma Dock on the ESC menu, with the Nobody's Leaders 3 badge, a short description, and a link to the Nexus page.

### 🔄 Changes

- Improved titles related to SS2 in the settings box.

## [0.1.0] - 2026-09-06

### ✨ Additions

> These additions represent exclusively what's new in Nobody's Leaders 3 + F4SE module.

- Added an in-game panel for browsing SS2 leader cards and assigning city leaders, replacing SS2 traditional barter menu.
- Added leader trait cards feature Tags with Leader Traits + their respective description, requirement details and settlement assignment information.
- Added support for filtering leaders by leader pack, searching by name or trait, and showing unavailable leaders.
- The panel features Fullscreen and Windowed display modes with layouts that adapt from compact displays through 4K resolutions.
- While the panel replaces SS2's barter menu, in the panel the SS2 barter menu shortcut is available if the user so chooses that method.
- Assigned leaders are marked directly on their cards with the settlement they lead.
- Settlement restrictions are shown on cards when a leader can only lead specific settlements.
- Leader assignment follows SS2's exact normal availability checks and assignment flow.
- Added all SS2 recruitable characters from SS2 + Chapter 2 & Chapter 3.
- Its also possible to reset the Leaders Cache, for ease of use.

> The following changes and fixes represent what has been changed and fixed from the previous version of Nobody's Leaders 2

### ✨ Additions

- The leader pack now registers 146 leader cards (72 Fallout 4 + DLC, 74 SS2), up from 70 in NBL2. No NBL2 leader was removed.
- Added all 74 recruitable SS2 characters from SS2 + Chapter 2 & Chapter 3 (62 Ch1, 7 Ch2, 5 Ch3). NBL2 had no SS2 characters.
- Added Ben Gibson to the leaders list (Preston's Friend).
- Automatron coverage now includes 3 leaders (Ada, Isabel Cruz, Jezebel), up from 2 in NBL2.
- A release validator now checks every build against the reviewed leader roster.

### 🔄 Changes

- All NPCs traits & weaknesses were reviewed and tweaked to better fit the character lore in the game. 61 of the 70 returning Fallout 4 leaders had at least one trait changed.
- Each card now holds at most one major trait, one minor trait and one weakness (NBL2's Dogmeat, Smiling Larry and Anne Hargraves had extras). Every leader has at least one positive (major or minor) trait, and every Fallout 4 leader now has both a minor trait and a weakness.
- Card descriptions now match each card's actual traits and follow one consistent format.
- NBL2 used to replace DLC01MQ05 original quest script to add Isabel Cruz to The Mechanist Lair in order to make her available as a leader, this is no longer the case, NBL3 AddonScript listens for DLC01MQ05 stage 685, the exact “spare the Mechanist” stage for that same purpose.
- Removed both Automatron & Vault-Tec Workshop support ESPs. All required support for both DLCs is now done all through runtime soft-linked scripts in the NBL3 main ESP, which has no DLC masters, so no separate patches are needed.
- NBL3 no longer edits vanilla records (NBL2's main ESP edited 18 vanilla NPCs and 5 cells).
- Quest restart handling is safer, and all scripts are now namespaced under NBL3:.
- The Leader Pack is now versioned separately from the F4SE module.

### 🛠️ Fixes

- Fixed Jezebel was never actually added to NBL2 leaders list (listed in NBL2's changelog but never had a card), she now is correctly added to NBL3 leader list.
- Fixed Preston Garvey and Piper Wright issue that wouldn't allow them to become available as leaders.
- Fixed Sheffield missing barter menu description and typos in his name.
- Fixed Drinkin' Buddy's description missing a line, and 5 cards whose descriptions referred to traits they didn't have.
- Minor other format fixes and tweaks to Leaders descriptions.

### 📑 Google Sheet Changes

- The sheet has been completely overhauled to better fit the new panel theme, and improve its clarity overall.
- All Fallout 4 Characters hyperlinks were moved to Independent Fallout Wiki.
- All SS2 were added to the sheet, and their hyperlinks will go to their Sim Settlements 2 Wiki page.
- Leader Traits and descriptions were moved to the main sheet, from column J1 to column L74
- Added NPC's Sources (base game, dlc and or SS2) and Type.

> The sheet no is no longer attached to Nobody's Leaders 2.