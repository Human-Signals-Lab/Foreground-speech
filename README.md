# Foreground-speech


This is the Github page for paper 'Automated foreground speech detection in everyday home environments: A transfer learning approach'

The dataset: https://dataverse.tdl.org/dataset.xhtml?persistentId=doi:10.18738/T8/YTHWD4&version=DRAFT

Sample code to unify the labels and perform clustering: demo.ipynb

=====

# Overview

There are two types of features - FFT and embeddings. The FFT features of Participant Group x are under ./fft/P<x>.zip, where <x> is the group index. Similarly, the embeddings of Participant Group x are under ./embeddings/Px.zip.

=====

# Annotation:

For groups 1-15:

1 - wearer speech; 2 - background speech from non-wearer participants; m - mixed (wearer & non-wearer) speech; t - television/laptop; p - telephone voice; c - baby sounds/crying; b - non-vocal background; x - ambiguous sounds.

For groups 16-18:

1 - foreground speech (wearer speech + mixed speech); 2 - background sound (sound other than foreground speech types); x - ambiguous sounds.

Files of the FFT features are named as seg<segment id>_label_<y>.csv. For embedding features, the features and labels are put together in individual csv files, where [:,:-1] are the features and [:, -1] are the labels. The embeddings are not sorted by label type rather than segment index.
  
 For groups 16-18:
  
 Only three labels are applied: 1 - wearer speech; 2 - non-wearer speech; x - ambiguous sounds.
  
 =====
  
 Please cite paper xxx if you use our dataset for your research. Thank you!
