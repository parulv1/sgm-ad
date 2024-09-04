# Impaired long-range excitatory time scale predicts abnormal neural oscillations and cognitive deficits in Alzheimer’s disease   

`Spectrome` is a combination of the words "spectrum" and "connectome". This package is the collection of codes that constructed the analysis for the preprint ["Impaired long-range excitatory time scale predicts abnormal neural oscillations and cognitive deficits in Alzheimer’s disease "](https://alzres.biomedcentral.com/articles/10.1186/s13195-024-01426-7#Sec1). This repository is developed based on the original model's [repository](https://github.com/Raj-Lab-UCSF/spectrome).

The spectral graph model (SGM) is a brain structure-function model that simulates brain activity power spectrum given a structural connectome. The model is linear, low-dimensional, and provides an analytical relationship between the brain's structural and functional patterns.

## Citation:
The code in this repository is used for the analysis as shown in: Verma et al. “Impaired long-range excitatory time scale predicts abnormal neural oscillations and cognitive deficits in Alzheimer’s disease ” (2024). If you found this useful, please cite the following:

```
@article{verma2024impaired,
  title={Impaired long-range excitatory time scale predicts abnormal neural oscillations and cognitive deficits in Alzheimer’s disease},
  author={Verma, Parul and Ranasinghe, Kamalini and Prasad, Janani and Cai, Chang and Xie, Xihe and Lerner, Hannah and Mizuiri, Danielle and Miller, Bruce and Rankin, Katherine and Vossel, Keith and others},
  journal={Alzheimer's Research \& Therapy},
  volume={16},
  number={1},
  pages={62},
  year={2024},
  publisher={Springer}
}

```

## Abstract:
Background

Alzheimer’s disease (AD) is the most common form of dementia, progressively impairing cognitive abilities. While neuroimaging studies have revealed functional abnormalities in AD, how these relate to aberrant neuronal circuit mechanisms remains unclear. Using magnetoencephalography imaging we documented abnormal local neural synchrony patterns in patients with AD. To identify global abnormal biophysical mechanisms underlying the spatial and spectral electrophysiological patterns in AD, we estimated the parameters of a biophysical spectral graph model (SGM).

Methods

SGM is an analytic neural mass model that describes how long-range fiber projections in the brain mediate the excitatory and inhibitory activity of local neuronal subpopulations. Unlike other coupled neuronal mass models, the SGM is linear, available in closed-form, and parameterized by a small set of biophysical interpretable global parameters. This facilitates their rapid and unambiguous inference which we performed here on a well-characterized clinical population of patients with AD (N = 88, age = 62.73 +/- 8.64 years) and a cohort of age-matched controls (N = 88, age = 65.07 +/- 9.92 years).

Results

Patients with AD showed significantly elevated long-range excitatory neuronal time scales, local excitatory neuronal time scales and local inhibitory neural synaptic strength. The long-range excitatory time scale had a larger effect size, compared to local excitatory time scale and inhibitory synaptic strength and contributed highest for the accurate classification of patients with AD from controls. Furthermore, increased long-range time scale was associated with greater deficits in global cognition.

Conclusions

These results demonstrate that long-range excitatory time scale of neuronal activity, despite being a global measure, is a key determinant in the local spectral signatures and cognition in the human brain, and how it might be a parsimonious factor underlying altered neuronal activity in AD. Our findings provide new insights into mechanistic links between abnormal local spectral signatures and global connectivity measures in AD.

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

