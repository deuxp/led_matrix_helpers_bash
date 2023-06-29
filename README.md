# led_matrix_helpers_bash

A collection of utilities to prep or modify video files to be played on an LED matrix

## Usage

Make any executable globally available.
**Mac & linux**

```bash
-$ sudo [executable] chmod +x && mv [executable] /usr/local/bin/[executable]
```

## Helpers

### ledsca

Short for `LED scaler` This utility will scale a video to the size of the LED matrices configuration. For best results use a 1:1 sizing,
ie., if your matrix is 64x64, scale the video to 64 x 64 pixels.
All 4 flags are mandatory.

```bash
-$ ledsca -i [INPUT_FILE] -o [OUTPUT_FILE] -w [WIDTH] -h [HEIGHT]
```
