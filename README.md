# MMDet-ObjectDetection

## Installation and Setup

Follow these steps to install and set up the MMDet-ObjectDetection project.

### Prerequisites

- Python 3.10.x
- Pytorch (compatible version)
- CUDA 11.8
- MMCV
- MMDet
- MMYolo

### Step 1: Clone the Repository

```bash
git clone https://github.com/Jayant71/MMDet-ObjectDetection.git
```

### Step 2: Create a Virtual Environment

```bash
conda create -n env_name python=3.10
conda activate env_name
```

### Step 3: Install Dependencies

Only MMDetection -

```bash
pip install  torch==2.1.0 torchvision==0.16.0 torchaudio==2.0.0 --index-url https://download.pytorch.org/whl/cu118
pip install  mmcv==2.1.0 -f https://download.openmmlab.com/mmcv/dist/cu118/torch2.0.0/index.html
pip install  mmdet
```

Both MMDetection + MMYolo

```bash
pip install torch==2.0.0 torchvision==0.15.1 torchaudio==2.0.1 --index-url https://download.pytorch.org/whl/cu118
pip install  mmcv==2.0.1 -f https://download.openmmlab.com/mmcv/dist/cu118/torch2.0.0/index.html
pip install  mmdet
pip install  mmyolo
```

### Step 5: Verify the Installation

```bash
# MMDetection
python -c "import torch; print(torch.__version__); import mmcv; print(mmcv.__version__); import mmdet; print(mmdet.__version__);"
# MMDetection + MMYolo
python -c "import torch; print(torch.__version__); import mmcv; print(mmcv.__version__); import mmdet; print(mmdet.__version__); import mmyolo; print(mmyolo.__version__)"
```

If the setup is correct, you should see the environment information printed out.

```bash
# Output
2.0.0+cu118
2.0.1
3.3.0
0.6.0
```

Few Sample Notebooks are provided modify the dataset and configuration paths before use.

Add you dataset classes in metainfo -

```python
metainfo = {
    'classes': ('Box', ),
}
```

### Additional Resources

For more detailed instructions, please refer to the [MMDetection documentation](https://mmdetection.readthedocs.io/).
