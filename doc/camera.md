
# Notes

## Test camera with **raspistill**
```bash
raspistill -o tmp.jpg
```

## Use FFmpeg + MIPI CSI Camera to capture video
```bash
# make sure the v4L2 driver is available.
sudo rpi-update 

# load v4L2 driver and create /dev/video0
sudo modprobe bcm2835-v4l2

# capture video
sudo apt install ffmpeg
sudo ffmpeg -f v4l2 -vcodec h264 -r 30 -s 640x480 -i /dev/video0 -vframes 100 tmp.mp4

# playback video
ffplay -i tmp.mp4
```
# Reference

https://picamera.readthedocs.io/en/release-1.13/
