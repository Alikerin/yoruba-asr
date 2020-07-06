# Yoruba Automatic Speech Recognition (ASR)
This repository contains data and code for the 2020 African Masters in Machine Intelligence (AMMI) Speech Recognition Course. It contains 132 minutes of diacritized Yoruba read speech.

## Data Collection and Processing
A corpus of diacritized Yoruba text containing 1001 sentences was collected from two open-source text corpus available at [https://github.com/Niger-Volta-LTI/yoruba-text]. The first source is a collection of Yoruba proverbs and the second is the JW300, which is a parallel corpus of over 300 languages. The collected text corpus was then processed into a format suitable for LIG-Aikuma [https://lig-aikuma.imag.fr/]: an Android application developed specifically for collecting speech data. The corpus was read into 132 minutes (2 hours and 12 minutes) of speech using the “elicitation from text” feature of LIG-Aikuma. The resulting output formed the dataset for this project.

The data consist of an audio file (in the .wav format) for each sentence in the corpus. The recording was made in 20 different sessions and each session has a file linking the audio file to the corresponding line of text. The text was preprocessed to remove digits and punctuation marks and finally tokenized. A separate file was generated that maps each audio filename to the text that produced it. The preprocessed dataset was splitted into 8, 8, and 4 sessions of training, testing and validation set respectively. This is equivalent to 50, 55, and 27 minutes respectively.

## Model Training
The model training code relies heavily on the implementation of Constrastive Predictive Coding (CPC) available at https://github.com/facebookresearch/CPC_audio.
