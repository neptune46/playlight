# OpenCV

## install opencv from binary
```bash
sudo apt update && sudo apt upgrade
sudo apt install python-opencv

# verify installation
python
>>>import cv2
>>>cv2.__version__
```

## install opencv from source code
```bash
sudo apt update && sudo apt upgrade

# install dependencies
sudo apt install build-essential cmake pkg-config
sudo apt install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev
sudo apt install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
sudo apt install libxvidcore-dev libx264-dev
sudo apt install libgtk2.0-dev libgtk-3-dev
sudo apt install libatlas-base-dev gfortran
sudo apt install python2.7-dev python3-dev

# get opencv source code
git clone https://github.com/opencv/opencv.git

# build opencv
mkdir build_opencv
cd build_opencv
cmake -DWITH_IPP=OFF -DWITH_HDF5=OFF ../opencv
make -j4
```