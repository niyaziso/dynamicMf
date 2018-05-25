# dynamicMF
Dynamic Matrix Factorization (dynamicMF) was designed to analyze resource usage statistics obtained regularly for each compute node in High-Performance Computing systems (HPC).

## Compatibility
Code is compatible with tensorflow version 1.4.1 and Python 2.7.14.

## External Data
Because of github repository space limit, we upload data files in the following link:

https://buffalo.app.box.com/s/fa4fcniq25bnjcahob4baifcpo6shvml

Users need to download data files into **Data** folder before running the code.

## Data folder

## Reproduce Figure 2

## Reproduce Figure 3

## Reproduce Figure 4

## Reproduce video of correlation between latent dimensions throughout the time

```
ffmpeg -r 10 -i correlation_%04d.png -c:v libx264 -vf fps=25 -pix_fmt yuv420p correlation_temporal.mp4
```


## Reproduce video of nodes representation 

