# ALSdisMNs
Automated identification of disease motor neurons (disMNs) in histopathological sections from high-content microscopy data

## Overview
This repository contains source code to implement automated identification of MNs exhibiting aberrant phenotype from high-content microscopy data. It contains the raw data as acquired from CellProfiler for both mouse and human spinal cord MNs, two Jupyter notebook allowing to reproduce the figures in manuscript *Automated and unbiased classification of motor neuron phenotypes with single cell resolution in ALS tissue*, Hageman et al. 2020 (BioRxiv). 

## Repository content
* [Scripts](./Scripts): Jupyter Notebook containing `R` and `Python` codes to automatically identify MNs subpopulation from the data.
* [Figures](./Figures): raw figures as outputted by the analysis and used for the paper. 
* [Data](https://zenodo.org/record/3981414#.XzRMxqeB3OQ): folder containing all raw data acquired from CellProfiler on multichanel fluorescent images segmented using the pipeline. This should can be dowloaded from Zenodo under the accession number 3981414.



## Dependencies

It is recommended to create a virtual environment to ensure complete reproducibility of the project, which relies on R (tested on R-3.3.1) and Python (tested on Python 3.5.3).

```R
install.packages(c('data.table', 'dplyr','knitr','chron','colortools','RColorBrewer','corrplot','geneplotter',
             'lme4','beeswarm','rlang','stargazer','viridis','mclust','ape','dendextend','wordcloud','reshape'))
```

Here is how to create a virtual environment called *env* 

1. If virtualenv is not installed, `python3 -m pip install --user -U virtualenv`
1. `cd $MY_PATH` where  `$MY_PATH` is the location of the repository
1. `virtualenv -p ``which python3`` env`
1. `source ./env/bin/activate`
1. `pip3 install --upgrade -r requirements.txt` 

The file `requirements.txt` contains all the Python librariries.


Then you can create and work as you would do normally. The next time 

1. `cd $MY_PATH`
1. `source ./env/bin/activate`


### To work on Jupyter Notebook remotely

On your remote  machine (access via SHH for example):

1. `cd $MY_PATH`
1. `source ./env/bin/activate` 
1. `jupyter notebook --no-browser --port=8786`

On your local machine:

1. `ssh -N -L localhost:8787:localhost:8886 <username@remote.com>`
1. Open your browser on the local machine and type in the address bar: `localhost:8787`







