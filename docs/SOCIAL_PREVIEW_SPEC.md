# Social preview specification

The deployed interface currently has accurate page title/description metadata, but neither the GitHub repository nor the site has a purpose-built social-preview image. This is a specification for a future manual asset, not a generated or published image.

## Recommended composition

- Canvas: `1280 × 640 px` (2:1), exported as PNG under 1 MB.
- Background: the product's near-black/green visual language; keep contrast high at small preview sizes.
- Title: **Tactical Style Fingerprint**.
- Subtitle: **380 matches → 20 teams → 5 tactical dimensions**.
- Visual: use the real Liverpool–Tottenham comparison radar and the genuine `0.620` distance, not an invented decorative chart.
- Footer: small `StatsBomb event data · interpretable similarity` line if space permits.
- Safe area: keep critical text and the radar inside the central `1120 × 520 px` region to survive platform crops.

## Source material

- Use a frame from [`assets/tactical-style-fingerprint-demo.gif`](assets/tactical-style-fingerprint-demo.gif) or capture the live Liverpool–Tottenham comparison.
- Preserve the existing green/cream palette and typography; do not add football stock photography, fake badges, stars, usage numbers, or awards.

## Manual publishing

1. Export and inspect the PNG at both full size and approximately 320 px wide.
2. Upload it in the GitHub repository's **Settings → General → Social preview**.
3. If adding site Open Graph metadata later, place the optimized asset in `frontend/public/` and update Next.js metadata in a separate application change.

The application was intentionally not changed during this documentation task merely to add Open Graph metadata.
