[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rezaakb/VizWiz-Classification-Dataset/blob/main/eval.ipynb)

# VizWiz-Classification

![VizWiz-Classification Cover Image](http://drive.google.com/uc?export=view&id=1EyB5mB37DIPbZ-qbHnd3DxxK7_tqiAA3)

## Introduction

VizWiz-Classification is a new test set using 8,900 images taken by people who are blind for which we collected metadata to indicate the presence versus absence of 200 ImageNet object categories. Please read our paper to learn more:

[A New Dataset Based on Images Taken by Blind People for Testing the Robustness of Image Classification Models Trained for ImageNet Categories.
Reza Akbarian Bafghi, and Danna Gurari. CVPR, 2023.](https://openaccess.thecvf.com/content/CVPR2023/papers/Bafghi_A_New_Dataset_Based_on_Images_Taken_by_Blind_People_CVPR_2023_paper.pdf)


## Dataset download

Before you can use our sample code, you must download the dataset (~20GB). Links to download the images and annotations are available [here](https://vizwiz.org/tasks-and-datasets/image-classification).

Alternatively, you can run this shell script. This will create a directory `dataset` with all the files in your current directory. This may take a while.
```
$ sh download_dataset.sh
```

## Installation

Please run the following command to install the library for testing pre-trained models from [PyTorch Image Models](https://github.com/rwightman/pytorch-image-models) on our dataset.
```
$ pip install timm
```

## Evaluation
After downloading the dataset, you can run this code.

```
$ python eval.py 
```

Or, you can set variables in this way.
```
$ python eval.py --model_name vgg19 --images_path dataset/images --ann_path dataset/annotations.json --batch_size 64 --prediction_path predictions
```

After the prediction file is generated, you should upload it to our [EvalAI](https://eval.ai/web/challenges/challenge-page/1999/overview) server for evaluation. Instructions on how to do it are provided [here](https://vizwiz.org/tasks-and-datasets/image-classification).

## Citation

If you make use of our dataset for your research, please be sure to cite our work with the following BibTeX citation.
```
@InProceedings{Bafghi_2023_CVPR,
    author    = {Bafghi, Reza Akbarian and Gurari, Danna},
    title     = {A New Dataset Based on Images Taken by Blind People for Testing the Robustness of Image Classification Models Trained for ImageNet Categories},
    booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
    month     = {June},
    year      = {2023},
    pages     = {16261-16270}
}
```

For any questions, comments, or feedback, please send them to [Reza Akbarian Bafghi](https://www.linkedin.com/in/rezaakbarian/) at [reza.akbarianbafghi@colorado.edu](mailto:reza.akbarianbafghi@colorado.edu).
