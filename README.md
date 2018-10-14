# practical-fastai

It was confused experience overall for the first time using FastAI. Currently, If you wanted to learn some courses in its source code, there would only version 0.07 which is able to support you. Unfortunately, You need to ignore the `fastai 1.0.x` in this case.

So I will show you how to install FastAI on Window 10. At the first name, I found it very strange and right now I am used to it.

- 1. Make sure you have a Nvidia GPU installed and the drivers are set up already.
- 2. [Anaconda](https://www.anaconda.com/download/?lang=en-us#download) need to be installed initially. I installed 64-bit version on my computer. Please check out my tutorial about setting up this over [here](https://github.com/bangoc123/learn-machine-learning-in-two-months/blob/master/essential-installs/vn-windows-python-and-libraries-installations.MD#4-anaconda). 
- 3. If you are a developer, [Git](https://gitforwindows.org/) should be installed already.
- 4. Clone FastAI from Github: `git clone https://github.com/fastai/fastai.git` 
- 5. Go to the FastAI folder and type: `conda env update`
- 6. Activate a designed enviroment with a command:  `activate fastai`
- 7. Add an widget to our jupyter: `jupyter nbextension enable --py widgetsnbextension --sys-prefix`
- 8. This part is quite strange and miserable. You have to to map **fastai** file in the courses to older version 0.7 outside.
  - `cd courses\dl1`
  - `del fastai`
  - `mklink /d fastai ..\..\old\fastai`
  - `cd ..\..`
- 9. Run your notebook and checkout whether fastai was installed or not. Command with `jupyter notebook`
- 10. You need to ensure the correlation between versions of Pytorch and FastAI. Otherwise, you would get some errors about lacking API of Pytorch while running FastAI.
  - `fastai 1.0.x` matches `pytorch 1.0`
  - `fastai 0.7.x` matches `pytorch 0.4.1`

**So please be vigilant about this.**



