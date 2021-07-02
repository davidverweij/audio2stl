# audio2stl
Converts an audio file to a 3D spectrogram and (optionally) saves as a stereolithography (STL) file for 3D printing

![example](https://github.com/ChristopherCarignan/audio2stl/blob/master/spec3d.png)

Original code by [Christopher Carignan](https://github.com/ChristopherCarignan)

## Online

Open this repo in a binder (link to follow)

## Offline
Following [this article](https://developers.refinitiv.com/en/article-catalog/article/setup-jupyter-notebook-r)
- Install Python
- Install R
- Open R, and install the R-kernel for Jupyter.
  > When 'Making the kernel available to Jupyter', don't run the command in the R terminal. Instead open your terminal , run `R` followed by `IRkernel::installspec(user = FALSE)`.
- Install packages as shown in [install.R](/install.R) through the R terminal or session in your regular terminal.
- run `jupyter notebook` and run the code within

> If on MacOS, you might need [XQuartz](https://www.xquartz.org/releases/)

## Description:

Converts an audio file to a 3D spectrogram; (optionally) saves as a stereolithography (STL) file for 3D printing

## Arguments:

inputfile (required): filepath string associated with WAV audio file

outputfile (optional): filepath string associated with STL file to save

sampfreq: re-sampling frequency

axisnorm: keep the x- and y-axis scaling (FALSE) or normalize so that they have the same dimensions (TRUE)

preemph: value for pre-emphasis of audio

window: option for windowing audio using a variety of Matlab/Octave compatible filters found in the "signal" package
  ex: 'bartlett', 'blackman', 'hamming', 'hanning', 'triang'
