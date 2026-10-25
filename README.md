# IB1 Remaster

**Infinity Blade (2010), rebuilt to run properly on a 2026 iPhone: full screen, HD, 60 fps, with its original bugs fixed.**

Infinity Blade set the standard for what a phone game could look like when it came out in December 2010. Fifteen years later, the original no longer works on a current iPhone. There are no sword sounds or voices, the picture doesn't fill the screen, and half the controls sit off the edge.

IB1 Remaster starts from the original game (version 1.4.3 with the fan Community Patch 2.5) and leaves its data files untouched. Every change is made by a small add-on that loads with the game. The result is the game as Chair Entertainment made it, running in full on an iPhone 17, sharper than it has ever looked on a phone, and without bugs that had been there since 2010.

| | |
|---|---|
| **Release** | 1.0 (build 17, 24 October 2026) |
| **Tested on** | iPhone 17, iOS 27.0.1 |
| **Base game** | Infinity Blade 1.4.3 + Community Patch 2.5 (data files unchanged) |
| **Resolution** | 2622 × 1206 (the screen's native resolution), 60 fps |
| **App size** | About 3.1 GB installed |

---

## What's new

### Looks
- **Full screen at full sharpness.** Drawn at the iPhone 17's native resolution, edge to edge, with no letterboxing or stretching.
- **HD textures for the whole game.** About 680 textures replaced with clean versions up to 4096 × 4096. These come from the fan-made HD texture pack where it covers them, and from the PC version's originals elsewhere. Each one is colour-matched to the iPhone original so the look stays the same.
- **Your own gear in HD.** The game builds the knight's swords, shields, armour and helmets into one combined texture while it runs. That texture is now rebuilt from HD pieces.
- **HD item icons.** All 115 shop and inventory icons enlarged 4×. The 54 weapon icons were redrawn from each weapon's own 3D model and coloured to match the originals.
- **HD menu lettering** in every language the game supports.
- **PC-style graphics settings.** Full-size textures everywhere (statues and columns had been drawn at a quarter of their detail), smooth texture blending, 4× anti-aliasing and 16× anisotropic filtering, none of which the game had switched on.
- **Light effects.** Soft bloom on bright areas, a gentle film-style contrast curve and sharpening. These apply to the 3D scene only, never to the menus.
- **Bump and shine maps from the PC version**, 76 of them across the castle, so stone, metal and floors catch the light.
- **PC-style lens flare.** The sun's flare now fades when your knight, a wall or a chest blocks it, instead of shining straight through.
- **The original 2010 opening film is back** in HD. It's widened to fill the screen, its lighting is extended into the new side areas, and its judder is smoothed out.
- **A sensible field of view.** On today's long screens the original widened the view so far you could see where levels end. It's now set to match the 16:9 phones the developers designed for.
- **A steady 60 fps** with all of the above, thanks to the Community Patch.

### Sound and music
- **Sword sounds, voices and effects are back.** On iOS 26 and later, the original plays only music.
- **New volume sliders** for Master, Music and Voice, alongside the original SFX slider.
- **Speech you can hear.** Music dips while characters speak, and their lines are slightly louder. The God King's offer was nearly drowned out before.
- **Fight music follows the fight.** Stage changes play the right track, and the tracks stay in step.
- **Music when you resume a saved game**, and "fade out" moments are silent, as intended.
- **No dropped sounds in busy moments.** The sound engine now has 64 voices instead of 32.

### Controls and screen
- **Redesigned dodge buttons.** The dark square panel is gone. The arrows are now deep black with a soft white glow, matching the health bar, and they light up in the game's blue when pressed. They're drawn at their true shape and at twice the detail.
- **Block button size slider**, under the game's own Dodge Button Size setting. It goes from the original size up to 1.5×, and the shield, its number and its touch area all grow together.
- **Controls and health bars clear of the Dynamic Island** and the rounded corners.
- **Fast-forward only while held.** It can no longer get stuck and race through later cutscenes.
- **The skip button works wherever you tap it**, including its bottom half at the screen's edge.
- **Swiping home no longer swings the camera.**
- **Larger subtitles**, a hidden status bar and home bar, and a properly placed Start button.

### Menus and convenience
- **Every menu and screen fills the display**, with no black or bright strips at the sides.
- **Saves appear in the Files app** (On My iPhone → Infinity Blade), so you can back them up without a computer.
- **The broken gold store is switched off.** It used to hang forever on "Connecting to iTunes". The shop now behaves as designed for builds without a store: BUY only lights up when you can afford something, and spending gold you don't have tells you how much more you need.
- **The end screen shows its Infinity Blade logo again.**

---

## Bugs fixed

### From the original 2010 game
These were in the game as released, not caused by modern iPhones.
- Cutscenes losing their sounds and effects in long sessions: footsteps, shouts, screams and the God King's blue flames vanished the longer you played, until a restart.
- Fight music jumping back to the first stage's track when a fight moved on quickly, so the second stage's music was never heard.
- No stage music changes in the Guardian fight, which opens every bloodline.
- Silence after resuming a save. Only 3 of the castle's 37 save points restarted the music.
- "Fade out" moments playing the castle walking music instead of silence.
- Zero's death music never playing, because the file was requested with the wrong capital letter.
- The knight walking past his spot to the cliff edge in the opening scene, when two of the developers' films competed to control him.
- Fast-forward sticking on and racing through later cutscenes by itself.
- A dazed boss knocked below its next-stage mark staying in the old stage until another hit landed. It now changes stage as soon as the daze ends.
- The God King's dying lines playing over a black screen after skipping his ending.
- The end screen's missing logo.
- The sun's flare shining through characters and walls (the iPhone version never had the PC version's check).
- Judder in the opening film, where every fifth frame of movement was doubled by the original 2010 conversion.

### From running a 2010 game on a 2026 iPhone
- No sound effects or voices, only music (iOS 26 and later).
- No music on first launch.
- A letterboxed picture instead of full screen.
- Health bars and the block, dodge and fast-forward buttons off-screen once the picture filled the display.
- Bright strips and black sides on the results screen, tutorials, Options and Character Slots.
- Touch circles drawn beside enemies instead of on them.
- Sound cutting out after a half swipe up, Control Centre or a call banner, and effects going permanently silent after a pause.
- The picture rendered below the screen's native sharpness.
- The skip button only responding when tapped above its middle.

---

## How the big ones were found

<details>
<summary><b>1. Cutscenes going quiet, and the God King's missing flames (a 2010 bug)</b></summary>

**Found:** In long sessions, walk-ups to enemies were silent, enemies drew their swords without a shout, and kicked enemies didn't scream. The God King's blue flames disappeared in his intro and at the final stab, but never in the two scenes in between.

**Tracked down:** Logs showed that the cutscenes' cues (the sound and effect markers inside each animation) weren't firing at all. A test build recorded each God King cue as it came due. The film requested it every time, but his animation was set to fire cues only at full blend, and at those moments it was a hair short of full. That setting came from the game's own fight code, which switches it on when a move ends so the move's sounds don't play as it fades out. Cutscenes reuse the same animation slot and never switch it back. A fresh start has no such slots, which is why restarting the game brought the effects back. I remember exactly that from playing on my iPhone 5.

**Fixed:** Whenever a cutscene takes over an animation slot, it switches back to "always fire cues", just as the game does when a fight move starts. One fix covers every cutscene in the game.
</details>

<details>
<summary><b>2. A silent game on iOS 26</b></summary>

**Found:** Music played, but there were no swords, grunts or voices.

**Tracked down:** The game pauses its sound engine with a counter whenever iOS interrupts the audio. The opening film triggers an interruption, and current iOS never sends the "interruption ended" message, so the counter stays stuck.

**Fixed:** Once a second, if the sound engine is paused when nothing should be pausing it, the game's own "interruption ended" code is called.
</details>

<details>
<summary><b>3. The mech's intro racing past in a blur</b></summary>

**Found:** Starting the mech fight jumped straight to the middle of the battle.

**Tracked down:** Fast-forward was switching back on with no finger on the button. Over five test runs it turned out the game keeps three saved copies of its speed: one for the fast-forward button, one for the pause menu, and one in every film with a slow-motion section. A copy saved while you held fast-forward would switch fast-forward back on later. Every saved log was then replayed to count each case by its cause.

**Fixed:** None of the three copies can hold a fast-forward speed, and a fast-forward with no finger down is ended immediately.
</details>

<details>
<summary><b>4. "My own armour doesn't look HD"</b></summary>

**Found:** Enemies looked HD, but the knight's equipped shield and armour didn't.

**Tracked down:** The game never uses an item's texture directly. While it runs, it builds one combined texture from everything you're wearing, so the HD swap never saw the individual item textures.

**Fixed:** The combined texture is now recognised piece by piece and rebuilt from the HD versions. Every texture the game loads is checked, so a miss would show up immediately.
</details>

<details>
<summary><b>5. Fight music going backwards</b></summary>

**Found:** The second stage's music never seemed to play.

**Tracked down:** The developers set each intro track to start the next track when it finished, however it finished. When a stage change replaced the intro early, that link still fired and put the first stage's track back on.

**Fixed:** That handover is skipped when another track has already taken over, in all 25 places the developers used it.
</details>

<details>
<summary><b>6. Zero's death music</b></summary>

**Found:** His death scene was silent.

**Tracked down:** It requests "menu-normal", but the file is "Menu-Normal.mp3", and iOS treats capital letters as different.

**Fixed:** Every music request now finds its file regardless of capitalisation.
</details>

---

## Under the hood

| Area | Detail |
|---|---|
| Base game | Infinity Blade 1.4.3 + Community Patch 2.5 (data files unchanged) |
| Device | iPhone 17, iOS 27.0.1 |
| Resolution | 2622 × 1206 (native), 60 fps |
| Textures | About 680 in HD, up to 4096 × 4096 |
| Graphics | 4× anti-aliasing, 16× anisotropic filtering, full-size mip levels, bloom, contrast curve, sharpening, bump and shine maps |
| Sound | 64 mixer voices (was 32); Master, Music, SFX and Voice sliders |
| App size | About 3.1 GB |

---

## Version history

| Build | Date | What came in |
|---|---|---|
| 1 | 21 Oct 2026 | The game working on the iPhone 17: sound and voices, full screen, controls, menus, music fixes, volume sliders, no stuck gold store, field of view |
| 2 | 21 Oct | Full sharpness; saves in the Files app |
| 3 | 21 Oct | The original opening film, in HD |
| 4 | 21 Oct | The opening film fills the screen; the knight stops on his rock |
| 5 | 22 Oct | The skip button responds at the bottom edge |
| 6 | 22 Oct | New dodge buttons |
| 7 | 22 Oct | Block button size setting |
| 8 | 22 Oct | No more dropped sounds in busy moments |
| 9 | 22 Oct | Graphics settings and light effects |
| 10 | 22 Oct | Effects on every frame; fight music that keeps up |
| 11 | 22 Oct | Swiping home no longer moves the camera |
| 12 | 24 Oct | Bump and shine maps, PC textures, the sun's flare, stage music |
| 13 | 24 Oct | The end screen's logo, sound safety checks |
| 14 | 24 Oct | Speech over music, Voice Volume slider, skipped ending stays skipped |
| 15 | 24 Oct | An experimental effects "safety net" switched off |
| 16 | 24 Oct | HD textures for the whole game, HD gear, HD icons |
| **17** | **24 Oct** | **Fast-forward only while held — released as 1.0** |
| 18 | testing | Every cutscene keeps its sounds and effects, however long you play |

---

## Still to come
- **Build 18:** every cutscene keeps its sounds and effects however long you play (in testing).
- **iPad version** (iPad Air), with saves shared between iPhone and iPad through iCloud.

## Documentation
- **FIXES.md** records every problem, its cause and the exact fix, with enough detail to redo the whole project from the original download.
- **GAME-MAP.md** and its study files explain how the whole game works: levels, fights, music, menus, saves and the iPhone side.
- Every music track, sorted by fight and named by when it plays, with a guide and side-by-side comparison clips.

## Credits
Infinity Blade by **Chair Entertainment** and **Epic Games**. Built on the fan **Community Patch 2.5** and the fan-made **HD texture pack**, plus the PC version's original textures. Restoration work by Second Light.

*This is a personal, non-commercial restoration project. Infinity Blade and all its assets belong to their respective owners.*
