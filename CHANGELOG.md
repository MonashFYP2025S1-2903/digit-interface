# Changelog

## 2026-09-02 [0.2.1+csiro.1] — CSIRO fork (MonashFYP2025S1-2903)

- `Digit.connect()`: force the V4L2 backend (`cv2.VideoCapture(dev, cv2.CAP_V4L2)`).
  Without an explicit backend, OpenCV picks FFMPEG for a `/dev/videoN` string path,
  and its V4L2 input fails at `get_frame()` with `ioctl(VIDIOC_QBUF): Bad file descriptor`
  on Ubuntu 24.04 + opencv-python 4.x. See the tactile-gap project's DIGIT notes.

## 2021-04-27 [0.2.1]

- Changed location of Digit defaults
- Fixed error when printing device info when not connected

## 2021-04-27 [0.2]

- Added suport for individual control of RGB LED's through firmware version 2.00

## 2020-06-22 [0.1.4]

- Added PyPi support
- Added PyPi CI support
- Improved documentation