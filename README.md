# led_matrix_helpers_bash

A collection of utilities to prep or modify video files to be played on an LED matrix

## Usage

**Clone the Repository**

```bash
-$ git clone https://github.com/deuxp/led_matrix_helpers_bash.git
```

**OPTIONAL: Make executables globally available:**

**Mac & linux**

```bash
-$ sudo [executable] chmod +x && mv [executable] /usr/local/bin/[executable]
```

## Utility

### ledsca

Short for `LED scaler` This utility will scale a video to the size of the LED matrices configuration while preserving the original aspect ratio.
All 4 flags are mandatory.

```bash
-$ cd led_matrix_helpers_bash/src/
-$ ledsca -i [INPUT_FILE] -o [OUTPUT_FILE] -w [WIDTH] -h [HEIGHT]
```

For best results, map the size of the video (pixels).
ie., if your matrix is 64x64, scale the video to 64 x 64 pixels:

```bash
-$ cd led_matrix_helpers_bash/src/
-$ ledsca -i [INPUT_FILE] -o [OUTPUT_FILE] -w 64 -h 64
```

## Dependencies

-   [ffmpeg](https://ffmpeg.org/download.html)
