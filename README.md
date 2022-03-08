# Foreground-speech


This is the Github page for paper 'Automated foreground speech detection in everyday home environments: A transfer learning approach'

The dataset: https://dataverse.tdl.org/dataset.xhtml?persistentId=doi:10.18738/T8/YTHWD4&version=DRAFT

Sample code to unify the labels and perform clustering: demo.ipynb



## Overview

There are two types of features - FFT and embeddings. The FFT features of Participant Group x are under ./fft/P*x*.zip, where *x* is the group index. Similarly, the embeddings of Participant Group x are under ./embeddings/Px.zip.



## Annotation

For groups 1-15:

1 - wearer speech; 2 - background speech from non-wearer participants; m - mixed (wearer & non-wearer) speech; t - television/laptop; p - telephone voice; c - baby sounds/crying; b - non-vocal background; x - ambiguous sounds.

For groups 16-18:

1 - foreground speech (wearer speech + mixed speech); 2 - background sound (sound other than foreground speech types); x - ambiguous sounds.

For more details of the annotation, please refer to our paper.



## The files

### FFT features:
Each FFT file contains one instance of the FFT spectrogram, in a shape of (64x20). The files are named by ./session/seg*i*_label_*y*.csv, where *i* is the temporal index of the instance (in second) for the activity session, and *y* is the sound type label. 

### Embedding features: 
We release two types of embeddings, as described in the paper. Each embedding file contains ALL embedding features of an embedding type per session. The csv files are named by ./emb_type/session.csv, where emb_type refers to the type of embedding features, and session refers to the activity session. The data shape is (T, 513) for emb1 and (T, 1001) for emb2 in each csv file, where T is the total number of embedding vectors for the session (i.e., the temporal size). The features can be accessed at [:, :-1], and the labels can be accessed at [:, -1]. The embeddings are NOT sorted by temporal order.
  


## Citation

Please cite our paper xxx if you use our dataset for your research. Thank you!
