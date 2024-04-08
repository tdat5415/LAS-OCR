# LAS-OCR

OCR model made of using LAS's speller and image encoder.

---

### Example

```python
from model import InferenceModel

model_path = './models/LAS_number_enclstm3_declstm3_3440.pt'
inference_model = InferenceModel(model_path)
```
```python
import matplotlib.pyplot as plt
import cv2

img = cv2.imread(your_img_path)
s, _ = inference_model(img, is_bgr=True, use_beam=True)
print(s)

plt.imshow(img[...,::-1])
```
```
51.55
```
![download](https://github.com/tetrapod0/LAS-OCR/assets/48349693/f1108625-a409-4080-a8fe-2ab333b6c7c9)

---

### Preview
![download](https://github.com/tetrapod0/LAS-OCR/assets/48349693/3d095616-a443-4539-8993-1374e747b3fd)

### Loss Graph
![download](https://github.com/tetrapod0/LAS-OCR/assets/48349693/59e51897-332f-4777-b95e-3074603d34e5)

---

### Reference

[Listen-Attend-and-Spell-Pytorch](https://github.com/AzizCode92/Listen-Attend-and-Spell-Pytorch)

[Chan, William, et al. “Listen, attend and spell.” arXiv preprint arXiv:1508.01211 (2015).APA](https://arxiv.org/pdf/1508.01211.pdf)
