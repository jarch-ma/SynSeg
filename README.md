# 1. Data Preparation

1. Create a folder named `SynSeg_dataset`.

2. Download the dataset from [Jarch-ma/FSS_Dataset](https://huggingface.co/datasets/Jarch-ma/FSS_Dataset) and simply unzip it.

---

# 2. Environment Configuration

Please run the following commands to configure the environment:

```bash
# 2. Creating a conda environment
conda env create -n SynSeg python=3.10

# Install torch Depend on your CUDA

# 2.1 CUDA 11.8
pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1 --index-url https://download.pytorch.org/whl/cu118

# 2.2 CUDA 12.4
pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1 --index-url https://download.pytorch.org/whl/cu124

# 3. Install dependencies
pip install -r requirements.txt

# 4. Install flash-attention
pip uninstall -y ninja && pip install ninja
pip install flash-attn --no-build-isolation

# 5. Install SAM then delete the folder
git clone https://github.com/facebookresearch/sam2.git && cd sam2
pip install -e .
```
