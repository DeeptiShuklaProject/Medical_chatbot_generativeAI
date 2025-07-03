# Medical_chatbot_generativeAI


# How to run?
### STEPS:

Clone the repository

```bash
Project repo: https://github.com/DeeptiShuklaProject/Medical_chatbot_generativeAI.git
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n medibot python=3.10 -y
```

```bash
conda activate medibot
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


(medibot) D:\Medical_chatbot_generativeAI>python
Python 3.10.18 | packaged by Anaconda, Inc. | (main, Jun  5 2025, 13:08:55) [MSC v.1929 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> from pathlib import Path
>>> p = "test/t.py"
>>> Path(p)
WindowsPath('test/t.py')
>>> import os
>>> os.path.split(p)
('test', 't.py')
>>>



then go to setup.py and write below code
from setuptools import find_packages, setup

setup(
    name = 'Medical_chatbot_generativeAI',
    version= '0.0.0',
    author= 'DeeptiShuklaProject',
    author_email= 'deeptishukla515@gmail.com',
    packages= find_packages(),
    install_requires = []

)

# add reuirements.txt .....    -e . then run pip install.r requirements.txt 
then check pip list 
showing project name like "Medical_chatbot_generativeAI 0.0.0       d:\medical_chatbot_generativeai"