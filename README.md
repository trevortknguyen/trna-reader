# trna-reader
A project to see if recurrent neural networks can learn to write transcribe tRNA

## Installing Everything

### Anaconda Packages
* numpy
* scipy
* biopython (may come in later)

### Environment PyPi Packages
* tensorflow
* keras

## Windows Installation
We have to use Python 3.5 because Tensorflow for Windows only supports Python 3.5 for now.

If you have an nVidia graphics card, then you can use ```pip install tensorflow-gpu```, but if not, you have to stick with ```pip install tensorflow```.
```
conda create -n trna-env python=3.5
activate trna-env
conda install -y numpy scipy
pip install tensorflow keras
```

# Miscellaneous Things

## BARNACLE stuff
So BARNACLE is going to be the program that turns the tRNA predictions into tertiary structures! It's going to add some more requirements to the project. Unfortunately, the BARNACLE project seems a little dead, but it's all that I can get for now.

BARNACLE requires biopython in order to manage pdb files and it also needs numpy, which is something we already have.

Because BARNACLE is a Python 2.7 library and because the project has to run on Python 3.5, the current version being used is a hacky port from Python 2.7 to Python 3.x. I was debating whether or not to even use BARNACLE because the project seems to be inactive and there currently is not any test coverage for the BARNACLE library in order to ensure the port is stable.

In order to install Barnacle to an Anaconda environment:
```
source activate trna-env
pip install /path/to/barnacle/directory --target /path/to/anaconda/environment
```
Use the ```--upgrade``` flag if necessary.

## PyMol Issues
For some reason, I can't get PyMol to install on any system other than Windows. I keep getting "segmentation fault" on my Debian-based systems. I would really like to use PyMol because it would integrate well with my Python-based project.

I am currently looking at VMD (Visual Molecular Dynamics) as an alternative, but I will be using PyMol on Windows for now.

Some possible molecular visualization software that I may use in the future are listed on the [Biopython Structural Bioinformatics FAQ](http://biopython.org/wiki/The_Biopython_Structural_Bioinformatics_FAQ).
