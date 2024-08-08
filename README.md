    ffmpeg -i input.gif -c:v libvpx-vp9 -lossless 1 -pix_fmt yuva420p output.webm


    -i input.gif: Specifies the input GIF file.
    -c:v libvpx-vp9: Sets the video codec to VP9, which is commonly used for WebM files.
    -lossless 1: Enables lossless mode to preserve the color and quality.
    -pix_fmt yuva420p: Ensures that the pixel format supports transparency (alpha channel).
