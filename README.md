# [CVPR2022] Thin-Plate Spline Motion Model for Image Animation Windows Installation

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
![stars](https://img.shields.io/github/stars/yoyo-nb/Thin-Plate-Spline-Motion-Model.svg?style=flat)
![GitHub repo size](https://img.shields.io/github/repo-size/yoyo-nb/Thin-Plate-Spline-Motion-Model.svg)

Source code of the CVPR'2022 paper "Thin-Plate Spline Motion Model for Image Animation"

[**Paper**](https://arxiv.org/abs/2203.14367) **|** [**Supp**](https://cloud.tsinghua.edu.cn/f/f7b8573bb5b04583949f/?dl=1)

### Example animation

![vox](assets/vox.gif)
![ted](assets/ted.gif)

### Installation

- Install Anaconda 
- Open ```Anaconda Powershell Prompt```

- Create Anaconda environment:
```bash
conda create --name thin-plate-spline python=3.9
```

- Download this git and place it anywhere you want on your drive, for exemple : ```S:\Python\Projects\thin-plate-spline```

- Create a folder named ```checkpoints```

- Download pretrained models (pick one link)
-- [Tsinghua Cloud](https://cloud.tsinghua.edu.cn/d/30ab8765da364fefa101/)
-- [Google Drive](https://drive.google.com/drive/folders/1pNDo1ODQIb5HVObRtCmubqJikmR7VVLT?usp=sharing)

- Unzip all files on your ```checkpoints directory```, for exemple : ```S:\Python\Projects\thin-plate-spline\checkpoints```

- On Anaconda console type :
```bash
cd S:\Python\Projects\thin-plate-spline
```

- To install the dependencies run:
```bash
pip install -r requirements.txt
```

**Note:** Those without an NVIDIA GPU can add `--cpu` to the command below to use the CPU rather than the GPU

### Image animation demo

```bash
python demo.py --config config/vox-256.yaml --checkpoint checkpoints/vox.pth.tar --source_image assets/source.png --driving_video assets/driving.mp4
```

# Acknowledgments
The main code is based upon [FOMM](https://github.com/AliaksandrSiarohin/first-order-model) and [MRAA](https://github.com/snap-research/articulated-animation)

Thanks for the excellent works!

And Thanks to:

- [@chenxwh](https://github.com/chenxwh): Add Web Demo & Docker environment [![Replicate](https://replicate.com/yoyo-nb/thin-plate-spline-motion-model/badge)](https://replicate.com/yoyo-nb/thin-plate-spline-motion-model) 

- [@TalkUHulk](https://github.com/TalkUHulk): The C++/Python demo is provided in [Image-Animation-Turbo-Boost](https://github.com/TalkUHulk/Image-Animation-Turbo-Boost)

- [@AK391](https://github.com/AK391): Add huggingface web demo [![Hugging Face Spaces](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue)](https://huggingface.co/spaces/CVPR/Image-Animation-using-Thin-Plate-Spline-Motion-Model)
