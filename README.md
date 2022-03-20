# resnet50 based attribute detection
## Requirements
- pytorch 1.4.0
- torchvision 0.5.0
- tqdm 4.43.0
- easydict 1.9
## Dataset
PETA: Pedestrian Attribute Recognition At Far Distance 

## Get Started
1. Create a directory to dowload above datasets. 
     ```
    mkdir data
    ```
3. Prepare datasets to have following structure:
    ```
    /data
        PETA
            images/
            PETA.mat
            README
    ```
4. generate `dataset.pkl`
    ```
    python ./dataset/preprocess/format_peta.py
    ```
5. Train model
    ```
    CUDA_VISIBLE_DEVICES=0 python train.py PETA
    ``` 
