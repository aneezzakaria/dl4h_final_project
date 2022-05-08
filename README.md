# Implementation for Improving Clinical Outcome Predictions Using Convolution over Medical Entities with Multimodal Learning
## Usage

* Clone the code to local.

* Pre-processed Output - a preprocessed version of the input file from MIMIC-III with default parameters is available via gcp,
[here](https://console.cloud.google.com/storage/browser/mimic_extract).To access this, you will need to be credentialed for MIMIC-III GCP access through physionet. Instructions for that are available [on physionet](https://mimic.physionet.org/gettingstarted/cloud/).

* Copy the pre processed output file from previous step named all_hourly_data.h5 to data folder.

* Run 01-Extract-Timseries-Features.ipnyb to extract first 24 hours timeseries features from MIMIC-Extract raw data.

* Copy the ADMISSIONS.csv, NOTEEVENTS.csv, ICUSTAYS.csv files into data folder.

* Run 02-Select-SubClinicalNotes.ipynb to select subnotes based on criteria from all MIMIC-III Notes.

* Run 03-Preprocess-Clinical-Notes.ipnyb to prepocessing notes.

* Run 04-Apply-med7-on-Clinical-Notes.ipynb to extract medical entities.

* Download pretrained Word2Vec & FastText embeddings into embeddings folder via https://github.com/kexinhuang12345/clinicalBERT.

* Run 05-Represent-Entities-With-Different-Embeddings.ipynb to convert medical entities into word representations.

* Run 06-Create-Timeseries-Data.ipynb to prepare the timeseries data to fed through GRU / LSTM.

* Run 07-Timeseries-Baseline.ipynb to run timeseries baseline model to predict 4 different clinical tasks.

* Run 08-Multimodal-Baseline.ipynb to run multimodal baseline to predict 4 different clinical tasks.

* Run 09-Proposed-Model.ipynb to run proposed model to predict 4 different clinical tasks.

## References

* https://github.com/tanlab/ConvolutionMedicalNer

* https://github.com/MLforHealth/MIMIC_Extract

* Download Pre-trained Word2Vec & FastText embeddings: https://github.com/kexinhuang12345/clinicalBERT

