# Consistent Patch Transformer for Dual-Focused Day and Night Raindrop Removal

<!-- ### [Paper (ArXiv)]() -->

**This repository is the official pytorch implementation of our paper, *Consistent Patch Transformer for Dual-Focused Day and Night Raindrop Removal*.**

[Wenjie Li](https://24wenjie-li.github.io/)<sup>1</sup>,
[Zhenyu Jin]()<sup>1</sup>,
[Heng Guo](https://gh-home.github.io/)<sup>1</sup>,
[Zhanyu Ma](https://zhanyuma.cn/publications/index.html)<sup>1</sup> <br>

<sup>1</sup>[PRIS Lab](https://github.com/PRIS-CV), Beijing University of Posts and Telecommunications (BUPT).

---
## Contents

The contents of this repository are as follows:

1. [Dependencies](#Dependencies)
2. [Train](#Train)
3. [Test](#Test)

### Dependencies

> - Python (>=3.8)
> - Pytorch (2.4.1+cu118)
> - basicsr (1.4.2)
> - numpy==1.24.4

```
# For install basicsr
pip install basicsr==1.4.2

python setup.py develop -i http://mirrors.aliyun.com/pypi/simple/

pip install -v -e .

python -m pip install --upgrade pip

numpy==1.24.4
```

extra infos: 
> - [BasicSR](https://github.com/XPixelGroup/BasicSR)

### Train

```
# For Train
torchrun --nproc_per_node=$GPUS basicsr/train.py -opt options/train_CPT.yml --launcher pytorch
```

### Test

```
# For Test
python basicsr/test.py -opt options/test_CPT.yml
```

## Results

- **Pretrained models and visual results**

| Results |                                                                                          Model Zoo                                                                                           |                                                                                         Visual Results                                                                                          | 
| :----- |:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
                                                                                            |
| Ours | [Link]() | [Google Drive](https://drive.google.com/file/d/1ZjnuC7L73snKOleSlPmE4JRmTTzMH-L8/view?usp=drive_link)|


## Acknowledgement

The foundation for the training process is [BasicSR](https://github.com/XPixelGroup/BasicSR) , which profited from the outstanding contribution of [XPixelGroup](https://github.com/XPixelGroup) .

The following research forms the foundation for the CPT implementation:

> _Restormer: Efficient Transformer for High-Resolution Image Restoration_ [paper](https://arxiv.org/abs/2111.09881) [github](https://github.com/swz30/Restormer)

> _Improving Image Restoration by Revisiting Global Information Aggregation_ [paper](https://arxiv.org/abs/2112.04491) [github](https://github.com/megvii-research/TLC)


## Contact

This repo is currently maintained by Wenjie Li ([@WenjieLi](lewj2408@gmail.com)).
