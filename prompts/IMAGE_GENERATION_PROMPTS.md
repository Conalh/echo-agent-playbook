# Image Generation Prompts

Reusable prompt patterns and preferences for image-generation tasks.

---

## Default Preference

Unless multiple variants are explicitly requested, generate one strong image.

The user may personally crop, frame, or adjust the result afterward. Do not generate extra versions only to solve cropping unless asked.

---

## Single Image Prompt Pattern

```text
Generate one image of [SUBJECT].

Style:
[style / mood / medium]

Composition:
[main framing, camera angle, major objects]

Lighting:
[lighting direction, intensity, color mood]

Constraints:
- one image only
- no text unless requested
- leave enough margin for cropping if useful
- prioritize strong silhouette and readable composition
```

---

## Visual Asset Prompt Pattern

```text
Generate one concept image for [ASSET].

Purpose:
[illustration / portrait / environment concept / item icon / UI background]

Visual identity:
[themes, motifs, materials]

Composition:
[framing and focal point]

Avoid:
[things that do not belong]

Constraints:
- one image only
- readable at small size
- strong silhouette
- no logos or text unless requested
```

---

## Iteration Prompt

```text
Revise the previous image.

Keep:
- [what worked]

Change:
- [specific change]

Avoid:
- [what went wrong]

Generate one image only.
```

---

## Likeness Rule

If the image should include the user or a real person, request a reference image first unless one is already provided in the current conversation.
