ffmpeg -i input.gif -c:v libvpx-vp9 -b:v 0 -crf 0 -pix_fmt yuva420p output.webm


    -i input.gif: Specifies the input GIF file.
    -c:v libvpx-vp9: Uses the VP9 codec, which is suitable for WebM files.
    -b:v 0: Sets the video bitrate to zero, allowing the -crf option to control the quality.
    -crf 0: Sets the Constant Rate Factor to 0, which is the highest quality setting, effectively making it lossless.
    -pix_fmt yuva420p: Ensures the pixel format supports transparency, which is crucial for maintaining the GIF's transparency in the WebM output.
