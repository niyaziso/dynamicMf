# 
dynamicMf



######
#Generation of video command #
ffmpeg -r 10 -i correlation_%04d.png -c:v libx264 -vf fps=25 -pix_fmt yuv420p correlation_temporal.mp4
######
