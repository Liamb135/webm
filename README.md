Convert GIF to a WebM lossless quality and transparency support.

```bash
ffmpeg -i input.gif -c:v libvpx-vp9 -lossless 1 -pix_fmt yuva420p output.webm

```
    -i input.gif           # Input GIF file.
    -c:v libvpx-vp9        # Sets the video codec to VP9.
    -lossless 1            # Lossless mode to preserve colour and quality.
    -pix_fmt yuva420p      # Format supports transparency.
