# Logo Creation Workflow

> Status: ✅ Done — stable and tested with 2 projects

## Pipeline

1. Receive inputs: ProductName, ProductIdea, VoiceTone, SampleColors[], NeedsDarkWhiteVariants (default true)
2. Determine next sequence number (auto-increment, zero-padded)
3. Generate SVGs: Logo.svg, Logo-Dark.svg, Logo-White.svg, Logo-Animated.svg (SMIL)
4. Render rasters: 052, 128, 256, 512, 1024-Light, 1024-Dark
5. Generate animated GIF from SVG frames
6. Generate Palette.md + Tokens.json
7. Regenerate root favicon.ico, favicon.png, gif-animation.gif
8. Update index.html favicon links
9. Write README.md with all relative paths

## Validation Checklist
- [ ] `Projects/{Seq}-{PascalCaseName}/` exists with all 4 subfolders
- [ ] 4 SVGs in `icons-svg/`
- [ ] 7 raster files in `icons-image/`
- [ ] Palette.md + Tokens.json in `colors-themes/`
- [ ] Root favicon + gif updated
- [ ] README renders on GitHub

## Notes
- One-shot unless user asks for phased delivery
- Never overwrite existing project folders
- Dark + white variants default to ON
