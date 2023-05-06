# Solve-MacOS-M1-Tensorflow

## Check Anaconda, Must be arm64
python
```
import platform
platform.platform()
```
if not 'macOS-12.6-arm64-arm-64bit', completely reinstall conda environment


## Step 1
```
conda update conda
```

## Step 2
> if Conflict 

```
conda install --revision 0
```

## Step 3
```
conda install anaconda-clean
anaconda-clean --yes

# remove dir
rm -rf anaconda3
rm -rf ~/anaconda3
rm -rf ~/opt/anaconda3
```

## Step 4
# reinstall arm64 conda
# https://docs.conda.io/en/latest/miniconda.html
or
```
bash ~/miniconda.sh -b -p $HOME/miniconda
source ~/miniconda/bin/activate
conda install -c apple tensorflow-deps
```

# Install base TensorFlow & tensorflow-metal plug-in
```
python -m pip install tensorflow-macos
python -m pip install tensorflow-metal
```


