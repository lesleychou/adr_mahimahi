# README
Requirements: python3.7

Downgrade python3.8 to 3.7:
```
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt-get update
sudo apt-get install python3.7

ls /usr/bin/python3.7

sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.7 1
sudo update-alternatives --config python3
python3 --version
```
Create venv then install packages:
```
sudo apt-get install python3-pip
sudo pip3 install virtualenv
virtualenv lesvenv
source lesvenv/bin/activate

pip install pyvirtualdisplay selenium numba tflearn
pip install tensorflow==1.14.0
```
