# PyTorch-based Person Re-identification Baseline

![Project Demo](show.png)

This repository provides a strong and flexible PyTorch-based baseline for person re-identification (Re-ID) tasks. It is designed to be easily understandable, extensible, and to achieve competitive performance on a variety of Re-ID datasets.

This project is an excellent demonstration of deep learning skills applied to a real-world computer vision problem, showcasing expertise in model training, evaluation, and implementing state-of-the-art techniques.

## 🚀 Key Features

- **State-of-the-Art Models**: Built on top of powerful backbones like ResNet, DenseNet, and Vision Transformers (ViT) via `timm`.
- **Multiple Datasets Support**: Includes easy-to-use data preparation scripts for popular Re-ID datasets such as Market-1501, DukeMTMC-reID, MSMT17, VeRi, and more.
- **Advanced Training Techniques**: Implements modern training strategies like random erasing, label smoothing, and various loss functions including CircleLoss and InstanceLoss.
- **Distributed Training**: Supports Distributed Data Parallel (DDP) for efficient training on multiple GPUs.
- **Re-ranking**: Incorporates post-processing techniques like re-ranking to further boost performance.
- **Easy to Use**: Simple scripts for training, testing, and evaluation.

## 🛠️ Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/Person_reID_baseline_pytorch.git
   cd Person_reID_baseline_pytorch
   ```

2. **Install dependencies:**

   It is recommended to use a virtual environment.

   ```bash
   pip install -r requirements.txt
   ```

## 📚 Dataset Preparation

Before you start training, you need to prepare the datasets. This project provides convenient scripts to download and format several popular Re-ID datasets.

For example, to prepare the Market-1501 dataset, you would typically run a script like:

```bash
python prepare.py
```

Similar scripts are available for other datasets like `prepare_Duke.py`, `prepare_MSMT.py`, etc. Please check the scripts for more details.

## 🏃‍♂️ Training & Testing

### Training

To train a model, you can use the `train.py` script. You can customize the training process by passing various arguments.

```bash
# Example training command
python train.py --name resnet50 --data_dir /path/to/your/dataset --batchsize 32
```

For multi-GPU training, use `train_DDP.py` with the provided shell script:

```bash
./DDP.sh
```

### Testing

Once the model is trained, you can evaluate its performance using `test.py`.

```bash
# Example testing command
python test.py --name resnet50 --test_dir /path/to/your/dataset
```

## ✨ Advanced Features

This repository also includes implementations of several advanced techniques to improve Re-ID accuracy:

- **Random Erasing**: A data augmentation technique to make the model robust to occlusions.
- **Circle Loss**: A state-of-the-art loss function for metric learning.
- **Re-ranking**: A post-processing step to optimize the ranking of retrieved images.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
