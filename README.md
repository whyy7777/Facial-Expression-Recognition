![amazing](./amazingkelly.jpeg)

Opensource deep learning framework [TensorFlow](https://www.tensorflow.org) is used in **Facial Expression Recognition(FER)**. 
The trained models achieved 65% accuracy in fer2013. If you like this, please give me a star.

#### Dependencies

FER requires:
- Python (>= 3.3)
- TensorFlow (>= 1.1.0) [Installation](https://www.tensorflow.org/install/)
- OpenCV (python3-version) [Installation](http://docs.opencv.org/master/da/df6/tutorial_py_table_of_contents_setup.html)

Only tested in Ubuntu and macOS Sierra. Other platforms are not sure work well. When problems meet, open an issue, I'll do my best to solve that.

#### Usage
###### demo
To run the demo, just type:
```shell
python3 main.py
```
Then the program will creat a window to display the scene capture by webcamera. You need press <kbd>SPACE</kbd> key to capture face in current frame and recognize the facial expression.

If you just want to run this demo instead of training the model from scaratch, the following content can be skipped.

###### train models
If you want to train a model from scaratch by yourself, download the fer2013 datasets in [kaggle(91.97MB)](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data). Then extract the data to `data/fer2013` folder.

It's is import that modifying the `MODE`(in `main.py`) from `demo` to `train`  before you start training.
Then type:
```shell
python3 main.py
```

#### Issues & Suggestions
If any issues and suggestions to me, you can create an [issue](https://github.com/xionghc/Facial-Expression-Recognition/issues/).

Some tips for who want to use this in 2020
There are many differences between tensorflow2.0 and tensorflow1.x, the latter one is uesd by this project, so this means, if you don't modify codes to tensorflow2.0 style, it's better to look at some tips as follows:
 1: please download python which version is previous version of 3.8, as i tested, only 3.8 can not use opencv module. 
 2: tensorflow2.0 will occured some attributes wrong since this project used tensorflow 1.x, i tried tensorflow1.14.
 3: please add 1 line after all of the import :import os
 											  os.environ["KMP_DUPLICATE_LIB_OK"] = "TRUE".  because of some reason i don't know, this can avoid some operation system errors.
 4: for some complex reason, you can change import tensorflow as tf to import tensorflow.compat.v1 as tf
