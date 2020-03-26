# MIRTools

- [1.Raw Audio Input](#RawAudioInput)
- [2.Low Level Representation](#LowLevelRepresentation)
- [3.Mid Level Representation](#MidLevelRepresentation)
- [4.High Level Representation](#HighLevelRepresentation)


## RawAudioInput
Fundamental part including floating point audio representation in time/frequency domain. The raw input data is often too large, noisy and redundant for analysis.

Down-Mixing
Down-mixing is usually done by simply computing the arithmetic mean over all input channel signals xc{i) per sample i. 

DC-Removal

Normalization

Down-Sampling
## LowLevelRepresentation
(Timbre)
### Temporal Features
* RMS

* ZCR

### Spectral Features
* Log Energy

* Spectral Skewness (statistical property domain)

The spectral skewness measures the symmetry of the distribution of the spectral magnitude values around their arithmetic mean. In general, the more similar the spectral magnitude, the lower the skewness; while the higher the magnitude at fundamental frequency, the more skewed we have.

* SpectralKurtosis (statistical property domain)

The spectral kurtosis measures whether the distribution of the spectral magnitude values is shaped like a Gaussian distribution or not. 

* Spectral Rolloff (spectral shape domain) 

Spectral rolloff measures the bandwidth of the analyzed block of audio sample. It is relatively low in the presence of a tone.

* Spectral Flux (spectral shape domain) 

The spectral flux measures the amount of change of the spectral shape. It is defined as the average difference between consecutive STFT frames; Low results indicates steady-state input or low input levels.(Which is appropriate for onset/novelty detection)


* Spectral Centroid (spectral shape domain) 

The spectral centroid represent the COG(center of gravity) of spectral energy. It is defined as the frequency-weighed sum of the power spectrum normalized by its unweighted sum. Low result indicate significant low-frequency component and low "brightness"

* Spectral Spread, a.k.a Instantaneous bandwidth (spectral shape domain) 

The spectral spread describes the concentration of the power spectrum around the spectral centroid. (or standard deviation of the power spectrum around spectral centroid) Low result indicates the concentration of the spectral energy at a specific frequency region.(e.g. during notes for a monophonic signal), while higher when harmonics appears.

* Spectral Decrease (spectral shape domain) 

The spectral decrease estimates the steepness of the decrease of the spectral envelope over frequency.

* Spectral Slope (spectral shape domain) 

It is calculated using a linear approximation(e.g. linear regression) of the magnitude spectrum.

* Cepstrum (spectral shape domain) 

* MFCC (spectral shape domain) 

The Mel Frequency Cepstral Coefficients (MFCCs) can be seen as a compact description of the shape of the spectral envelope of an audio signal. The main difference to standard cepstrum is the use of a non-linear frequency scale(mel-scale) to mode the non-linear human perception of pitch and the use of the DCT instead of DFT

* Spectral Crest Factor(signal property domain) 

A very simple measure of tonalness compares the maximum of the magnitude spectrum with the sum of this magnitude spectrum. Low results indicate a flat magnitude spectrum and high indicate a sinusoidal.

* Spectral Flatness(signal property domain) 

Spectral flatness is the ratio of geometric mean and arithmetic mean of the magnitude spectrum. Lower results hint toward a non-flat, possibly a tonal spectrum while high results indicate a flat(noisy) spectrum.( Thus spectral flatness is thus a measure of noisiness as opposed to tonaless)

* Tonal Power Ratio(signal property domain) 

A straightforward way of computing the tonalness of a signal is to compute the ratio of the tonal power to the overall power. Low result hint toward a flat(noisy) spectrum or a block with low input level.

* Max of ACF (signal property domain) 

The ACF of a time signal yields local maxima where the ACF lag matches the wavelengths of the signal-inherent periodicities. The less periodic and therefore less tonal the signal is, the lower is the value of such maxima.(non-periodic or periodic?)

* Predictivity Ratio(signal property domain) 

The predicitivity ratio is a measure of how well the audio signal can be predicted by k-order linear prediction

* Autocorrelation Coefficients

The lower the input frequency and the more tonal the singal is, the higher the coefficient is.

* ZCR

The number of changes of sign in consecutive blocks of audio samples. The more often the signal changes, the more high-frequency contnt can be assumed to be in the signal.


## MidLevelRepresentation
(Tonality)arranges sounds according to pitch relationships into inter- dependent spatial and temporal structures.
### Pitch
* Chroma 

Chroma describes the angle of pitch rotation as it traverses the pitch helix
* Tonnets
### Onset

### Key

### Chrod

### Beat

## HighLevelRepresentation
* Style
* Artist
* Mood
* Form

## PostProcessing

* Normalization
* Summarization
