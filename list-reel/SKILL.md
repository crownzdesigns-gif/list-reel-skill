---
name: list-reel
description: Plan and produce a short vertical "20 Things" list reel (e.g. 20 Loading Animations, 20 Button Hover Effects, 20 App Onboarding Screens) where each example plays for about a second while a numbered list fills in, ending on a grid of all examples. Use when someone asks for a list reel, a "20 X" reel, or an animated design-examples video for Instagram, TikTok or Shorts. Not for talking-head videos, voiceover tutorials or single-product promos.
---

# List Reel

Make a 9:16 list reel that shows a numbered set of design examples. Each example plays for about one second while a numbered list fills in beside it, and the reel ends on a grid of every example. The look always comes from the creator's own brand, never from another creator's style.

## 1. Collect inputs first

Ask for these before building anything. If the creator skips one, use the default in brackets and say which default you used.

1. **Topic and count.** What the list is about and how many items. [20; use 10 when each example needs more reading time]
2. **Example source.** Built demos (animations made in code or a design tool) or real examples (screenshots or recordings of public apps and websites). [built demos]
3. **Brand kit.** Background colour, accent colour, heading font, body font and handle. If they have none, propose two or three original palette and font pairings and let them pick. Never reuse another creator's palette, fonts or layout.
4. **Layout.** One of the layouts in step 2. [Stage + list]
5. **Format.** [9:16, 1080×1920, 30 fps, 20–30 seconds]

## 2. Pick a layout

Offer these and let the creator choose, so reels made with this skill don't all look the same.

- **Stage + list:** the example sits in a framed stage at the top and a two-column numbered list fills in underneath.
- **Phone frame:** the example sits inside a phone mockup in the centre, and the current item name appears in large type above it.
- **Full-bleed:** the example fills the screen, with a small counter ("07 / 20") and the item name in a corner.
- **Split screen:** the example plays on one half and the list scrolls on the other half.

## 3. Write the list

Draft the items so each is clearly different from the others. Name each one in 1–3 plain words a beginner would understand ("Pulse Rings", not "Concentric Radial Emitter"). Show the list to the creator and adjust it before building.

## 4. Gather or build the examples

**Built demos**
- Make each animation complete a clear motion within about 1.2 seconds, so it reads in its short slot.
- Keep the subject centred and large, with nothing important near the edges.
- Draw at 2× and downscale for crisp edges. When drawing semi-transparent shapes, draw them on a separate layer and composite it, or blend the colour toward the background; drawing alpha straight onto the frame and then flattening makes fades look solid.
- Align single letters on a shared baseline, not by their centres, or lowercase letters will jump.

**Real examples**
- Use public apps and websites and record the source name for each item.
- Leave out real people's faces, personal details (names, addresses, emails, tracking numbers), loading spinners, ads and seasonal banners that date the post.
- For scrolling or moving websites, use a real screen recording, or capture many frames at small scroll steps (about 40–90 px). A handful of far-apart screenshots looks laggy, and frame interpolation cannot fix large jumps.

## 5. Set the timing

At 30 fps:
- 20 items: about 37–38 frames each (≈1.25 s). Use `round((i+1)*37.5) - round(i*37.5)` so the total lands exactly.
- 10 items: about 75 frames each (2.5 s).
- End with 2–3 seconds of a grid showing every example.
- Keep the total under 30 seconds.

## 6. Design the frame in the creator's brand

- Title at the top ("20 Loading Animations") with the handle under it.
- The example in the chosen layout.
- The numbered list (or counter) revealing one item per example, so the list completes as the reel ends.
- Optional small label on each example, such as `loader/pulse-rings`.
- Check that no item name is long enough to collide with the next column; shorten names that are.

## 7. Render

Use the tool the creator has:
- **Code:** Python with Pillow for frames, piped to FFmpeg (`-f rawvideo -pix_fmt rgb24`), or HTML/CSS animations screen-recorded.
- **Design tools:** After Effects, Figma prototypes, CapCut.

Export H.264 MP4 at 1080×1920, `yuv420p`, with a silent audio track (e.g. FFmpeg `anullsrc`) so the creator can add trending audio in the app.

## 8. Cover and caption

- **Cover:** the final grid frame, or a still with the title and 4–6 examples. Keep the title inside the centre 3:4 area so the profile grid doesn't crop it.
- **Caption:** open with a question people can answer in a word or emoji ("Which one would you use?"), add one line on why the list is useful, then one call to action. Only offer "comment KEYWORD for the code" if the creator actually has the code ready to send.

## 9. Check before delivering

Pull a contact sheet of frames (for example `ffmpeg -vf "fps=1,scale=270:-1,tile=11x3"`) and look at it. Confirm that:

- Every item is visibly different and moves within its slot.
- Text is readable on a phone at arm's length.
- Nothing important sits in the bottom 20% of the frame or near the right edge, where Instagram and TikTok put their buttons.
- Real examples contain no faces, personal data or third-party watermarks.
- The video is 1080×1920 and the planned length.
- The look follows the creator's brand kit.

Report what you made, the list of items, and anything the creator should check (for example, an example that may date quickly).

## Why these reels get saved and shared

- The list is useful later, so people save it as a reference and send it to teammates.
- The examples move; live animation holds attention better than static screenshots.
- Each item is short, so viewers rewatch to catch the ones they missed.
- When one does well, a Part 2 with all-new items is the natural follow-up.
