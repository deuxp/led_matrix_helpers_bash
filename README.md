# led_matrix_helpers_bash

A collection of utilities to prep or modify video files to be played on an LED matrix

## Usage

**Clone the Repository**

```bash
-$ git clone https://github.com/deuxp/led_matrix_helpers_bash.git
```

**Install Dependencies**
The utilities in this repo depend on the ffmpeg library. Check the version from the command line.

```bash
-$ ffmpeg -version
```

Or you can download it [here](https://ffmpeg.org/download.html).

**Make executable:**

**Mac & linux**

```bash
-$ sudo [executable] chmod +x
```

**Make globally available (optional):**

```bash
-$ sudo mv [executable] /usr/local/bin/[executable]
```

## Utils

### ledsca

Short for `LED scaler` This utility will scale a video to the size of the LED matrices configuration while preserving the original aspect ratio.
All 4 flags are mandatory.

```bash
-$ cd led_matrix_helpers_bash/utils/
-$ ledsca -i [INPUT_FILE] -o [OUTPUT_FILE] -w [WIDTH] -h [HEIGHT]
```

For best results, map the amount of video pixels to the amount of LEDs in your configuration.
ie., if your matrix count is 64x64 LEDs, scale the video to 64x64 pixels as such:

```bash
-$ ledsca -i [INPUT_FILE] -o [OUTPUT_FILE] -w 64 -h 64
```

### play64

Plays a video file using the [led-matrix-repo](https://github.com/hzeller/rpi-rgb-led-matrix/tree/master/utils) with a resolution of 64x64, pre-processed by the latter, ledsca utility.
 

## Dependencies

-   [ffmpeg](https://ffmpeg.org/download.html)
