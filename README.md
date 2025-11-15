# Mscale-FNO-for-wave-prediction
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![DOI](https://zenodo.org/badge/latestdoi/REPLACE_WITH_ZENODO_BADGE.svg)](https://doi.org/10.5281/zenodo.17359600)

The code for the journal article !["Phase-resolved wave prediction from radar observations based on a multi-scale Fourier neural operator"](https://doi.org/10.1063/5.0301145) by Yaokun Zheng, Alistair G.L. Borthwick, and Zhiliang Lin. 

## Overview



This project uses the multi-scale FNO (MscaleFNO) to predict the future wave evolution based on radar images of sea surface:  
- Direct prediction and multi-task learning (with reconstructing sea surface as additional task)
- MscaleFNO with convolutional block: resolve the performance for high dimensional data (2D,2D+t)

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Inputs and Outputs](#inputs-and-outputs)
- [Citation](#citation)
- [License](#license)
- [Contact](#contact)
- [Acknowledgments](#acknowledgments)

## Installation

### Requirements

- Python
- torch
- numpy
- matplotlib
- cmocean (for plots)
- [neuraloperator](https://github.com/neuraloperator/neuraloperator) 
- [OpenSTL](https://github.com/chengtan9907/OpenSTL) (for runing ConvLSTM or SimVP)

### Setup

As guided in:
- [neuraloperator](https://github.com/neuraloperator/neuraloperator) 
- [OpenSTL](https://github.com/chengtan9907/OpenSTL) for runing ConvLSTM or SimVP


## Usage

Instructions to reproduce results from the paper:
- The input data can be obtained from [zendo](https://doi.org/10.5281/zenodo.17359600), put them at the same folder with codes.
- Run the corresponding notebook, config are within the notebooks.
- The code for metrics and plots are mainly in 'multitask_MscaleFNO.ipynb'.

## Inputs and Outputs

- The input data can be obtained from [zendo](https://doi.org/10.5281/zenodo.17359600)
- The are three folders: in each folder, there are '.mat' files. The name including the corresponding Hs and spreading angle. Within '.mat' file, 'a' stands for input radar scatter, 'e' stands for sea surface, and 'u' stands for future sea surface.

## Citation

If you use this code in your research, please cite:

```bibtex
@article{YourArticle2025,
  author    = { Yaokun Zheng, Alistair G.L. Borthwick, and Zhiliang Lin},
  title     = {Phase-resolved wave prediction from radar observations based on a multi-scale Fourier neural operator},
  journal   = {Journal Name},
  year      = {2025},
  doi       = {10.XXXX/XXXXXXXX}
}
```

As well as the following libraries:

- OpenSTL:
    ```bibtex
    @inproceedings{tan2023openstl,
      title={OpenSTL: A Comprehensive Benchmark of Spatio-Temporal Predictive Learning},
      author={Tan, Cheng and Li, Siyuan and Gao, Zhangyang and Guan, Wenfei and Wang, Zedong and Liu, Zicheng and Wu, Lirong and Li, Stan Z},
      booktitle={Conference on Neural Information Processing Systems Datasets and Benchmarks Track},
      year={2023}
    }
    ```
- neuraloperator:
    ```bibtex
    @misc{kossaifi2024neural,
       title={A Library for Learning Neural Operators},
       author={Jean Kossaifi and Nikola Kovachki and
       Zongyi Li and David Pitt and
       Miguel Liu-Schiaffini and Robert Joseph George and
       Boris Bonev and Kamyar Azizzadenesheli and
       Julius Berner and Anima Anandkumar},
       year={2024},
       eprint={2412.10354},
       archivePrefix={arXiv},
       primaryClass={cs.LG}
    }
    ```

## License

Distributed under the MIT License. See [LICENSE](LICENSE) for more information.

## Contact

- GitHub: [GoostValley](https://github.com/GoostValley)

## Acknowledgments

- This work uses [neuraloperator](https://github.com/neuraloperator/neuraloperator) and [OpenSTL](https://github.com/chengtan9907/OpenSTL).
