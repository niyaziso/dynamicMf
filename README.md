# dynamicMF
Dynamic Matrix Factorization (dynamicMF) was designed to analyze resource usage statistics obtained regularly for each compute node in High-Performance Computing systems (HPC).

# Compatibility
Code is compatible with tensorflow version 1.6.0 and Python 3.6.4.

# External Data
Because of github repository space limit, we upload data files in the following link:

Users need to download data files into *Data* folder before running the code.




######
#Generation of video command #
ffmpeg -r 10 -i correlation_%04d.png -c:v libx264 -vf fps=25 -pix_fmt yuv420p correlation_temporal.mp4
######
