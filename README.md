# Foreground-speech

=====

This is the Github page for paper 'Automated foreground speech detection in everyday home environments: A transfer learning approach'

The dataset: https://dataverse.tdl.org/dataset.xhtml?persistentId=doi:10.18738/T8/YTHWD4&version=DRAFT

Sample code to unify the labels and perform clustering: demo.ipynb

=====

There are two types of features - FFT and embeddings. The FFT features of Participant Group x are under ./FFT/Px.zip. The embeddings of Participant Group x are under ./embedding/Px

=====

Label mechanism:

For groups 1-15:

1 - wearer speech; 2 - non-wearer speech; m - mixed speech; t - Television/laptop; p - Telephone voice; c - Baby sounds; b - non-vocal background; x - ambiguous sounds.

For FFT features, the naming format is seg<x>_label_<y>.csv. For embedding features, the features and labels are put together in individual csv files, where [:,:-1] are the features and [:, -1] are the labels. The embeddings are not sorted by label type rather than segment index.
  
 For groups 16-18:
  
 Only three labels are applied: 1 - wearer speech; 2 - non-wearer speech; x - ambiguous sounds.
  
 =====
  
 Please cite paper xxx if you use our dataset for your research. Thank you!
