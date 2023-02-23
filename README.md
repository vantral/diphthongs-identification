# Diphthongs Identification

This repository contains code and data for identifying diphthongs and monophthongs in different languages. The main goal of the project is to propose an automatic method for distinguishing between these two types of sounds and apply it to languages that have been the subject of controversy regarding their phonological systems.

## Data
The repository includes csv tables obtained through the FastTrack plugin for Praat. The languages currently included are:

* Kildin Saami
* Skolt Saami
* Estonian
* Lithuanian

The data was collected during field work. We do not have corresponding permissions to share the audio files, however, the csvs with analyzed data are in free access.

## Methods
The identification of diphthongs and monophthongs is based on a combination of acoustic and statistical features, including formant trajectory length, changepoint detection, and cepstral coefficients. The analysis is performed using Python and the following libraries:

* NumPy
* SciPy
* scikit-learn
* ruptures
* python_speech_features


## File structure
The code is organized into different scripts for data preprocessing and classification.

* `division.ipynb` is responsible for cutting vowels out from marked words
* `changepoint analysis.ipynb` is responsible for ROC, changepoint and trajectory length classification and visualization
* `cepstral_coefficients.ipynb` is responsible for the classification based on cepstral coefficients

`divided` folder contains the data on each language

* `{language}/csvs/` contains csv tables obtained by the FastTrack plugin
* `{language}/file_information.csv` contains information on all audio files used