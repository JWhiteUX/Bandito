# Bandito

A minimal browser-based utility for diagnosing vertical banding and panel uniformity defects on monitors. Sweep through grayscale brightness levels and log where banding is visible, then export results as CSV for documentation or warranty claims.

## Usage

Open `index.html` in any browser and go fullscreen (`F11`).

| Key | Action |
|-----|--------|
| `↑` / `↓` | Adjust gray level (steps of 5, range 0–255) |
| `Space` | Log current gray value with timestamp |
| `D` | Download logged entries as CSV |
| `Click` | Toggle UI overlay |
| `Esc` | Show cursor |

The UI auto-hides after 8 seconds for a clean test surface.

## CSV Output

Exported CSV includes:

```
entry, gray_value, rgb, hex, timestamp, note
1, 40, "rgb(40,40,40)", #282828, 2026-03-11T03:48:21.915Z, 16% brightness
```

## Why

VA and OLED panels frequently ship with vertical banding visible on uniform gray fields — particularly in the 5–50% brightness range that overlaps with dark mode UI surfaces. This tool makes it easy to systematically identify affected brightness levels and produce timestamped evidence for returns or warranty claims.

## Tips

- Test in a dark room for best visibility
- Start at 0% and sweep up slowly
- Banding that stays fixed regardless of content or input source is a panel defect
- Banding that shifts with head movement may indicate VA viewing angle limitations
- Log every level where banding is visible, not just the worst ones

## License

MIT
