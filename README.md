# MIRTools

- [1.Raw Audio Input](#RawAudioInput)
- [2.Low Level Representation](#LowLevelRepresentation)
- [3.Mid Level Representation](#MidLevelRepresentation)
- [4.High Level Representation](#HighLevelRepresentation)


## RawAudioInput
Fundamental part including floating point audio representation in time/frequency domain. The raw input data is often too large, noisy and redundant for analysis.

## LowLevelRepresentation
(Timbre)
### Temporal Features
* RMS

* ZCR

### Spectral Features
* Log Energy

* Spectral Flux
* Spectral Centroid
* Spectral Spread
* Spectral Flatness
* Spectral Envelope
* ACF 
* Cepstrum

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
