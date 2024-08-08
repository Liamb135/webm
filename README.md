ffmpeg -i FILE.gif -vf palettegen palette.png

ffmpeg -y -i FILE.gif -i palette.png -vf scale=out_color_matrix=bt709:out_range=tv -pix_fmt yuva420p -bsf:v vp9_metadata=color_space=bt709:color_range=tv -crf 0 FILE.webm
