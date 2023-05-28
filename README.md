# Installing Ardupilot and MAVProxy Ubuntu 20.04


## Clone ArduPilot

```
cd ~
sudo apt install git
git clone https://github.com/ArduPilot/ardupilot.git
cd ardupilot
```

## Install dependencies:
```
cd ardupilot
Tools/environment_install/install-prereqs-ubuntu.sh -y
```

reload profile
```
. ~/.profile
```

## Checkout Latest Plane Build
```
git checkout Plane-4.4
git submodule update --init --recursive
```

Run SITL (Software In The Loop) once to set params:
```
cd ~/ardupilot/ArduCopter
sim_vehicle.py -w
```
# Intalling QGroundControl

```
sudo usermod -a -G dialout $USER
sudo apt-get remove modemmanager -y
sudo apt install gstreamer1.0-plugins-bad gstreamer1.0-libav gstreamer1.0-gl -y
sudo apt install libqt5gui5 -y
sudo apt install libfuse2 -y
```

## [Download QGroundControl.AppImage](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl.AppImage).

```
chmod +x ./QGroundControl.AppImage
./QGroundControl.AppImage
```
