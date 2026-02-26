# Setting up the self-hosted Cutive Mono font

To avoid depending on Google Fonts (which can be slow or blocked on poor connections),
the site loads Cutive Mono from this folder.

## Steps

1. Go to https://fonts.google.com/specimen/Cutive+Mono
2. Click "Download family"
3. Unzip the downloaded file
4. Convert `CutiveMono-Regular.ttf` to WOFF2 using a tool like:
   - https://cloudconvert.com/ttf-to-woff2
   - or locally: `woff2_compress CutiveMono-Regular.ttf`
5. Rename the output to `cutive-mono.woff2`
6. Place it in this folder (`assets/fonts/`)

The CSS uses `font-display: swap`, so the page renders immediately with
the system monospace fallback and swaps to Cutive Mono once it loads —
ideal for slow connections.
