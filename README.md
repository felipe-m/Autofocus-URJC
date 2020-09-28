# Autofocus

This is an open source project to develop a fully automated focusing system.


  INTRODUCTION

The original idea came up at the URJC with the QUASAR project, developed in collaboration with Cytognos S.L. and UNAV. The project aimed to create an hiperspectral histo-citometer which, in a few words, is like a fancy microscope.

This inspirated us to develop a general methodology and any-kind-of-application implementation for an autofocus solution. We are in the process of publishing a paper about this, but long story short, to focus a sample you need to sweep each field of view though the focal range to take a stack of images. Then, you use these images to calculate the contrast function of the stack, and its maximum would indicate the best focused position.

How do you calculate the contrast function of the stack? With a contrast calculation algorithm, of course! But there is a problem: there are many contrast calculation algorithms available, and the optimal one for a certain use varies with the sample and its content.

Then, we have to develop some kind of tool capable of selecting the best algorithms to use in a given application. And this is our first step: the creation of an automated analysis that studies a series of stacks with a set of algorithms. The analysis evaluates the performance of the algorithms and grades them, giving as a result a global ranking of those algorithms.

This is only the first step, and at this point our goal is to test the efectiveness of the analysis and its reliability. For this study we used 150 stacks of images, from 4 different types of mouse tissue (adipose, stomach, intestine and kidney), using 2 magnification settings (5x and 10x), and 2 bit-depth configurations (8 bits and 16 bits).

Those images were studied with 15 algorithms and evaluated according 4 criteria (accuracy, range, false maxima and FWHW) by 2 different analysis (semi-quantitative and quantitative), and the developed tool for this implementation, along with the datasets studied and the results ara availabe here. More details can be found in the following paragraphs.


  MATHERIALS

1- Images
  The images used to test our project can be found in the following link:
  
  https://urjc-my.sharepoint.com/:f:/g/personal/marina_bsanz_urjc_es/EjYdL3WWrCBBpagt8AJ16Q0BFZuvUiw87Da-EJ6MptLGLw?e=qyPgA5
  
  There are 150 stacks of images, taken from 4 different types of mouse tissue (adipose, stomach, intestine and kidney), using 2 magnification settings (5x and 10x), and 2 bit-depth configurations (8 bits and 16 bits). The images are .tif in greyscale and have a resolution of 1388x1040, and are filed as follows:
  
  
