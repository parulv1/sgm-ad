# Spectral graph modeling reveals global slowing of neurophysiological network transmission in Alzheimer's disease

`Spectrome` is a combination of the words "spectrum" and "connectome". This package is the collection of codes that constructed the analysis for the preprint ["Spectral graph modeling reveals global slowing of neurophysiological network transmission in Alzheimer's disease"](). This repository is developed based on the original model's [repository](https://github.com/Raj-Lab-UCSF/spectrome).

The spectral graph model (SGM) is a brain structure-function model that simulates brain activity power spectrum given a structural connectome. The model is linear, low-dimensional, and provides an analytical relationship between the brain's structural and functional patterns.

## Citation:
The code in this repository is used for the analysis as shown in: Parul Verma, Srikantan Nagarajan, and Ashish Raj. “Spectral graph modeling reveals global slowing of neurophysiological network transmission in Alzheimer's disease” (). If you found this useful, please cite the following:

```
To be updated
```

## Abstract:
Alzheimer's disease (AD) is the most common form of dementia, progressively impairing memory and cognition. While various neuroimaging studies have revealed functional network abnormalities in patients with AD, how these relate to aberrant  neuronal circuit mechanisms remains unclear. We employed a spectral graph-theory model (SGM) to identify abnormal biophysical markers of neuronal activity in AD. SGM is an analytic model that describes how long-range fiber projections in the brain mediate and couple excitatory and inhibitory activity of local neuronal subpopulations. Unlike other coupled neuronal mass models, the SGM is linear, available in closed-form, and parameterized by a small set of global parameters that facilitate rapid and unambiguous model inference. We performed SGM inference with resting state magnetoencephalography (MEG) imaging data on a well-characterized clinical population of patients with AD and a cohort of age-matched controls. We estimated model parameters that best captured the regional power spectra across frequency. Patients with AD had significantly elevated long-range excitatory neuronal time constant, local inhibitory neural gain, and local excitatory time constant. Long-range excitatory time constant had the highest effect size and was also the most important feature for the accurate classification of patients with AD from controls. Furthermore, a higher time constant was associated with a greater decline in global cognition. These results indicate that abnormal spectral signatures in AD can be reliably and succinctly explained by the SGM. Intriguingly, our work is able to recapitulate the spatial and spectral patterns of AD-related functional activity without introducing any spatial heterogeneity; indeed, the SGM model is entirely global and spatially-invariant. This raises the possibility that a global increase in the long-range excitatory time constant might be a sufficient factor underlying observed spatiotemporal alterations of neuronal activity in AD. Our findings provide new insights into potential mechanistic links between abnormal neural oscillations and their cellular correlates in AD.

## Set-up:

First clone the environment to your computer, either download this repo as a `.zip` file or `git clone https://github.com/Raj-Lab-UCSF/spectrome.git`.

Set up a [conda environment](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html) if you do not have all the packages/compatible versions. The list of dependencies is listed in `environment.yml`.

Set-up environment using conda, detailed instructions can be found [here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html). Or after cloning this repository, go to the repo by typing `cd spectrome` and then typing:
`conda env create -f environment.yml`

If conda complains about not finding packages/libraries, make sure `conda-forge` is in the list of channels being searched by `conda`.
You may add `conda-forge` to your list of channels with the command: `conda config --add channels conda-forge`.

The default name of the environment is `spectrome`, activate the environment with `source activate spectrome`, and deactivate with `source deactivate` or `conda deactivate`.

If you want to be able to run `spectrome` from anywhere, just add it's path to your PYTHONPATH. For instance, if you downloaded `spectrome` to `~/Documents/spectrome` do `export PYTHONPATH=$PYTHONPATH:~/Documents/spectrome`. You may have to restart your terminal to make sure this change takes effect.

After completing the set-up for conda environment and `spectrome` path, you may go to the `spectrome` folder and type `jupyter notebook` or `jupyter lab` in your terminal to run the Jupyter notebooks.

## Files:
 - `../spectrome/notebooks`: contains three jupyter notebooks, `run_model_example.ipynb` is the basic simulation of frequency spectrums with optimized parameters for controls and AD. `AD_CONT_stats.ipynb` shows the basic statistical corelations of parameters with MMSE and CDR in AD, and `AD_CONT_classification.ipynb` develops a random forest classifier with the optimized SGM parameters as features of the classifier.

 - `../spectrome/data`: contains intermediate data.
    - `mean80_fibercount/count.csv`: HCP template connectome
    - `mean80_fibercount/length.csv`: HCP template distance matrix.

