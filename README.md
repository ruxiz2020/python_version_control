
This documentation answers following question:
# How to do Python version control on a shared cluster?


## Method 1: using virtualenv + jupyter kernel

#### prepare virtualenv
```bash
virtualenv -p python3.7 env
source env/bin/activate
```

#### Install the requirements:

```bash
env/bin/python3 -m pip install --upgrade pip
env/bin/pip install -r requirements.txt
```

#### Bring up ipython notebook using python in virtualenv
```bash
env/bin/pip3 install jupyter
env/bin/ipython kernel install --name "shap3" --user
env/bin/jupyter notebook
```

Then select shap3 from kernel dropdown in jupyter to work inside of the corresponding virtualenv.


## Method 2: using pyenv
