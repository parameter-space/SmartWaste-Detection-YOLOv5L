# SmartWaste Detection with YOLOv5-L
This repository presents an object detection project utilizing the YOLOv5-L model to accurately identify and classify recyclable waste items in real-world environments.

## Project Overview
- **Task**: Object detection for recyclable materials.
- **Model**: YOLOv5-L (Large variant)
- **Dataset**: Custom-annotated images of recyclable waste.
- **Goal**: Enhance waste sorting efficiency by enabling automatic recognition of recyclable objects.

## Files
- `YOLOV5_TrainedModel.ipynb` : Final training results including performance metrics, training curves, and predictions visualization. provided jupyter notebook
- `README.md` : Project documentation. 

## Key Features
- Custom YOLOv5-L fine-tuning for recyclable item categories.
- Training, validation, and prediction results are provided in an organized HTML report.
- Model adaptable for real-world deployment (e.g., smart recycling bins, industrial waste management).

## Usage
No executable model is provided here.  
This repository is intended to document the final model performance and showcase results.

If you wish to train or infer based on a similar setup:

1. Set up the YOLOv5 environment:
    ```bash
    git clone https://github.com/ultralytics/yolov5.git
    cd yolov5
    pip install -r requirements.txt
    ```

2. Fine-tune using your dataset:
    ```bash
    python train.py --img 640 --batch 16 --epochs 100 --data custom.yaml --cfg yolov5l.yaml --weights yolov5l.pt --name smartwaste
    ```

3. Evaluate the model:
    ```bash
    python val.py --weights runs/train/smartwaste/weights/best.pt --data custom.yaml
    ```

## Notes
- **Training Details**: Batch size, learning rate, augmentation techniques, and additional hyperparameters can be found within the attached HTML report.
- **Model Architecture**: Based on the YOLOv5-L variant architecture, optimized for better precision on mid-sized datasets.

## License
This project is shared for educational and non-commercial research purposes only.

## Reference
- [YOLOv5 GitHub Repository](https://github.com/ultralytics/yolov5)
