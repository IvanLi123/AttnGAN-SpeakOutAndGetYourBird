# Speak Out And Get Your Bird -- 2018Fall Final project for CMPT-732

## Introduction

- This is a simple TkInter GUI application that can transform your voice into images.  (Currently only bird supported)
- In this project, we trained a new model that adds additional layer (one discriminator and one generator) on current AttnGAN model, which is aim to increase the image resolution with richer details and higher image quality. Specifically, our model is able to generate a bird image with 512\*512 pixels while the existing AttnGAN model with 256\*256 pixels.
- The major purpose of this app is to let users can interact with our new model in a more directly and user-friendly way.
- What we base on is the AttnGAN Model, the Speech Recognition Package and a WAV recording functionality using pyaudio.
	- https://github.com/taoxugit/AttnGAN 
	- https://pypi.org/project/SpeechRecognition/
	- https://gist.github.com/sloria/5693955
- You can also find our most recently trained model at below url.
	- https://drive.google.com/file/d/1J_fgi0HSPFioG-QUuGa1AWk4pJlG7GZX/view?usp=sharing
- Data
 If you want to train our model yourself, you need:
 Download the [birds] (http://www.vision.caltech.edu/visipedia/CUB-200-2011.html) image data. Extract them to data/birds/
 [DAMSM for bird](https://drive.google.com/file/d/1GNUKjVeyWYBJ8hEU-yrfYQpDOkxEyP3V/view) Download and save it to DAMSMencoders/
- Framework
<img src="framework.png" width="900px" height="1000px"/>

## How to use
### Dependencies
- Please make sure the python version is 2.7 and `pip install` all the following packages.
	- `python-dateutil`
	- `easydict`
	- `pandas`
	- `torchfile`
	- `nltk`
	- `scikit-image`
	- `torch`
	- `pyyaml`
	- `torchvision`
	- `pyaudio`
	
### Samples
<img src="sample.png" width="1154px" height="550px"/>

- Output Birds
<img src="howtouse4.png" width="800px" height="632px"/>

### GUI
- Running Command: cd to code directory
	- python gui.py
  In file gui.py,387 line, you can lower the threshold value. Since in the poster session day, the noise is huge, we set the threshold value higher than usual. You can turn it down a bit to help improve voice recognition accuracy.
- Main Interface
<img src="howtouse1.jpg" width="420px" height="300px"/>
- Voice Input
<img src="howtouse2.png" width="300px" height="222px"/>
- Text Input
<img src="howtouse3.png" width="300px" height="222px"/>

