# luminFish 2.0 (was Sol Macro / Brry)

## Design (features unchanged)
- New night-blue luminFish look in the panel AND the app: glowing animated border, twinkling stars, drifting glow, emblem start button.
- Panel is now 16:9 and smaller. App > Look > Panel size: Small / Normal / Big.
- App > Look > Panel background: pick a photo or GIF (GIFs move on Android 9+), and how dark it is.
- App icon + floating icon = luminFish emblem. Floating icon: breathing glow, pulse rings, orbiting spark, bobbing, green spinning ring while running, amber when paused.
- Panel closes by itself when Roblox is closed or left.
- Credits: creator's Roblox avatar loaded from the internet (shows the logo offline).

## Bugs
- Cast: the panel was still on screen for 450 ms when Start was pressed, so the first Cast tap hit the panel. Now removed instantly, first cast waits 0.28 s.
- Cast / X / Sell taps are re-sent up to 3x when Android cancels or refuses them; anti-AFK no longer interrupts a running press.
- Clicker circles: Android could shift the overlay window (camera notch, bars) so the saved spot differed from the circle. Now the real on-screen position is measured, corrected and saved.

## Detection
- ImageReader: 3 buffers, GPU-friendly hardware buffers on Android 10+, capture fps meter.
- OpenCV: bulk Mat load (no per-pixel loop), Mats reused between scans.
- Adaptive speed (panel toggle): scan detail follows capture fps, scan time and hit rate. ROI box grows before falling back to a full scan.
- Stats page shows capture fps and scan detail.

Not compiled or run on a phone here (no Android SDK). The GitHub build is the first compile: send the error line if it fails.
