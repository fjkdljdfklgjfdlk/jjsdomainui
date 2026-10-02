# JJS Domain Creator — Roblox / Skill Builder tutorial

This guide follows the supplied **domain** template. The template has been decoded and inspected, but has **not been tested inside Jujutsu Shenanigans**. Game menu names may change. The companion video is an original illustrated walkthrough, not a recording of the game.

## The template is optional

**You do not have to paste or use the template. You can build the skill from scratch in Skill Builder.** Create your own sequence of Visual nodes with Effect set to Overlay, assign your uploaded frame textures in order, and add Wait nodes between frames. Start with a wait of `1 / FPS` seconds, then adjust the Overlay lifetimes and test playback. Add branches or other effects only if your design needs them.

The 36 + 36 nodes and 72 texture replacements described below apply **only to the supplied template**, not to every custom skill. A scratch-built skill can use your own frame count and structure.

## Steps

### 1. Export the frames

Finish your domain, then choose 3 seconds and 12 FPS. Click Download frames (.zip).

3 seconds × 12 FPS = 36 PNG frames

### 2. Upload all 36 PNGs

Extract the ZIP. Upload the numbered PNGs as image / decal assets in Roblox Creator Hub or Studio.

Wait for each image to finish processing and moderation.

### 3. Keep the textures in order

Copy the image / texture asset ID for every uploaded frame. Keep a numbered list.

Use the texture/image ID accepted by JJS, not a page URL.

### 4. Open Skill Builder

Join your JJS private server. Enter Build Mode, place a Character Block, and open Configure.

Edit the relevant skill to open its Skill Builder.

### 5. Choose a template or build from scratch

Either build your own Overlay/Wait sequence from scratch, or optionally copy the entire template from the tutorial popup and paste it into the code/import editor.

If the skill editor rejects the format, use Configure’s character import control.

### 6. Assign your own frame textures

If you use the supplied template, the main sequence has 36 Overlay Visuals and the Freeze branch has another 36. Replace both sets in order. If you build from scratch, assign the matching uploaded frame texture to each Overlay you create.

72 texture fields total. Reuse the same 36 frame IDs in each sequence.

### 7. Set timing. Test. Improve.

For 12 FPS, use roughly 0.0833 seconds between frames. The supplied waits are 0.1 seconds.

Adjust effect lifetimes, test both sequences, then save. Make it your own.

## Important template details

- The provided code contains a skill named `domain` in slot 1, with a 4-second cooldown.
- There are **36 Overlay Visual nodes in the main `Line` and 36 more in `Branch → Freeze → Line`**.
- **Change ALL Overlay Visual Texture values to YOUR uploaded video-frame texture IDs.** Replace them in playback order in both sequences, including repeated or apparently blank frames. Do not leave the example textures behind.
- Reuse the same ordered set of 36 uploaded frame IDs for each sequence. You do not need to upload each frame twice.
- The starter export of 3 seconds at 12 FPS gives 36 frames, matching the number of Overlay nodes per sequence. The template has 35 Wait nodes per sequence, currently set to `0.1` seconds. At 12 FPS, start with `1 / 12 ≈ 0.0833` seconds between successive frames and check the Overlay effect lifetimes, including the final frame. Changing only the waits does not guarantee that the total effect duration matches the video.
- If you export a different number of frames, add or remove matching Overlay/Wait nodes in **both** sequences. Do not squeeze a longer sequence into fewer nodes by silently skipping frames.
- This template also contains animation, hitbox, and stun settings. Review their behavior in your private server and adjust them to fit your domain.

## Uploading and finding the correct IDs

In Roblox Creator Hub, open your creations/development items and the image or decal upload area. Alternatively, import the PNGs using Roblox Studio's asset tools. Upload every numbered PNG from the extracted `frames` folder. The ZIP or MP4 itself is not the texture sequence.

Keep filenames in ascending order: `domain_0000.png`, `domain_0001.png`, …, `domain_0035.png`. Roblox assigns an asset ID to each imported image. Use **Copy Texture ID / Copy Asset ID**, where available, or inspect the uploaded image in Studio. A decal's catalog/container ID may differ from the underlying image ID: use the actual image/texture ID expected by the Overlay Texture field. Test one image first if unsure. Use `rbxassetid://ID` only if the field expects a URI; otherwise paste the numeric ID.

Wait for moderation/processing and check that the assets can be used in the target experience. A blank image may mean the ID is wrong, the asset is unavailable, or the Overlay settings hide it.

## Import route

Start with the requested workflow: Character Block → Configure → edit the relevant skill → Skill Builder → code/import editor. Paste the complete template below, without Markdown backticks, and apply/import it. This is compressed JJS configuration data, **not Lua code for Roblox Studio's script editor**.

The decoded outer structure is a list of skill settings. If the skill editor does not accept it, use the Character Block Configure menu's import/clipboard control, then reopen the imported `domain` skill. Full-character configuration and individual-skill imports are distinct routes. Preserve an existing character by exporting a backup before replacing its settings.

## Replace textures, test, and customize

Open each Visual node with Effect set to Overlay. Replace its Texture field with the corresponding uploaded frame's texture ID. Repeat the entire operation inside the Freeze branch. Keep the same order in each path. Preview the move, check the first and last frames, and test whatever conditions trigger the Freeze branch. Verify the overlay disappears at the end.

You can modify the character, background, text, frame count, speed, effects, animation, and gameplay settings. Improve the template as much as you like, then save/export your character from JJS. Saving the web editor's JSON project does not save your in-game character.

## Original template code

The following string is preserved as supplied. Copy the entire single line.

```text
KLUv/WB2bsUoAEpGTAwpAI22DjzZAoY88UIAF35EfeWiNwj7OEBSN769frktSTn6qJcAVFVVTQjOAMAAnADsXFt0QggiB0CpM+2i00FG5j0eyIhN8zAKA+M8aKE4HkhBgQ1RvgZCBGKkkyJVNBjIwOhMvOiEkOY16Ew6JxAeRDqXxAAWnTIyKDJ6jc6kE8onI52LzpmcF53QESXDgYrzKA1knMfoTBIHCiIIFp0ygiALBTaLF0WGToqHRadkEtHoTBAPi84GEkgyQSKZUNBJsehMYGASmVjopNBFn3wMTb6oI+BhNM/DaOJFHWBDkzZNbEQFGpp0EhFZIHFAF4WO52iSQJh4sCiD8ZTiIeu8zhs71VrzUsyMtynnzX0xa36nlnV73l/MKWblrt7/n+mU8QlgilTxgEAQlE6UEFEwIYnwMFBBASadzYNEsUHng4nI44GEBHQgQmISWQCBQeeiU0LvoTgwngVkxEiRDowNA8EGCEaK8ygOBNKZOsBORBadsHGQUWQgFBnKghOjB2P0PHQmnaukVdLqXHQ6T5RPPpAimycdyON4imyezqRTSf+tc9EJPc3D6FQSA9C56GwFEoiRIpunMzX2xrxrqd2M1fpfzbcXu8ZaLcbaK99l52zbem/9z858dbdtzGr3V3Pbz7ypZuu+ued2ztm1Wv7PFivm5e7c3Fp+brWt+Jv7ry+/WrWY7z9Tzda3ZcXamXq12G2zd+613My/y618nWvM7a7i9/d2bNktX8/Ni9ez39bLjPW3XeddirHGy7lfzc3PWrdrTq1q3r6p5V/l2h077+ZrMTv23VrxChAVqos+olSa55GatIKBxMRDZ4Lo/v6eREQWSDAeDlJpME/KN+BZyMigpHWdi04GxnnQAuK5WbwG8zSLpokNuAA9qcBmwYkRXHiOx5BMIg4mUeeiE0aQAo7oOKLzIDrtw6JTAIwNEHpUVEB027WuXH97xd3M/1tb77jbu1Ley9Tiphp75xi7ak2x6u11z/aZeWvXijnexXo5143Vaubfq9pit27tN2Pn5apZc+6bWuW767zZr37ljrUWgL2o8RUhhIyMiIidglQaA6ACEREaGUk8EkiASBAJYQhCEVBERoAgCCERECJ8IiCColgiffkuA7i7w/yXSg8KVavCy1iu2BBcI4xx2XUg6/hb6zjEk0YdX7QxjjK9sDsPjGIRrHPDp2CRJ/hzZ8mj6WXHRhjPNprOwbsiJzPQpOO6eH/HV1iJdqaX/UxhPFN1Ogdnl5zMXpaO63F/52K0Q8fP4fZDpk8sBxXjx/keOtNn5ovIBAfI5vhOG4pgZC8MMGxDjnMUVxBn+smaxBjuj5Ic32nSEhAbck8x86h2NT79ziZsYBFtM7y2JiWatbk/c0mpa8ZPCcDAJv37VbWGt9ftKVwpTecmhQ+wfBKXsmNtOFwVyc9Yzb8tRK9ZI63PKMxlNuw/cv1DXBg0QOr0YTnsKAzHJhpFHjULi7IxGAzCxmZABsKV8CMbu8aAWGwqDKk/Ez+I/6zyY/Kz7Ae/AHFdhp8JP85+Zn4Q+xlNfiSV93GdHzuKZz89ktVnKPmR1N7HTJ8Ef0DoE4nYT7UASeIirF8yRP0gnxqpSFNAKnboYK52ZDXYxr9DgsMn8TnpTAMokwNISdUUNQ/3Kwnme7fXcK5vGaL19xLTeiS+q3wuhPL1cKfSwhUVUMp8LzcM+IGezb9Zs9sJmsSjFgU0nEYBf934d6B/drtVeWMVCtPV
```

## Research and references

Checked October 2, 2026. Roblox documentation is the primary source for image assets. JJS menu guidance comes from community documentation; the template counts above come from direct inspection of the supplied code.

- [Roblox: textures and decals](https://create.roblox.com/docs/parts/textures-decals)
- [Roblox: assets](https://create.roblox.com/docs/projects/assets)
- [JJS community wiki: Skill Builder](https://jujutsu-shenanigans.fandom.com/wiki/Build_Mode/Skill_Builder)
- [JJS community wiki: Build Mode](https://jujutsu-shenanigans.fandom.com/wiki/Build_Mode)
- [Community guide: importing JJS codes](https://jjsbuilder.com/guides/how-to-import-jjs-moveset-codes/)
