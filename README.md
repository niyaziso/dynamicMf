# dynamicMF
Dynamic Matrix Factorization (dynamicMF) was designed to analyze resource usage statistics obtained regularly for each compute node in High-Performance Computing systems (HPC).

## Compatibility
Code is compatible with tensorflow version 1.4.1 and Python 2.7.14.

## External Data
Because of github repository space limit, we upload data files in the following link:

https://buffalo.app.box.com/s/fa4fcniq25bnjcahob4baifcpo6shvml

Users need to download data files into **Data** folder before running the code.

## Data folder

1. **Zdat.p**: a pickle file that stores tensor with size T x N x M of resource usage statistics of N nodes, M metrics and T time steps. In particular, in this experiment, T = 1000 time steps, N = 1709 nodes and M = 86 metrics. Each metrics has been normalized to standard normal distribution. 

2. **tensortime.csv**: stores the actual clock time corresponding to each time step

3. **nodelist.txt**: the list of names for each compute nodes in Lonestar 4 system. 

4. **metric_names.txt**: the list of metric names used in this experiment

5. **Results**: stores pickles file of resulting factorization for different value of K (K = 3, 5, 10 respectively). For the script to obtain these results, see in the file **dynamicMF.ipynb**

6. **log**: a folder to store the reconstruction error at each time step when running dynamicMF script **dynamicMF.ipynb** for different values of K (K = 3, 5, 10)

## Reproduce Figure 2

By reading recontruction errors in folder **./Data/log/**, visualize the value of objective function in every iteration for different values of K (K = 3, 5, 10). The script to generate this figure is **compare_K.ipynb**

## Reproduce Figure 3

From the resulting factorization, visualize the distribution of node in 10 dimensional latent space at the first time step. For complete view of node distribution throughout a week of data, see the video **./Video/node.mp4**. Each frame in this video is generated in **temporal_node.ipynb**. The first frame in the video is also Figure 2 in the paper.

## Reproduce Figure 4

From the resulting factorization, visualize the correlation between 10 latent dimensions at each time step. Figure 4 shows the correlation at 1st time step. For complete view of correlation throughout a week (resolution is 10 minutes), see the video **Video/corr.mp4**. Each frame in this video is generated in **correlation.ipynb**.

## Reproduce video of correlation between latent dimensions throughout the time

```
ffmpeg -r 10 -i correlation_%04d.png -c:v libx264 -vf fps=25 -pix_fmt yuv420p correlation_temporal.mp4
```


## Reproduce video of nodes representation 

