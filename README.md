# Face Recognition with ArcFace 
Uses a smaller version of the Asian Face Dataset:
- Includes 302 classes and covers 49,615 images for the training process.
- Includes 20 classes and covers 3,776 images for the testing process.

## Prepare data
Upload data 
```bash
├── database
│   ├── profile1_1.png
│   ├── profile1_2.png
│   ├── profile1_3.png
│   ├── ...
```

Clone repository
```bash
!git clone https://github.com/deepinsight/insightface "/content/drive/MyDrive/XuLyAnh/insightface"
%cd /content/drive/MyDrive/XuLyAnh/insightface/recognition/arcface_torch
!pip install -r requirement.txt
```

## Train
```bash
# To run on one GPU
!python train_v2.py configs/ms1mv3_r50_onegpu
#Please note that you need to replace some parameters in the backbone and configs files, hehe =))
```

## Inference
```bash
!python inference.py --network r50 --weight "output/model.pt" --folder "content/test" --path "output_test.npy"

```
## Contributor
**_NGUYEN VAN HOP_**