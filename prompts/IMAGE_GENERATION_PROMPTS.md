# Image Generation Prompts

Reusable prompt patterns for image tasks.

## Default

Generate one strong image unless variants are requested.

Do not generate extras just to solve cropping.

## Single Image

```text
Generate one image of [SUBJECT].

Style:
[medium / mood / reference style]

Composition:
[framing, angle, key objects]

Lighting:
[direction, intensity, color mood]

Constraints:
- one image only
- no text unless requested
- leave crop margin if useful
- prioritize readable silhouette
```

## Visual Asset

```text
Generate one concept image for [ASSET].

Purpose:
[illustration / portrait / environment / item icon / UI background]

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

## Iteration

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

## Likeness

For real-person likeness, request a reference image unless one is already provided.
