# aiy-vision-testing
repo with interesting code to try with google aiy vision and raspberry pi

# Current Goal
Take a local img file, identify objects and draw bounding boxes.

This will require a bonnet-friendly model of many objects with bounding boxes. Should be able to download such a model (probably http://download.tensorflow.org/models/object_detection/ssd_mobilenet_v1_coco_2017_11_17.tar.gz) from the Model Zoo, then use the Bonnet Compiler (https://dl.google.com/dl/aiyprojects/vision/bonnet_model_compiler_2017_12_13.tgz) to convert to a bonnet-friendly model.  We then should be able to mostly use the code from /reference/object_detection.py (although it's not clear to me how the "ANCHORS" factor into this. Does the Bonnet .binaryproto file not include annotation data?  If not, can it be extracted from the frozen model .pb or .pbtxt files?)

# Next Steps
- Take input from live camera
- Write text of name of object onto the output img along with the bounding boxes.

note to self: check out /sys/bus/i2c/drivers/aiy-io-i2c/1-0051/gpio-aiy-io/gpio for pin data. might have something interesting.
