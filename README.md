# Data Preparation

1. Create a folder named `SynSeg_dataset`.

2. Download the dataset from [Jarch-ma/FSS_Dataset](https://huggingface.co/datasets/Jarch-ma/FSS_Dataset) and simply unzip it.

---

# Environment Configuration

## 1. Creating a Conda Environment

```bash
conda env create -n SynSeg python=3.10
```

## 2. Install Torch

Depend on your CUDA version.

### CUDA 11.8

```bash
pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1 --index-url https://download.pytorch.org/whl/cu118
```

### CUDA 12.4

```bash
pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1 --index-url https://download.pytorch.org/whl/cu124
```

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## 4. Install Flash-Attention

```bash
pip uninstall -y ninja && pip install ninja
pip install flash-attn --no-build-isolation
```

## 5. Install SAM

Then delete the folder.

```bash
git clone https://github.com/facebookresearch/sam2.git && cd sam2
pip install -e .
```
