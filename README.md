# Bill Walsh College Football '95 Elevated

A mod for **Bill Walsh College Football '95** (Sega Genesis / Mega Drive). It keeps everything that made the original fun to play, fixes its bugs, and adds subtle gameplay tweaks, more plays, a smarter CPU, and new controls that put the 6-button gamepad’s X, Y and Z buttons to use for the first time. It comes in two editions: the **1994 Season Edition** with **all 107 Division I-A teams of 1994** and the 19 real bowl games, and the **2026 Season Edition** with **all 138 FBS teams of 2026** and the College Football Playoff. Both have real player names, 32 historic teams and Dynasty support.

**[Download the latest release here →](https://github.com/jd6-37/Bill-Walsh-CFB-95-Elevated/releases/latest)** (scroll down to the Assets section)

<img width="400" height="280" alt="Title screen, 1994 Season Edition" src="images/title_1994_season.png" /> <img width="400" height="280" alt="Title screen, 2026 Season Edition" src="images/title_2026_season.png" />

- **Fixed fatigue system!** Every player tires from what he does on the field and recovers between plays. In the original game, ball carriers tired extremely quickly and barely recovered during a drive, so after one or two carries your best players were essentially unusable for the rest of the drive unless you called a timeout. This fix is why the mod was started, and on its own it drastically improves the game.
- **The original game's bugs, fixed:** the wrong team kicking off after a 2-point try turnover, pitches that land behind fast backs, and a season sim that reads offense and defense backwards.
- **More explosive plays:** ball carriers keep their speed longer on long runs and runs after the catch, so breakaway plays happen more often.
- **Two Season Editions:** all 107 I-A teams of 1994 with their conferences, the real 1994 schedule, the SEC Championship Game and the 19 bowls; or all 138 FBS teams of 2026 with 2026 rosters and conferences, random or real 2026 schedules, conference title games and a 12-team College Football Playoff (or 24, 4, BCS 2 or none).
- **32 historic teams** in both editions, from Alabama '78 to Indiana '25, with their era's art and real rosters (Exhibition).
- **Real player names, impact players and milestones**, ratings in single points instead of 16 big steps, and **Dynasty support** through the Dynasty app.
- **More plays and pre-snap control:** 67 plays from College Football USA '97 (the original game has 96 offensive plays), eight new formations with 100 more plays, two all-new plays (RPO and HB SWING), speed options, a Flip Play tile, pre-snap motion, hot routes, flipping plays at the line, and defensive alignment shifts.
- **6-button gamepad support:** true 5-receiver passing with the X and Y buttons, hot routes, flips and shifts at the line, a truck button, and pre-snap views of the play art, routes, assignments and energy bars. With a 3-button gamepad the game plays as before.
- **A smarter CPU:** four difficulty levels, more and smarter CPU audibles, more aggressive 4th downs, smarter defenses, and more.
- **2026 rules** in the 2026 Season Edition: the two-minute timeout, today's clock rules and today's overtime.
- **Quality-of-life improvements:** alternate uniforms, faster kickoff setups after scores, team OFF/DEF ratings on Game Setup, Team Rosters from Game Setup, whole-play replays, menu music on or off with X, and more.

This repository contains BPS patches only, no ROM. You need your own copy of the game.


## Contents

- [Why Bill Walsh '95?](#why-bill-walsh-95)
- [Which patch?](#which-patch)
- [Features](#features)
- [Controls](#controls)
- [How to patch](#how-to-patch)
- [Game Genie codes (fatigue only, no patching)](#game-genie-codes-fatigue-only-no-patching)
- [Original ROM required](#original-rom-required)
- [Patched ROMs](#patched-roms)
- [Changelog](#changelog)
- [Technical notes](#technical-notes)
- [Testing](#testing)
- [Credits](#credits)

## Why Bill Walsh '95?

In my opinion, Bill Walsh College Football '95 for the Sega Genesis has the greatest gameplay of any 16-bit football game. It has the fun physics and player models of Madden '94, and it introduced windowless passing for the first time in an EA Sports football game. Later games (Madden '95 and College Football USA '96) changed the player models and gameplay significantly and, in my opinion, aren't as fun to play. The biggest problem with BW95 was its broken fatigue system, which this mod fixes, along with the game's other bugs. It also adds the plays, controls, CPU smarts and teams the game was missing.

## Which patch?

| Patch | What you get |
|---|---|
| `Bill_Walsh_College_Football_95_Elevated_1994_Season_v2_1_0.bps` | **Elevated: 1994 Season Edition.** Every feature below except the 2026 rules, with all 107 I-A teams of 1994, their rosters and conferences, and the 19 bowls. Title screen: ELEVATED, 1994 Season Ed. A 4 MB ROM with 32 KB of save RAM (see [Saves](#saves)). Replaces v2.0.0's 36-team `Elevated` patch. |
| `Bill_Walsh_College_Football_95_Elevated_2026_Season_v2_1_0.bps` | **Elevated: 2026 Season Edition.** Every feature below, with all 138 FBS teams with 2026 rosters and conferences, and the College Football Playoff. Title screen: ELEVATED, 2026 Season Ed. A 4 MB ROM with 32 KB of save RAM (see [Saves](#saves)). |
| `Bill_Walsh_College_Football_95_Fixed_Fatigue_Fixes_v2_1_0.bps` | The fatigue fix and fixes for the original game's bugs (2-point try kickoff, pitches to fast backs, season sim). No other gameplay changes. Original title screen. |
| `Bill_Walsh_College_Football_95_Fixed_Fatigue_v2_1_0.bps` | Only the fatigue fix. Original title screen. |
| `Bill_Walsh_College_Football_95_No_Fatigue_v2_1_0.bps` | Only one change: energy never drops. Original title screen. |

The patches are in the [`patches`](patches) folder. Both Elevated editions use Fixed Fatigue. Patches for older versions are attached to their [releases](https://github.com/jd6-37/Bill-Walsh-CFB-95-Elevated/releases).

## Features

The original-game fixes below are in the patches as shown in their table. Everything else is in both Elevated editions, except where a section says it's for one edition.

### Original-game fixes

| Fix | Elevated editions | Fixed Fatigue + Fixes | Fixed Fatigue |
|---|:-:|:-:|:-:|
| [Fatigue](#fatigue) | ✓ | ✓ | ✓ |
| [Wrong team kicks off after a 2-point try turnover](#2-point-conversion-kickoff) | ✓ | ✓ | |
| [Pitches land behind fast backs](#pitches-to-fast-backs) | ✓ | ✓ | |
| [Season sim reads offense and defense backwards](#season-sim) | ✓ | ✓ | |

#### Fatigue

**Everyone tires, from what he does on the field.** In the original game a running back loses about 27% energy per carry and barely recovers during a drive; only a timeout brings players back. Now every player's energy drops with what he does while the play is live: the distance he runs, the time he's locked in a block, and hits. Everyone recovers a quarter of his fatigue at each snap, and timeouts and halftime still reset everyone to 100%.

#### 2-point conversion kickoff

In the original game, if the defense recovered a fumble on a conversion try, the team that got scored on had to kick off. Now the scoring team kicks off.

#### Pitches to fast backs

The game aims a pitch where the back will be if he keeps his speed. On the option the back is held to the QB's pace until the pitch and then speeds up, so a fast back ran past the ball and it landed behind him. Now the pitch is re-aimed in flight at where the back will be when it comes down, with the same flight time and arc. Fast backs are no longer a problem on the option and toss plays.

#### Season sim

When the original game simulated CPU-vs-CPU season games, it read each team's offense and defense ratings backwards, so a great defense scored points and a great offense kept the other team's score down. Fixed in the Elevated editions and Fixed Fatigue + Fixes.

### More explosive plays

In the original game a ball carrier starts losing speed right away and is down to lineman speed after a few seconds, so breakaway runs crawl after a few yards. Some slowdown is part of the game's design, but it's too much. The Elevated editions reduce it on long runs and runs after the catch, for human- and CPU-controlled teams, so explosive plays happen more often. The ball carrier keeps full speed for about the first 1.5 seconds, then slows down, faster the more tired he is:

| Energy (roster screen) | Slowdown after the first 1.5 s |
|---|---|
| 90% or higher | about 2/3 as fast as the original game |
| 75–89% | about 3/4 as fast as the original game |
| below 75% | same as the original game |

### 1994 Season Edition with all 107 I-A teams

- **All 107 Division I-A teams of 1994:** the original game's 36 plus 71 more (from College Football USA '97, and Pacific). On Game Setup the teams are in alphabetical order; hold left or right to scroll fast.
- **1994 conferences:** SEC, Big Ten, Pac-10, Big Eight, SWC, ACC, Big East, WAC, Big West, MAC and the Independents.
- **1994 rosters:** the original game's rosters for its 36 teams, and rosters for the 71 new teams built from 1994 research (preseason magazines such as Athlon, Lindy's and The Sporting News' 1994 yearbook, StatMuse and sports-reference). Real names for 2,962 of the 3,424 players. Team OFF/DEF ratings come from the rosters.
- **The real 1994 preseason AP poll** starts every new season.

### 2026 Season Edition with all 138 FBS teams

<img width="800" alt="All 138 FBS teams: the 28 with new helmets, logos, wordmarks and uniforms, plus all 110 teams from College Football USA '97" src="images/new_teams_2026.png" />

- **All 138 FBS teams of 2026:** the 110 teams from College Football USA '97, and 28 more with new helmets, logos, wordmarks and uniforms made for this mod (above). On Game Setup the teams are in alphabetical order; hold left or right to scroll fast.
- **2026 conferences:** SEC (16 teams), Big Ten (18), ACC (17), Big 12 (16), American (14), Sun Belt (14), MAC (13), Mountain West (10), Conference USA (10), Pac-12 (8) and the Independents (Notre Dame, UConn).

  <img width="400" height="280" alt="Rankings: SEC standings after a simulated season" src="images/conferences_2026.png" />

- **2026 rosters with real names**, converted from EA Sports College Football 27's player ratings (Week 9 update), and CPU offense and defense styles that follow each team's 2026 scheme.
- **Team ratings from the 2026 rosters:** OFF/DEF ratings on Game Setup and Team Schedules, also used by the season sim.
- **Preseason Walsh Reports for all 138 teams**, written for 2026.
- **The real 2026 preseason AP poll** starts every new season.
- **New title art:** Malachi Toney of Miami replaces Bill Walsh's portrait.

#### 2026 rules

- **Two-minute timeout:** at 2:00 of the 2nd and 4th quarters the game stops (at once when the teams are at the line, after the play otherwise): "TWO-MINUTE TIMEOUT!", both teams go back to the play-call screen, the play clock starts over, and players get some energy back. No team's timeout is charged.
- **The clock keeps running** after first downs and after a runner goes out of bounds (until the teams line up), except in the last 2:00 of a half. A team can't call two timeouts in a row before a snap. The game clock runs about 4% slower, so games keep about as many plays.
- **Overtime as today:** every tied game goes to overtime. Each team gets a possession from the opponent's 25; from the 2nd overtime a touchdown must be followed by a two-point try, and from the 3rd the teams alternate two-point tries.

### Season mode

- **Game Setup**, Play Mode *New Season*:
  - **Schedule:** *Random* (each conference's games plus random non-conference games, dealt again every season: 11 weeks in 1994, 12 in 2026) or the real schedule (*Real 1994*: Week 0 to Week 13; *Real 2026* from Week 0). Games against I-AA / FCS teams become byes.
  - **Postseason:** 1994: *Bowls* (default) or *None*. 2026: *CFP 12* (default), *CFP 24*, *CFP 4*, *BCS 2* or *None*.

  <img width="400" height="280" alt="Game Setup for a new season: Schedule and Postseason rows" src="images/season_setup_2026.png" />

- **1994 bowls:** the 19 bowls of the 1994 season with their real tie-ins: the Rose (Big Ten and Pac-10 champions), the Bowl Coalition's Orange, Sugar, Cotton and Fiesta, and conference slots for the rest; a team needs 6 wins. Each bowl's name shows on the Week Schedule. No team finishes the season ranked above the team that beat it in its bowl.
- **Conference title games:** 1994 has the SEC Championship Game (East vs West), as in 1994. In 2026 every conference except the Independents has one (every Postseason setting except None): the top two by conference record (then overall record, then rank) meet at the first team's home. Title games count like regular-season games in the rankings.
- **2026 playoff formats:**

  | Postseason | Field |
  |---|---|
  | CFP 12 | The 2026 rules: the ACC, Big Ten, Big 12 and SEC champions, the best-ranked champion of the other conferences, Notre Dame if it's in the top 12, and the highest-ranked other teams. Seeded by rank; seeds 1-4 get a bye, first-round games are at the higher seed. |
  | CFP 24 | The four champions above, the best-ranked champion of the other conferences, and 19 more teams by rank. |
  | CFP 4 | The top 4 in the rankings: semifinals 1 vs 4 and 2 vs 3, then the final. |
  | BCS 2 | The top 2 in the rankings meet in the BCS National Championship. |
  | None | Regular season only. |

  In the final rankings, no playoff loser stays ahead of the team that beat it.
- **Season screens** (Start on the Week Schedule):
  - **Week Schedule:** one week at a time. *Play Week* simulates every CPU game of the week.
  - **Team Schedules:** any team's schedule, results and OFF/DEF ratings. C sets all of its games to HOLD (you play them) or CPU and makes it one of your teams, so its postseason games start on HOLD.
  - **Rankings:** the Top 25 and every conference's standings.
  - **CFP Bracket** (2026), during the playoff.
  - **Season Stats, Team Stats and Team Rosters** over every team.

  <img width="400" height="280" alt="Week Schedule: CFP First Round" src="images/week_schedule_2026.png" /> <img width="400" height="280" alt="Rankings: Top 25" src="images/rankings_2026.png" />
  <img width="400" height="280" alt="Team Schedules: a season's results with OFF and DEF ratings" src="images/team_schedule_2026.png" /> <img width="400" height="280" alt="CFP Bracket: 12 teams, seeds 1-4 with a bye" src="images/cfp_bracket_2026.png" />

- **Top 25 ranks in games:** "#5 Georgia" in the score box and the timeout box (a short name when it's too wide, e.g. "#22 FSU"), "#5" under the team on the controller select screen, and Walsh's welcome names the ranked team.
- **Realistic simulated games:** CPU-vs-CPU games score like real seasons (about 25-27 points a team; a team far ahead stops piling on, some drives end in field goals), favorites win about as often as in real seasons, and home teams win about 58%.
- If one of your teams wins the national title, the end-of-season celebration plays.

### Historic teams

Both editions have 32 historic teams for Exhibition games: 18 from the original Bill Walsh College Football (1993) and 14 more from 1995-2025. On Game Setup, go left from the first team.

Alabama '78, Alabama '09, Auburn '83, Boston Col. '84, BYU '84, Clemson '81, Clemson '18, Colorado '90, Florida '08, FSU '87, FSU '93, FSU '99, Georgia '80, Georgia Tech '90, Indiana '25, LSU '19, Miami '87, Miami '01, Michigan '85, Nebraska '83, Nebraska '95, Notre Dame '88, Ohio State '14, Oklahoma '85, Penn State '86, Pitt '80, Tennessee '85, Texas '05, UCLA '88, USC '79, USC '04, Washington '91.

- Each team has its era's logo, helmet, wordmark, uniforms and end zones, a real roster with names and classes, hand-picked impact players for 13 of them, and a Walsh Report looking back on its season.
- The 1993 game's teams keep its ratings, converted to each edition's scale; the greatest stars can rate above today's best players.

### Dynasty

Play season after season with the **Dynasty app** on the Elevated site: it reads your save and ROM after a season, runs the offseason (graduation, recruiting, the transfer portal in 2026, progression) and writes a new season ROM. Season mode then plays the app's rosters, names, ratings, schedule, preseason poll and impact players, while Exhibition keeps the built-in rosters. A ROM without dynasty data plays as before. Both editions.

#### Saves

A season needs 32 KB of save RAM (the original game has 8 KB). It works in RetroArch (Genesis Plus GX) and on a Mega Everdrive Pro. v2.1.0 has a new save layout: **saves from v2.0.0 reset once** (custom audibles go back to the defaults, and a season in progress is lost).

### Plays

- **67 offensive plays from College Football USA '97**, added as new rows on the existing formation pages, with play art. The CPU calls them too. A few share a name, one to each side, as they do in CF97 (for example two I-FORM HB SWEEPs).
- **Eight new formations with 100 new plays**, adapted from Madden NFL 97, on two new rows at the start of the formation page: SINGLEBACK, SB 3WR, SB 4WR, PISTOL, 4 WR, EMPTY, TRIPS and SHOTGUN 2RB. The CPU calls them by offense style. To make room, 16 old plays left (PRO FORM's last row, NEAR's 5th row, four each from FAR and I-FORM).
- **Speed option and option sweeps:** SPEED OPT. in SINGLEBACK, TRIPS, SB 4WR, 4 WR and SHOTGUN 2RB, where the QB runs down the line toward the play side; NEAR's HB TS. SWEEP and FAR's HB TOSS SWP. are options too. C pitches.
- **Two new Shotgun plays:**
  - **RPO**: press B within about a second of the snap to pitch to the HB. Otherwise the QB keeps it and rolls out right, and you pass as usual. The CPU pitches half the time.
  - **HB SWING** (replaces HB SHOV.PASS): the HB swings across in front of the QB and up the sideline.

  <img width="400" height="280" alt="Shotgun plays page with HB SWING and RPO" src="images/rpo_hb_swing.png" />

- **Flip Play.** A FLIP PLAY tile replaces Instant Replay on the play-call screen (X on a 6-button gamepad does the same). It mirrors the formation, every assignment and the play diagrams; the offensive line stays on its side.

  <img width="400" height="280" alt="Play-call screen with FLIP PLAY on and the formations mirrored" src="images/flip_play.png" />

- **Pre-snap motion.** Send a back or receiver in motion before the snap: toward the middle he crosses the formation, toward the sideline he takes a short motion, and you can bring him back. A back runs straight up first, then over. You can send more than one man in motion on a play. Your selected defender follows him until you move the defender yourself, and CPU defenders in man coverage go with him.

  <img width="400" height="280" alt="Animation: a slot receiver goes in motion across the formation and his defender follows" src="images/motion.gif" />

- **Line motion.** The end man on the line (a tight end or split end) can go in motion too, when a receiver off the line on his side can step up: he leaves the line and the receiver steps up to take his place.
- **Swap tiles on the play-call screen:** SWAP HBS (offense) and SWAP MLBS (defense) replace Time Out (still on the pause menu) and put the backup halfback or middle linebacker in, with his own ratings, energy and stats, until you swap back (Z does the same); SWAP WR1/2 replaces Team Rosters on offense and trades the split end and flanker for the whole game. Swaps are yellow while on. CPU teams rotate their halfbacks and middle linebackers by energy.

### 6-button gamepad

These need a 6-button gamepad. With a 3-button gamepad the game plays as before.

- **5-receiver XY passing.** X and Y throw to the 4th and 5th receivers, with their own icons. A/B/C work as before.

  <img width="400" height="280" alt="Pass play with the A, B, C, X and Y receiver icons" src="images/xy_passing.png" />

- **Hot routes.** Before the snap on a pass play, press Y, pick a receiver (A, B, C, X or Y), then a route with the D-pad: for receivers and tight ends Up = streak, Outside = out, Inside = slant, Down = curl, Y = drag; for backs Up = wheel, Outside = swing, Inside = angle, Down = check-release, Y = screen; C = block. The same route again goes back to the called one, and Z cancels.
- **Flip at the line.** Open the audible menu with A, then press X: the play flips and the players run to their mirrored spots. A CPU defense usually flips with you (see [CPU and difficulty](#cpu-and-difficulty)).

  <img width="400" height="280" alt="Animation: the offense flips at the line and the CPU defense realigns to match" src="images/flip_defense.gif" />

- **Defensive shifts.** Before the snap, tap X, Z or Y to pick the line, the linebackers or the safeties (Shift Line, Shift LBs, Shift Safeties shows at the top right). Then left or right shifts the group a step that way (up to 2), down and up pinch or spread the line and linebackers or move the safeties up or back, and the same button again puts them back where the call lines them up. The players sidestep into place, facing the line.

  <img width="400" height="280" alt="Animation: the defensive line shifting before the snap" src="images/defense_shifts.gif" />

- **Flip your defense.** On defense, A then X mirrors your alignment and assignments; again to flip back.
- **SET FORM.** Y on the play-call screen goes back to the formations, on offense and defense.
- **Truck.** Hold Y as the ball carrier to truck, over and over while you hold it. B works as before (tap to truck, hold to spin).
- **Pre-snap info**, while you hold the button before the snap:
  - **X on offense:** the called play's art, an icon with the jersey number over each receiver, and a route icon over each one.

    <img width="400" height="280" alt="Hold X on offense: the play art and the receiver icons with jersey numbers" src="images/presnap_offense.png" />

  - **X on defense:** the defensive call's art, and a marker over each defender: R (rush), Z (zone), M (man) or S (spy).

    <img width="400" height="280" alt="Hold X on defense: the defensive call's art and the R, Z, M and S markers" src="images/presnap_defense.png" />

  - **Z:** energy bars over every player.

    <img width="400" height="280" alt="Z: energy bars over every player" src="images/presnap_energy.png" />

- **Team Rosters from Game Setup.** Z shows the highlighted team's roster; left and right step through every team, C switches between names and ratings, and when you close it the highlighted Home or Visitor row takes the team you're on.
- **Alternate uniforms.** On the controller select screen, Y under a team opens a picker for its helmet, jersey and pants (Up/Down = piece, Left/Right = option, Y = done). Many teams have real alternates; the visitor wears the opposite jersey type. CPU teams wear their primary uniform unless you change it.
- **Back to Game Setup.** Z (or B on a 3-button gamepad) on the controller select screen goes back to Game Setup with the teams and settings kept, in Exhibition and Season.

### Players and ratings

- **Player names:** on Team Rosters press C to switch between ratings and names with classes ("SO Malachi Toney"). The play recaps name the players: "Pass to #14 Micah Gilbert", "for 12 yards", "Tackle by #9 Chris Jones".
- **Impact players:** three per team, picked from the ratings and spread across positions (in Dynasty seasons the Dynasty app picks them). They're marked on the field and with a yellow dot on Team Rosters. Good plays put them "in the zone" (and bad ones can knock them out): while in it they get rating boosts, receivers drop fewer passes, a back or QB breaks the first tackler more often, and defenders tackle and intercept more.
- **Milestones:** a banner with the player's position, number, name and the team's helmet when he reaches a mark in a game (100/200/300 rushing yards, 3/4/6 passing TDs, 5/10/15 catches, 50+ yard plays …) or, in Season mode, in the season (1,000-yard rusher, 3,000-yard passer, 100 catches …).
- **Finer ratings:** every rating works in single points instead of the original game's 16 big steps, so players inside the same old step now differ. Team Rosters shows CFB-style 0-99 numbers and exact weights, the same scale in both editions.
- **Position labels:** cornerbacks are CB1-CB4 (CB1 and CB2 the starters) and the 3rd and 4th receivers WR3 and WR4.

### Gameplay

- **Realistic pass hang time:** a tapped deep lob lands in about 3 seconds (was 4), a short pass in about 1. Harder throws are unchanged.
- **More pass rush:** defenders chasing a QB who still holds the ball behind the line get a little more top speed.
- **No safety from the QB's own drop-back:** near his own goal line, for the first 1.5 seconds the QB doesn't drop out of the back of the end zone. If he scrambles out of it later, it's still a safety.
- **Defenders realign twice as fast after a defensive audible**, and CPU man defenders go straight to their man.
- **Kickoffs:** onside kicks are harder to recover, and a hard hit or dive on a kickoff returner fumbles at most 1 time in 20.

### CPU and difficulty

- **Difficulty row on Game Setup:**

  | Level | CPU |
  |---|---|
  | Normal | The original game. |
  | Smart | Audibles against your formation at the line and leans toward stopping what's working for you. |
  | Elite | Smart, plus +1 to the CPU team's ratings. |
  | Champion | Smart play calling with sharper adjustments and more audibles, +2 to the CPU team's ratings (speed +1), faster-reacting defenders, and a CPU team that tires at half the rate. |

- **Audibles that are harder to read** (Smart and up). Against your Nickel or Dime the CPU offense usually audibles to a run, but sometimes to another pass; against your 4-4 or Goal Line it's the other way around. Now and then it also checks into another play of the same kind elsewhere on the field. Champion audibles more often.
- **The defense answers your flip.** When you flip a play, with the FLIP PLAY tile or at the line, a CPU defense mirrors its alignment 9 times in 10, and its assignments follow: zones and rush lanes switch sides, and man defenders pick up the player who now has their man's role. It's set again in about a second.
- **Smarter 4th downs.** The CPU goes for it on 4th and short and more often in your territory, instead of almost always kicking. It still plays it safe late in a half and when leading late.
- **Reworked CPU defenses.** 3-4, 4-3 and Multiple styles, Dime on 3rd and 11+, and some 4-4 in run situations. Nickel and Dime linebackers are picked by rating, and every team uses the same DT1/DT2 and MLB1/MLB2 roster layout.
- **The CPU runs VEER** with its Option and Power offense styles. The original game never called VEER plays.

### Quality of life

- **Faster kickoff setup.** After a score the players run to their kickoff spots much faster: about 5 seconds to the kick instead of 13.
- **Team OFF/DEF ratings on Game Setup**, under each team's logo, as modern-style overall ratings (OVR), from each team's roster.

  <img width="400" height="280" alt="Game Setup with the OFF/DEF ratings and the Difficulty row set to Champion" src="images/game_setup.png" />

- **Instant replays keep the whole play**, however long (the original kept only the last 11-12 seconds).
- **Pause menu:** Resume Game, then Timeout with how many you have left ("Timeout - 2 left"), then Team Rosters.
- **New default audibles** for every team in a new save: offense I-Form Trp. Opt. R., I-Form WR Outs, Shotgun Deep Outs; defense 4-4 Jet Blitz, 4-3 Medium Zone, Nickel Full Zone. Set Audibles still changes them.
- **Menu music off or on.** Press X on a 6-button gamepad on the title screen, Game Setup or the season screens. Fight songs and sound effects still play. The setting is saved, and a music note on screen shows it.
- **Walsh Report:** a blank line between the offense and defense paragraphs.
- **Jersey numbers** under the players and in the recaps show single digits without a leading zero.
- **A medium skin tone** for every team's players.

### Title screen

ELEVATED appears in red under '95, so you can tell the patched game from the original at a glance, with "1994 Season Ed." or "2026 Season Ed." under it. The three other patches keep the original title screen. Every patched ROM has the game's built-in checksum corrected, so none needs a Game Genie master code.

### Known limitations

- Each added team plays one of the original game's 36 fight songs, so most teams don't play their own.
- 1994 Season Edition: played regular-season and exhibition games can still end in a tie, as in the original game.
- The historic teams play Exhibition games only.

## Controls

| When | Button | What it does |
|---|---|---|
| Title screen, Game Setup, season screens | X (6-button) | Menu music off / on |
| Game Setup | Left/Right on the Difficulty row | Normal, Smart, Elite, Champion |
| | Z (6-button) | Team Rosters (Left/Right: teams, C: names / ratings, Z or Start: back) |
| Controller select screen | Y (6-button) | Uniform picker for the team above |
| | Z (6-button) or B | Back to Game Setup |
| Play-call screen | C on the FLIP PLAY tile, or X (6-button) | Flip the play (the tile turns yellow); again to unflip |
| | Y (6-button) | SET FORM: back to the formations |
| | C on the SWAP tile, or Z (6-button) | Swap HB1 / HB2 (offense) or MLB1 / MLB2 (defense) |
| | C on SWAP WR1/2 (offense) | Swap the split end and flanker for the game |
| Before the snap, offense | Up/Down | Pick a motion man (a marker with arrows shows under him) |
| | Left/Right | Send him in motion; press the other way to bring him back |
| | A, then X (6-button) | Flip the play at the line |
| | Y (6-button), receiver, route | Hot route (Z cancels) |
| | Hold X (6-button) | Play art, receiver numbers and routes |
| Before the snap, defense | Tap X, Z or Y (6-button) | Pick a shift: line, linebackers or safeties |
| | Then Left/Right | Shift the group a step that way (up to 2) |
| | Then Down/Up | Line and linebackers: pinch / spread. Safeties: step up / back |
| | The same button again | Back to the call's alignment |
| | A, then X (6-button) | Flip your alignment; again to flip back |
| | Hold X (6-button) | Defensive call art and assignments |
| Before the snap, either side | Hold Z (6-button) | Energy bars |
| After the snap, QB | C, then A/B/C | Pass to receivers 1-3, as in the original game |
| | C, then X/Y (6-button) | Pass to receivers 4-5 |
| Ball carrier | Hold Y (6-button) | Truck, again and again |
| Option and RPO plays | C (option) / B within about 1 second of the snap (RPO) | Pitch to the back |
| Team Rosters | C | Names / ratings |
| Team Schedules | C | All of the team's games to HOLD or CPU |

**6-button gamepad in RetroArch (Genesis Plus GX):** the patched ROMs tell the emulator they support 6-button gamepads. If X, Y and Z do nothing, set *Quick Menu → Controls → Port 1 Controls → Device Type* to *MD Joypad 6 Button*.

## How to patch

1. Get an unmodified USA ROM that matches the checksums under [Original ROM required](#original-rom-required).
2. Download one `.bps` patch from the [`patches`](patches) folder and apply it. **Pick just one of these options** (any BPS patcher works):
   - **[Rom Patcher JS](https://www.marcrobledo.com/RomPatcher.js/)**, in your browser: choose your ROM, choose the patch, click *Apply patch*, save the result.
   - **Or [Floating IPS (Flips)](https://github.com/Alcaro/Flips)**: *Apply Patch*, pick the patch, pick your ROM, save.
   - **Or RetroArch soft-patching** (Genesis Plus GX core), no patched file needed: put the `.bps` next to your unzipped ROM and rename it to the same name as the ROM, e.g. `Bill Walsh College Football 95 (USA).md` + `Bill Walsh College Football 95 (USA).bps`. RetroArch applies it when the game loads and your ROM file stays unchanged.
3. Always patch the original ROM, not an already patched one. The patcher checks your ROM and refuses a different version.

## Game Genie codes (fatigue only, no patching)

If you only want to remove or fix fatigue, you can use Game Genie codes on the original ROM instead of patching it.

- These are v1.0's fatigue codes: the fixed version halves the original drain per play and recovers 4x faster. They don't include the current fatigue system or the other fixes; for those, use a patch.
- The first code in each line, `RZWB-66VG`, is the master code. It skips the game's checksum check, and the game won't start without it.
- Use them on the unpatched ROM only.

**No fatigue** (2 codes):
```
RZWB-66VG+R17A-N6YY
```

**Fixed fatigue** (5 codes), v1.0's fatigue fix:
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

| Patch | Size | CRC32 | SHA-1 | Genesis header checksum |
|---|---|---|---|---|
| Elevated: 1994 Season Edition | 4,194,304 bytes | `BFF60033` | `ed0cf10b17d4293780f31041cce9ad0149daec20` | `F90D` |
| Elevated: 2026 Season Edition | 4,194,304 bytes | `7E2A9410` | `7b4f9815b3aaf745acd590710f96484924fc7faa` | `6A2A` |
| Fixed Fatigue + Fixes | 2,097,152 bytes | `D7DA052E` | `c0997d06f32faa96d553862561550e51bbde8cec` | `EA9C` |
| Fixed Fatigue | 2,097,152 bytes | `FB633059` | `433ee808e77dc4254ac520682bad9e647584ae92` | `76E7` |
| No Fatigue | 2,097,152 bytes | `46E349F8` | `8ce1c5e64ee7cad54cac5df76470fe1ae994698c` | `B11D` |

Patch files:

| File | Size | SHA-256 |
|---|---|---|
| `Bill_Walsh_College_Football_95_Elevated_1994_Season_v2_1_0.bps` | 477,788 bytes | `e7f4ef436d381340c4832c9e4303f69b722479358f58b1ab2bde75f41934c2e2` |
| `Bill_Walsh_College_Football_95_Elevated_2026_Season_v2_1_0.bps` | 615,586 bytes | `ce6fdef466f3648cef4f30873144a89e405155cc6d718da06cc637fe7a81258f` |
| `Bill_Walsh_College_Football_95_Fixed_Fatigue_Fixes_v2_1_0.bps` | 632 bytes | `20b0c5d526666bb9a0aa27f8e0ed5468446be6e1b1d2f6d4de697a214904a996` |
| `Bill_Walsh_College_Football_95_Fixed_Fatigue_v2_1_0.bps` | 331 bytes | `73c28af91eec51b98300e95651a7f7695a675054f3b6dc3e21260dcff8f8249b` |
| `Bill_Walsh_College_Football_95_No_Fatigue_v2_1_0.bps` | 44 bytes | `9005796a80bf7c397f2039b6386454ef7b37c0570c2dc5bda33282964b452d73` |

## Changelog

### v2.1.0 (2026-11-19)
- **1994 Season Edition** (replaces the 36-team Elevated edition): all 107 I-A teams of 1994 with their conferences and rosters (real names for 2,962 of 3,424 players), the real 1994 schedule, the SEC Championship Game, the 19 bowls with their real tie-ins, the real 1994 preseason AP poll, and "1994 Season Ed." on the title screen. 4 MB ROM with 32 KB of save RAM.
- **Both Elevated editions:** 32 historic teams (Exhibition); Dynasty support with the Dynasty app; player names on Team Rosters and in the recaps; impact players; game and season milestones; Top 25 ranks in games; ratings in single points with CFB-style 0-99 numbers; eight new formations with 100 plays, speed options, hot routes, back motions and several motions a play; the swap tiles (HBS, MLBS, WR1/2); Y = truck; alternate uniforms (CPU teams wear their primary); Team Rosters from Game Setup; back to Game Setup from the controller select screen; whole-play replays; realistic pass hang time, more pass rush, no drop-back safeties, faster realignment after defensive audibles, harder onside kicks, fewer kickoff fumbles on big hits; realistic simulated seasons; new default audibles; a medium skin tone; the menu music setting is saved.
- **2026 Season Edition:** the two-minute timeout, today's clock rules and overtime, real names, a reworked CFB 27 ratings conversion, preseason Walsh Reports, and the real 2026 preseason AP poll.
- Fixes for v2.0.0 bugs: a garbled shift label near the end zones; glitched logos after fast team changes on Game Setup; 15 players in the 2026 rosters wore numbers their position can't wear.
- New save layout: saves from v2.0.0 reset once.
- Fixed Fatigue + Fixes, Fixed Fatigue and No Fatigue are the same as in v2.0.0.

### v2.0.0 (2026-11-11)
- **2026 Season Edition, rebuilt:** all 138 FBS teams (28 with new art), the 2026 conferences, rosters from CFB 27's ratings (Week 9 update), team styles and Walsh Reports for every team. New season mode: random or real 2026 schedules, conference title games, CFP 12, CFP 24, CFP 4, BCS 2 or no postseason, a CFP Bracket screen, Team Schedules for any team, Rankings with every conference, and Season Stats over all 138 teams. 4 MB ROM with 32 KB of save RAM (seasons saved with v1.1.0 start over). The pause menu shows the timeouts left, and single-digit jersey numbers have no leading zero.
- **Both Elevated editions:** defensive shifts and defense flips at the line (6-button), a CPU defense that answers your flip, line motion, SET FORM with Y on the play-call screen, faster kickoff setups, harder-to-read CPU audibles, and the menu music off or on with X.
- **Pitches to fast backs** are re-aimed in flight (Elevated editions and Fixed Fatigue + Fixes).
- **Fixed Fatigue + Fixes** now has only fixes for the original game's bugs: it also gets the season-sim fix, and the run-speed change for more explosive plays is now in the Elevated editions only.
- Fixes for v1.1.0 bugs: a delay of game or timeout after a flip at the line left the next play flipped; with the ball on the far hash, a CPU man defender could run across the field when your receiver went in motion.
- Fixed Fatigue and No Fatigue are the same as in v1.1.0.

### v1.1.0 (2026-11-09)
- The mod is now called Elevated; two editions (Elevated, and Elevated: 2026 Season Edition) plus three smaller patches (Fixed Fatigue + Fixes, Fixed Fatigue, No Fatigue).
- New fatigue system: every player tires from what he does on the field and recovers at each snap.
- 67 offensive plays from College Football USA '97, a new RPO play and HB SWING; the CPU calls the new plays.
- Flip Play, pre-snap motion.
- 6-button gamepad: 5-receiver passing, flip at the line, pre-snap info (Y) and energy (Z).
- Difficulty levels (Normal, Smart, Elite, Champion), smarter 4th downs, reworked CPU defenses, VEER for the CPU.
- Season-sim fix (offense and defense ratings were read backwards) and team OFF/DEF ratings on Game Setup.
- 2026 Season Edition: 11 teams from CF97, 2026 conferences, 2026 rosters from CFB 27 ratings, team styles, new Walsh Reports, CF97 logos for every team, new title art.
- Title screen: ELEVATED.
- The patches moved to the `patches` folder.

### v1.0 (2026-11-06), first release
- Released as *Bill Walsh College Football '95 Rebalanced*.
- Fatigue fix in two versions (fixed, none).
- Reduced slowdown on long runs and runs after the catch (human and CPU teams): 1.5-second burst, then a fade that depends on the runner's energy.
- 2-point conversion turnover kickoff fix.
- Title screen: REBALANCED under '95; the logo moved up 16 pixels to make room.
- Game Genie codes for the fatigue fix (fatigue only).

### Betas
The `v5` patches that were here before v1.0 were betas. They play the same as v1.0 but have the original title screen. The betas, release candidates and test builds of v1.1.0, v2.0.0 and v2.1.0 were private.

## Technical notes

For anyone digging into the ROM (68000 addresses):

- **Fatigue**:
  - Drain while the play is live: a hook at the snap (`0x06D11E`) and one in the per-frame player loop (`0x067E60`) add fatigue for each player from his speed every frame, his time in blocks, and the game's own events (tackles, route ends, jukes) at a quarter of their original cost.
  - Recovery: at each snap every player recovers a quarter of his fatigue; the roster screen no longer adds recovery. Code at `0x1E81E0`.
  - No Fatigue: AddFatigue returns at once (`0x06FA94` → `rts`).
- **More explosive plays** (Elevated editions):
  - In the original, a random tick at `0x075EC0` costs the ball carrier 1 speed point plus 10 fatigue while his speed is above 6.
  - The tick is hooked at `0x075EDE`. A snap hook at `0x06FB50` stores the original-game speed in two unused bytes of the player object (`$7E/$7F`), so fatigue builds exactly as before while the actual speed loss follows the table above.
  - Code at `0x1F0100`.
- **2-point fix**:
  - The fumble-recovery code (`0x075AA8`) flips possession even on a try; the interception path already checks for tries.
  - Hooks at `0x06FC38`, `0x06E588` and `0x06E4EC` (code at `0x1F0240`) count possession flips during the try and give the ball back to the scoring team before the kickoff is set up.
- **Pitches**: the hand-off/pitch routine (`0x075128`) leads a toss by the target's velocity at the pitch. A hook at `0x075230` marks the toss, and one in the ball's flight step (`0x07322A`) re-aims it every frame at the target's position plus his current velocity × the frames left, keeping the flight time. In Fixed Fatigue + Fixes the code is at `0x1E6800`.
- **Plays**: the new plays are numbers 100-167 in a new play list (`lea` at `0x06DC86`); a new offense image list holds the added rows, and the play-call menu maps each box to its play number. The CPU's play categories (pick at `0x079AB0`, membership test at `0x079A54`) point to a copy with the new plays, keeping each situation's run/pass and formation mix. The RPO and HB SWING take plays 143 (was DEEP OUTS 2) and 64 (was HB SHOV.PASS); the pitch is read in the ball carrier's input handler (`0x071AB4`).
- **Flip Play**: the top-row action that was Instant Replay (`0x06D930`) toggles the flip; formations and play commands are mirrored when they load, and the play-call art is drawn mirrored (draw hook `0x06DB00`).
- **6-button gamepad**: the header's I/O support is `J6` (`0x190`), and the pad read (`0x07A812`) reads both ports as 6-button pads; X/Y go into the throw select (`0x071CE4`) and a 5-receiver list.
- **Pre-snap shifts, defense flips, line motion**: input hook at `0x07601E`, SET FORM in the play-call menu handler (`0x06D79C`). The game's walk command moves the players; its start (`0x0734FE`) is hooked to speed up sidesteps, the realignment after a flip (3×) and the kickoff setup (3×), with every speed capped at ±32767. During a flip the defense's call is a mirrored copy in RAM; man defenders aim at their man's final spot through a hook in the hold handler (`0x0733D2`).
- **CPU**: the offense rule set (4th downs) is a copy at `0x106E7A`; the difficulty levels add a Game Setup row (menu at `0x10E000`, code from `0x10E6C0`), CPU rating boosts at the snap, and their own play-calling rule sets. The audible rules for Smart/Elite and Champion are at `0x290000`.
- **Menu music**: hooks at the sound driver's request (`0x07A6BC`) and stop (`0x07A654`) entries and at its update in the vblank handler (`0x076FE4`); only the menu songs `0x41` and `0x42` are affected.
- **Season sim**: `0x06F1A8` `move.w $2(a1),d1 ; move.w $4(a1),d2` → `move.w $4(a1),d1 ; move.w $2(a1),d2`, so a team scores by its offense (+2 of its ratings group) against the opponent's defense (+4).
- **OFF/DEF on Game Setup**: hook `0x0783A0` (code at `0x2D6800`) draws the text under each logo. The shown OVRs come from a table at `0x218000` ("OVR1", then {OFF, DEF} bytes by team slot); the sim reads the 0-100 ratings words.
- **Season Editions**: 4 MB ROMs (both editions since v2.1.0, on the same engine). Team tables from `0x218000` (OVRs, styles, menu order, end zones, fight songs, Walsh Report pointers), the Walsh Report text from `0x219000`, team data blocks from `0x230000`. 32 KB of save RAM on odd bytes (`0x200001`-`0x20FFFF`): only small copy routines below 2 MB switch it on, and the season screens work on a copy in RAM. Since v2.1.0 the save has room for about 150 season teams and records which build started and last saved a season. A manifest at `0x2DFF00` ("ELV1") tells apps and tools which build a ROM is and where its data lives.
- **Title screen**: the title image (`0x17C114`) is copied to `0x1F1000`, with the logo moved up and ELEVATED drawn in; the title code's two references to it (`0x078D70`, `0x078DA0`) point to the copy. In the 2026 Season Edition the portrait's cells and palette line 0 hold the new art.
- **Checksum**: the EA checksum constant at `0x1E6430` and the Sega header checksum are recomputed.

## Testing

- Play-tested in RetroArch (Genesis Plus GX) and on real hardware (Mega Everdrive Pro), where a v2.0.0 2026 season saved and reloaded fine.
- Verified with scripted headless runs (Genesis Plus GX):
  - Each patch applied to the original ROM reproduces the ROM above byte for byte (with Flips, and with a separate BPS decoder).
  - Every patched ROM boots, shows its title screen and plays CPU vs CPU.
  - v2.1.0, each Season Edition: 3 million frames of CPU-vs-CPU games, 2.4 million frames of random input on both gamepads, games with historic teams, and whole simulated seasons (1994 about 25 points a team, 2026 about 27, no ties); the stack never reaches the mod's RAM.
  - Full 2026 seasons from a new season to the champion, every game simulated, in every Postseason setting with random and real schedules: every game played; title games, seeds, pairings and the bracket checked at each round.
  - Pre-snap: 240 plays with random flips at the line, motions (line motion included), defense flips and shifts: every play snapped and ran with nobody off the field, except a few CPU delays of game.
  - Pitches: 46 pitches on 14 option and toss plays with max-speed backs, all caught. The case that fails in the original game (a long pitch after the QB has run) is caught.
  - Audibles: 12 tries of a CPU pass call against a human Nickel at Champion: 5 audibles to a run, 5 to another pass, 2 none (v1.1.0: 11 runs).
  - Flip Play: the lineups and assignments of all 96 original offensive plays mirror exactly, for both teams; audibles and special teams behave.
  - Every one of the 168 plays can be picked on the play-call screen; the RPO pitch was caught on 24 of 24 tries across defenses.
  - Difficulty: the CPU team's ratings at the snap are exactly +1 (Elite) or +2/+1 (Champion), capped at the maximum; the human team is unchanged.
  - Fatigue numbers are measured from CPU-vs-CPU games.
  - All new code is scanned for word or long accesses to odd addresses, which crash a real Genesis but not the test emulator.
- Limits:
  - The 2-point fix was verified by triggering the game's own turnover routine during conversion tries, not with a recorded real fumble.
  - In Fixed Fatigue + Fixes, the season-sim fix was checked in the code (the routine is only used by the sim).

## Credits

Created by JD637. Patches made with Floating IPS.

- Added plays, and 110 of the 2026 Season Edition's teams, come from EA's College Football USA '97.
- Helmets, logos, wordmarks and uniforms for the other 28 teams were made for this mod.
- 2026 Season Edition rosters are converted from EA Sports College Football 27's player ratings.
- 1994 Season Edition: 70 of the new teams come from College Football USA '97 and Pacific from College Football USA '96; the new teams' rosters come from 1994 preseason magazines (Athlon, Lindy's, The Sporting News), StatMuse and sports-reference; the real 1994 schedule and bowls from Wikipedia's 1994 team-season pages.
- Historic teams: 18 come from EA's Bill Walsh College Football (1993), with its rosters (names researched for this mod); the other 14 teams and their rosters were made for this mod.
- The real 2026 schedule comes from [cfbfastR-data](https://github.com/sportsdataverse/cfbfastR-data) (teams, dates and home/away only).
- 2026 Season Edition title art: Malachi Toney, converted to pixel art from a photo used with permission.

Not affiliated with or endorsed by Electronic Arts, the NCAA, or any school or player. No ROM is included in this repository.
