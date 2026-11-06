# Bill Walsh College Football '95 Rebalanced

A gameplay patch for **Bill Walsh College Football '95** (Sega Genesis / Mega Drive, USA). It fixes the broken fatigue system, cuts the slowdown on long runs for more explosive plays and breakaway touchdowns, and fixes a kickoff bug after 2-point conversions.

This repository contains BPS patches only, no ROM. You need your own copy of the game.

## Contents

- [Why Bill Walsh '95?](#why-bill-walsh-95)
- [Features](#features)
- [Which patch?](#which-patch)
- [How to patch](#how-to-patch)
- [Game Genie codes (fatigue only, no patching)](#game-genie-codes-fatigue-only-no-patching)
- [Original ROM required](#original-rom-required)
- [Patched ROMs](#patched-roms)
- [Changelog](#changelog)
- [Technical notes](#technical-notes)
- [Testing](#testing)
- [Credits](#credits)

## Why Bill Walsh '95?

In my opinion, Bill Walsh College Football '95 for the Sega Genesis has the greatest gameplay of any 16-bit football game. It has the fun physics and player models of Madden '94, and it introduced windowless passing for the first time in an EA Sports football game. Later games (Madden '95 and College Football USA '96) changed the player models and gameplay significantly and, in my opinion, aren't as fun to play. The only real problem with BW95 was its broken fatigue system, which this mod fixes.

## Features

- **Fatigue fix.** In the original game a running back loses about 27% energy per carry and barely recovers during a drive; only a timeout brings players back. Pick one of two versions (below).
- **More explosive plays.** In the original game a ball carrier starts losing speed right away and is down to lineman speed after a few seconds, so breakaway runs crawl after a few yards. The slowdown on long runs and runs after the catch is now reduced, which allows more explosive plays and breakaway touchdowns. This applies to human- and CPU-controlled teams. The ball carrier keeps full speed for about the first 1.5 seconds, then slows down, faster the more tired he is:

  | Energy (roster screen) | Slowdown after the first 1.5 s |
  |---|---|
  | 90% or higher | about 2/3 as fast as the original game |
  | 75–89% | about 3/4 as fast as the original game |
  | below 75% | same as the original game |

  He also tires during the run, so a long run fades faster toward the end. Fatigue itself builds exactly as in the original game.
- **2-point conversion bug fix.** In the original game, if the defense recovered a fumble on a conversion try, the team that got scored on had to kick off. Now the scoring team kicks off.
- The patched ROMs already have the game's built-in checksum corrected, so they don't need a Game Genie master code.

## Which patch?

Both include every fix above; only the fatigue setting differs.

| Patch | Fatigue |
|---|---|
| `Bill Walsh College Football 95 (USA) [fixed-fatigue] v5.bps` | **Recommended.** Half the original drain per play, 4x faster recovery. Roughly 91% after 1 carry, 83% after 2 straight carries. |
| `Bill Walsh College Football 95 (USA) [no-fatigue] v5.bps` | Energy never drops. |

Timeouts still reset everyone to 100% in both.

## How to patch

1. Get an unmodified USA ROM that matches the checksums under [Original ROM required](#original-rom-required).
2. Download one `.bps` patch and apply it with any BPS patcher:
   - **[Rom Patcher JS](https://www.marcrobledo.com/RomPatcher.js/)** in your browser: choose your ROM, choose the patch, click *Apply patch*, save the result.
   - **[Floating IPS (Flips)](https://github.com/Alcaro/Flips)**: *Apply Patch*, pick the patch, pick your ROM, save.
   - **RetroArch soft-patching** (Genesis Plus GX core): put the `.bps` next to your unzipped ROM and give it the same name, e.g. `Bill Walsh College Football 95 (USA).md` + `Bill Walsh College Football 95 (USA).bps`. RetroArch applies it when the game loads and your ROM file stays unchanged.
3. Always patch the original ROM, not an already patched one. The patcher checks your ROM and refuses a different version.

## Game Genie codes (fatigue only, no patching)

If you only want to remove or fix fatigue, you can use Game Genie codes on the original ROM instead of patching it.

- The codes only change fatigue. They don't include the explosive-plays change or the 2-point conversion fix; for those, use a patch.
- The first code in each line, `RZWB-66VG`, is the master code. It skips the game's checksum check, and the game won't start without it.
- Use them on the unpatched ROM only.

**No fatigue** (2 codes):
```
RZWB-66VG+R17A-N6YY
```

**Fixed fatigue** (5 codes), the same as the `[fixed-fatigue]` patch's fatigue setting:
```
RZWB-66VG+BD7A-NF66+FS7A-NYY8+AD7A-NY7C+JD7T-NH7C
```

- **In RetroArch:** go to *Quick Menu → Cheats*, add a new cheat, paste the whole line (codes joined with `+`) as its code, then enable it and apply the changes.
- **On a real Game Genie:** both lines fit (it holds 5 codes).

## Original ROM required

| | |
|---|---|
| File | `Bill Walsh College Football 95 (USA).md` (No-Intro name; `.bin`/`.gen` are fine too) |
| Size | 2,097,152 bytes (no header) |
| CRC32 | `A582F45A` |
| SHA-1 | `2ae000f45474b3cdedd08eeca7f5e195959ba689` |
| SHA-256 | `81a62d8ac659b1be6572220da7722ff73a55802407742d8e6fef3bcc873b9c20` |

## Patched ROMs

| Patch | CRC32 | SHA-1 | Genesis header checksum |
|---|---|---|---|
| `[fixed-fatigue]` | `9911AB86` | `bef8048a2dca09bd586c0dcd48187ac670e455a8` | `7924` |
| `[no-fatigue]` | `DAE625DA` | `1052120b581ef94c7d0d448d6b95ec3a606cc434` | `343D` |

Patch files:

| File | Size | SHA-256 |
|---|---|---|
| `Bill Walsh College Football 95 (USA) [fixed-fatigue] v5.bps` | 292 bytes | `9f33c9306bfaf6101044b7ec3e4b2cacd2b90976b868c852c7d3d94f6b017fdf` |
| `Bill Walsh College Football 95 (USA) [no-fatigue] v5.bps` | 286 bytes | `f3e249a19c6cd860ed6fc2663490939d2a8862ecf89396ed29af990ac3b3c66d` |

## Changelog

### v5 (2026-11-06), first public release
- Fatigue fix in two versions (fixed, none).
- Reduced slowdown on long runs and runs after the catch (human and CPU teams): 1.5-second burst, then a fade that depends on the runner's energy.
- 2-point conversion turnover kickoff fix.
- Game Genie codes for the fatigue fix (fatigue only).

Versions v1–v4 were private test builds.

## Technical notes

For anyone digging into the ROM (68000 addresses):

- **Fatigue**:
  - AddFatigue (`0x06FA94`) gains are halved (fixed) or disabled (no fatigue).
  - Recovery (`0x06FBA2`) is 4x the original, which subtracted half the elapsed seconds at each snap.
- **Run slowdown**:
  - In the original, a random tick at `0x075EC0` costs the ball carrier 1 speed point plus 10 fatigue while his speed is above 6.
  - The tick is hooked at `0x075EDE`. A snap hook at `0x06FB50` stores the original-game speed in two unused bytes of the player object (`$7E/$7F`), so fatigue builds exactly as before while the actual speed loss follows the table above.
  - Code at `0x1F0100`.
- **2-point fix**:
  - The fumble-recovery code (`0x075AA8`) flips possession even on a try; the interception path already checks for tries.
  - Hooks at `0x06FC38`, `0x06E588` and `0x06E4EC` (code at `0x1F0240`) count possession flips during the try and give the ball back to the scoring team before the kickoff is set up.
- **Checksum**: the EA checksum constant at `0x1E6430` and the Sega header checksum are recomputed.

## Testing

- Play-tested in RetroArch (Genesis Plus GX core).
- Verified with scripted headless runs:
  - Each patch applied to the original ROM reproduces the ROM above byte for byte.
  - Both boot and play.
  - Fatigue numbers are averages of measured carries.
  - The slowdown rule matched on every tick checked, and it also applies to CPU ball carriers (checked in a CPU-vs-CPU game).
- Limits:
  - The 2-point fix was verified by triggering the game's own turnover routine during conversion tries, not with a recorded real fumble.
  - Not tested on real hardware.

## Credits

Created by JD637. Patches made with Floating IPS.

Not affiliated with or endorsed by Electronic Arts. No ROM is included in this repository.
