# Tensorflow Installation Raspberry Pi 4
Installation of Tensorflow on Raspberry Pi 4
#### INSTRUCTIONS
- Open a terminal window
- If remoting into your Raspberry Pi: ssh pi@YOUR PI'S IP ADDRESS HERE

## Make your project directory:
```
cd Desktop
mkdir tf-pi
cd tf-pi
```
## Make a virtual environment (I'm assuming you have Python 3):

```
python3 -m pip install virtualenv
virtualenv tf-env
source tf-env/bin/activate
```
#### Run the commands based on https://github.com/PINTO0309/Tensorflow-bin/#usage:

```
sudo apt-get install -y libhdf5-dev libc-ares-dev libeigen3-dev
python3 -m pip install keras_applications==1.0.8 --no-deps
python3 -m pip install keras_preprocessing==1.1.0 --no-deps
python3 -m pip install h5py==2.9.0
sudo apt-get install -y openmpi-bin libopenmpi-dev
sudo apt-get install -y libatlas-base-dev
python3 -m pip install -U six wheel mock
```

#### Pick a tensorflow release from https://github.com/lhelontra/tensorflow-on-arm/releases (I picked 2.0.0): 
```
python3 -m pip uninstall tensorflow
python3 -m pip install tensorflow-2.0.0-cp37-none-linux_armv7l.whl
```
## RESTART YOUR TERMINAL

### Reactivate your virtual environment:
```
cd Desktop
cd tf_pi
source env/bin/activate
```
## Test:
### Open a python interpreter by executing: python3 
```
import tensorflow
tensorflow.__version__
```
This should have no errors and output: 2.0.0

# Single Script
```
sudo apt-get install -y libhdf5-dev libc-ares-dev libeigen3-dev
python3 -m pip install keras_applications==1.0.8 --no-deps
python3 -m pip install keras_preprocessing==1.1.0 --no-deps
python3 -m pip install h5py==2.9.0
sudo apt-get install -y openmpi-bin libopenmpi-dev
sudo apt-get install -y libatlas-base-dev
python3 -m pip install -U six wheel mock
wget https://github.com/lhelontra/tensorflow-on-arm/releases/download/v2.4.0/tensorflow-2.4.0-cp37-none-linux_armv7l.whl
python3 -m pip install tensorflow-2.4.0-cp37-none-linux_armv7l.whl
```