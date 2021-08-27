# README
## Client
### Requirements
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
Enable xvfb on the client
```
sudo apt-get install xvfb
```
Install chrome:
```
wget 'https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb'
sudo dpkg -i google-chrome-stable_current_amd64.deb
sudo apt-get -f -y install
```
Install the latest chromedriver under `adr_mahimahi/pensieve/virtual_browser/abr_browser_dir/`
```
wget https://chromedriver.storage.googleapis.com/92.0.4515.107/chromedriver_linux64.zip
unzip chromedriver_linux64.zip
```
### Run
Update the port inside run_wild.sh, then run:
```
bash pensieve/drivers/run_wild.sh
```

## Server
The video server port need to be inside the open TCP port range. Run:
```
python3 video_server.py --port=10201
```
