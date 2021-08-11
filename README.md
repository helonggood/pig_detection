# pig_detection
<div align="center">
<p>
<a align="left" href="https://ultralytics.com/yolov5" target="_blank">
<img width="850" src="https://github.com/ultralytics/yolov5/releases/download/v1.0/splash.jpg"></a>
</p>
<br>
<div>

<div align="left">
<details open>
<summary>Introduce</summary>
<p>
	The model_file "last.pt" has been trained for pig detection, it's based on yolov5s and you can use it directly without wasting a lot of time to train, first you should download the latest origin code from following "yolov5 code" url:
</p>
<a href="https://github.com/ultralytics/yolov5">yolov5 code</a>
</details>

<details open>
<summary>How to use</summary>
<p>
	Under the yolov5 project file, you can use this trained pig detection model by following example code:
</p>

```python
import torch
from PIL import Image
img = Image.open('your/path/to/images/8_origin.jpg')
# load model
model = torch.hub.load('ultralytics/yolov5', 'custom', path='your/path/to/model_file/last.pt')
model.conf = 0.25  # confidence threshold (0-1)
# Inference
results = model(img, size=1600, augment=True)
results.show()
```
</details>

<details open>
<summary>Model effect</summary>
<p>
The trained pig detection model metrics/mAP_0.5 is 78.4%, metrics/mAP_0.5:0.95 is 33.0%, metrics/precision is 78.5%, metrics/recall is 70.7%. The measured results are as follows:
</p>
<p>
<img width="850" src="https://github.com/helonggood/pig_detection/blob/main/images/8_origin.jpg"></a>
<img width="850" src="https://github.com/helonggood/pig_detection/blob/main/images/8_detected.jpg"></a>
</p>
<br>

</details>

<div>
