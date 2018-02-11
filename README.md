## azFace YOLOv2 Face Detector

This is a tiny yolo detector trained on FDDB+Dlib dataset.  It was trained on a GTX1080 for about 82k iterations.  It runs fast at 112 fps on GTX1080 which is more than enough for realtime usage.

## How To Use

### Windows

Clone the repo
```bash
>git clone https://github.com/azmathmoosa/azFace.git
```
CD into the repo
```
>cd azFace
```
Launch yolo_console_dll.exe followed by path to video/image
```
>yolo_console_dll.exe C:\random\video.mp4
```
Or use the darknet executable
```
>darknet.exe detector demo net_cfg\azface.data net_cfg\tiny-yolo-azface-fddb.cfg weights\tiny-yolo-azface-fddb_82000.weights C:\Dataset\random\crowd.mp4
```

### Linux

1. Clone this repo and the [darknet](https://github.com/AlexeyAB/darknet) repo.
2. Follow the instructions of darknet to build it
3. After building use the provided cfg and weight files like so
```
./darknet detector demo net_cfg/azface.data net_cfg/tiny-yolo-azface-fddb.cfg weights/tiny-yolo-azface-fddb_82000.weights /path/to/my/video.mp4
```

## Make your own Videos

To record a video use this command
```
>darknet.exe detector demo net_cfg\azface.data net_cfg\tiny-yolo-azface-fddb.cfg weights\tiny-yolo-azface-fddb_82000.weights C:\Dataset\random\crowd.mp4 -out_filename test.avi
```

You will need DivX codec installed to record and VLC to play the video.

## License

This work is licensed under LGPLv3.  Please attribute to the author incase you find this work useful.

## About Me

In my spare time I offer consultation services for deep learning projects.  If you need assistance for your projects feel free to reach me at `a z m a t h m o o s a @ g m a i l dot c o m`