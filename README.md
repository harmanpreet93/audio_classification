## Audio Event Detection
Comparative analysis of few popular machine learning and deep learning algorithms for multi-class audio classification.  

### Dataset
We conduct experiments on the General-Purpose Tagging of Freesound Audio with AudioSet Labels ([link](https://zenodo.org/record/2552860#.XfwJ8JNKjOT)) to automatically recognize audio events from a wide range of real-time environments. This dataset consists of heterogeneous uncompressed PCM 16 bit, 44.1 kHz, mono audio files consisting of 41  categories drawn from the AudioSet Ontology (related to musical instruments, human sounds, animals, etc.). For this project, we choose 10 audio classes to run experiments on.  

### Feature Design 
Feature extraction is a fundamental and important step for any machine learning algorithm. We extract features from audio data by computing Mel Frequency Cepstral Coefficients (MFCCs) spectrograms to create 2D image-like patches. MFCC features are derived from Fourier transform and filter bank analysis, and they perform much better on downstream tasks than just using raw features like using amplitude.  

![MFCC Features](https://github.com/harmanpreet93/audio_classification/blob/master/images/audio_features.png)


### Comparative Analysis  
CNNs are capable of excellent results when compared to other machine learning algorithms. Experiments were performed with different batch sizes by training on GPU using Adam optimizer. Batch Normalization was applied after all convolutional layers. Machine learning algorithms such as Naive Bayes and Logistic Regression underfit because they don't have enough capacity to model the complex characteristics of our audio data. An extensive comparison can be found in the report.

![Confusion Matrix](https://github.com/harmanpreet93/audio_classification/blob/master/images/confusion_matrix.png)
