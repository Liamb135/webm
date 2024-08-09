## BPM values for WebMs in dir:

[asciipepe](/asciipepe.webm?raw=true) BPM = 155.84

[asciipepebg](/asciipepebg.webm?raw=true) BPM = 155.84

---

## Tutorials

### Calculate the BPM of a WebM.

Find the duration of the video:
```bash
ffprobe -v error -show_entries format=duration -of default=noprint_wrappers=1:nokey=1 input.webm
```
    -v error                                  # Show only error messages.
    -show_entries format=duration             # Display the duration of the file.
    -of default=noprint_wrappers=1:nokey=1    # Output only the value, without extra formatting.
    input.webm                                # The WebM file to analyze.

**Calculate the BPM**: 
- BPM = 60 / Duration (in seconds)

- Multiply BPM by 2, or 4 for the WebM to play at the correct speed!

---

### Convert GIF to a WebM lossless quality and transparency support.

```bash
ffmpeg -i input.gif -c:v libvpx-vp9 -lossless 1 -pix_fmt yuva420p output.webm

```
    -i input.gif                              # Input GIF file.
    -c:v libvpx-vp9                           # Sets the video codec to VP9.
    -lossless 1                               # Lossless mode to preserve colour and quality.
    -pix_fmt yuva420p                         # Format supports transparency.
    -output.webm                              # The name of the output file.

---

### Remove sound from WebM

```bash
ffmpeg -i input.webm -c:v copy -an output.webm
```
    -i input.webm                             # Input WebM file.
    -c:v copy                                 # Copies the video stream, without re-encoding it.
    -an                                       # Removes all audio streams from the output file.
    -output.webm                              # The name of the output file, without audio.
