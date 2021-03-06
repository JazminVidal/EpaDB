# Epa-DB: 

This repository contains EpaDB, a database for development of pronunciation assessment systems. The database is an effort of the [Speech Lab](http://habla.dc.uba.ar/) at the Laboratorio de Inteligencia Artificial Aplicada from the Universidad de Buenos Aires and was partially funded by Google by a Google Latin America Reseach Award in 2018.
It is available for free for research purposes. 


## Table of Contents
* [About EpaDB](#About-EpaDB)
* [Overview](#overview)
* [Note on the TextGrid files](#Note-on-the-TextGrid-files)
* [Note on the recordings](#Note-on-the-recordings)
* [References](#references)

## About EpaDB

EpaDB is a speech database intended for research in pronunciation scoring. The corpus includes audios from 50 Spanish speakers (25 males and 25 female) from Argentina reading phrases in English. Each speaker recorded 64 short phrases containing sounds hard to pronounce for this population. Recordings were done in the personal computers of the participants to envison the use case scenario of a pronunciation scoring systems. 

In addition to the recordings, each phrase is manually annotated at phonetic level by two expert annotators from Argentina. One of the annotations is complete, the other covers only four phrases per speaker. We intend to complete the process and also add a third English native annotator in the course of the year.

For more information on the annotations, please refer to the paper. 

## Overview

You will encounter the following folders organized by speaker in the test and train folders:

- waveforms: contains all the speech recordings of the speaker.
- transcriptions: contains the prompts read by the speaker in .lab format.
- annotations_1: contains the set of complete manual annotations in TextGrid format.
- annotations_2: contains a subset of manual annotations in TextGrid format by a second annotator, in case it exists. 
- labels: it is an optional folder that contains the label per phone of each phrase computed by comparing the manual annotation with a reference transcription.

Additional files you will encounter in the main folder are: 

- reference_transcriptions: the file with all the possible reference transcriptions we considered.
- scripts to compute the labels
- a table with the updated annotated symobols in case the change.

## Note on the TextGrid files

Each TextGrid file contains 4 tiers:

- words: manually corrected word level alignments.
- annotation: phone level annotations by the expert annotators.
- score: an overall score provided by the annotator in a scale from 1 to 5.

## Note on the recordings

Note that some of the recordings may be missing due to low quality or recording problems and that recordings may be noisy. Specially spkr14. 
Manual annotation was performed at phone level using ARPA-bet and an ARPA-bet like extension to account for allophonic variations and Spanish sounds. For more informations refer to the paper in this folder.

## License

The database is released under the CC BY-NC 4.0 license, a summary of the license can be found [here](https://creativecommons.org/licenses/by-nc/4.0/), and the full license can be found [here](https://creativecommons.org/licenses/by-nc/4.0/legalcode). For any usage that is not covered by the CC BY-NC 4.0 license, please contact Jazm??n Vidal (jvidal@dc.uba.ar).


## References
If you want to replicate our results in pronunciation scoring using Kaldi-GOP or find a code to compute labels from the manual annotations you can run the code provided in our github repository: https://github.com/JazminVidal/gop-dnn-epadb

If you are interested in using EpaDB in your publications, please cite the following paper:

@article{
vidal2019epadb,????
title={EpaDB: a database for development of pronunciation assessment systems},????
author={Vidal, Jazmin and Ferrer, Luciana and Brambilla, Leonardo},????
journal={Proc. Interspeech 2019},??
pages={589--593},????
year={2019}
}
