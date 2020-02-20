# Raspberry Pi Zero W face recognition
Based on https://www.pyimagesearch.com/2018/06/25/raspberry-pi-face-recognition/  

After modifications, run:
```
$ python3 encode_faces.py --dataset dataset --encodings all_crew.pickle --detection-method hog
$ python3 pi_face_recognition.py --cascade haarcascade_frontalface_default.xml --encodings all_crew.pickle
```

** Mods**  
  
1. Added to .bashrc  
```
# for opencv
export LD_PRELOAD=/usr/lib/arm-linux-gnueabihf/libatomic.so.1.2.0
# face_recognition
PATH=/home/pi/.local/bin:$PATH
```
2. Commented out from pi_face_recognition.py  
```
# error thrown on this line
# frame = imutils.resize(frame, width=500)
```
