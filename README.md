# AbsegNet
Comprehensive evaluation of a deep learning model for automatic organs at risk segmentation on heterogeneous computed tomography images for abdominal radiotherapy (Accepted to [International Journal of Radiation Oncology Biology Physics](https://www.sciencedirect.com/journal/international-journal-of-radiation-oncology-biology-physics)).

## Notes
* This work was modified from [nnUNet](https://github.com/MIC-DKFZ/nnUNet).
* Due to data privacy protection, we can not release all-used hospital datasets, but we released 170 cases for academic research: please contact Xiangde (luoxd1996 AT gmail DOT com) for the dataset or download from [Goole Driven](https://drive.google.com/drive/folders/16qwlCxH7XtJD9MyPnAbmY4ATxu2mKu67?usp=sharing).

## How to use
### 1. Before you can use this package for abdominal OARs segmentation. You should install:
* PyTorch version >=1.8
* Some common python packages such as Numpy, SimpleITK, OpenCV, Scipy......
### 2. Run the inference script.
* Download the trained model (trained based our proposed method) from [Google Drive](https://drive.google.com/file/d/1HdNNO0fKtq_oyyPAW71AmyQZCCeO6TpL/view?usp=share_link).
* Now, you can use the following code to generate 16 OARs delineation.
```python
from InferRobustABOD import Inference3D
Inference3D(rawf="liver_70_img.nii.gz", save_path="liver_70_pred.nii.gz") # rawf is the path of input image; save_path is the path of prediction.
```

<!-- * This project was originally developed for our previous work [RobustNPC](https://www.sciencedirect.com/science/article/pii/S016781402300018X), if you find it's useful for your research, please consider to cite the followings:

        @article{luo2023deep,
        title={Deep learning-based accurate delineation of primary gross tumor volume of nasopharyngeal carcinoma on heterogeneous magnetic resonance imaging: a large-scale and multi-center study},
        author={Luo, Xiangde and Liao, Wenjun and He, Yuan and Tang, Fan and Wu, Mengwan and Shen, Yuanyuan and Huang, Hui and Song, Tao and Li, Kang and Zhang, Shichuan and Zhang, Shaoting and Wang, Guotai},
        journal={Radiotherapy and Oncology},
        volumes={180},
        pages={109480},
        year={2023},
        publisher={Elsevier}
        }
        
or 
```
"Deep learning-based accurate delineation of primary gross tumor volume of nasopharyngeal carcinoma on heterogeneous magnetic resonance imaging: A large-scale and multi-center study." Radiotherapy and Oncology 180, (2023): 109480. Accessed February 6, 2023. https://doi.org/10.1016/j.radonc.2023.109480.
``` -->

## Acknowledgment and Statement
If you have any question, please contact [Xiangde Luo](https://luoxd1996.github.io).
