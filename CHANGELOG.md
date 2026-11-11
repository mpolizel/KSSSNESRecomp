# Changelog

## 0.1.1 — 2026-11-11

Framework fixes from the later ports and RecompLauncher support. A setting
that needs a restart (renderer, audio output) now comes back to the same
moment instead of starting the game over; a game that reads the controller
by hand gets fresh buttons on every read; a save state loaded in another
scene is no longer drawn with the previous scene's registers. The release
carries a `recomplauncher.json` for
[RecompLauncher](https://recomplauncher.com). Normal play is unchanged (the
test run gives the same pictures, frame by frame); saves and save states from
0.1.0 keep working.

## 0.1.0 — 2026-11-04

First release: a setup pack that recompiles the game from your own ROM. Boots
through the Nintendo and HAL logos, the opening and the title screen into the
game select and the levels, at full speed with the SA-1 running; the in-game
save is kept in `build\saves\save.srm`. Two players (the second controls the
helper). A fresh install starts with no shader (the plain picture); scanline,
CRT and upscaler presets (ScaleFX, NNEDI3) are in Settings → Shader. Settings
during play (Ctrl+L or Select+L3); audio interpolation (I key: Gaussian,
Cubic, Sinc); update check on start that backs up your saves before
installing; asks for the dedicated graphics card on laptops with two;
console-free Windows build.

Framework fixes: the game no longer hangs on a black screen at power on (the
sound chip now runs from power on, so the game finds it and uploads its sound
driver), and stages are drawn with their own colors instead of the status
bar's (palettes reloaded mid-picture are kept per line).
