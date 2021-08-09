## Pre-requisites

1. Install requirements
   ```
   python3 -m pip install -r requirements.txt
   ```

## Usage

```
usage: python3 inference.py [-h] [-nd] [-cam] [-vid VIDEO] [-s SIZE] [-m MODEL]

optional arguments:
  -h, --help            show this help message and exit
  -nd, --no-debug       Prevent debug output
  -cam, --camera        Use DepthAI 4K RGB camera for inference (conflicts with -vid)
  -vid VIDEO, --video VIDEO
                        Path to video file to be used for inference (conflicts with -cam)
  -s SIZE, --size SIZE  
                        Size of input image. Expect to be a square image
  -m MODEL, --model MODEL 
                        Model path
  -o OUTPUT, --output OUTPUT
                        Name of final video
```

To use with a video file, run the script with the following arguments

```
python3 inference.py -vid ./input.mp4 -s 224 -m resnet18.blob
```

To use with DepthAI 4K RGB camera, use instead

```
python3 inference.py -cam -s 224 -m resnet18.blob -o test.mp4
``` 