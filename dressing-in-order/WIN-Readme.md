
### Jupyter notebook Cuda Issues
Run the following command in terminal and in Jupyter notebook:

```
torch.cuda.is_available()
```

If aforementioned command returns True but in Jupyter notebook, it returns false and you have cuda then you will have to create a new kernal rather than just using python venv.
Commands:
```
pip install jupyter
jupyter notebook --ip localhost --port 3001 --no-browser
```
The last command will output local jupyternotebook kernal url. Copy it.
Now Select the current from top right of jupyternotebook and select jupyter kernal, enter url and select the python env

### Torch Installation
Note the cuda version installed using nvidia-smi command and change it in index-url link, mine was cuda 12.2 however there was no torch url for that but still 12.1 worked for me
pip3 install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cu121

### SciKit Installation or Missing Draw package 
In case you face issues with scikit image installation, you can use following combination.
```
python3.9 -m pip install scikit-image==0.18.0
```