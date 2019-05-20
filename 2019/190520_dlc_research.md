
# Novelty Detection in NLP


##### Deeplearning campus in Modulabs
###### Created by aisolab ( [@aisolab](https://github.com/aisolab) )

---
# Agenda

- What is Novelty Detection?
- How to solve?
- Applying to NLP
- To do

---
# What is Novelty Detection?

* Deep neural networks (DNNs) can be generalized well when the test samples are from similary distribution (i.e., <span style="color:red">in-distribution</span>)

* However, in the real word, <span style="color:red">there are many unknown and unseen samples</span> that classifier can't give a right anwser

* Novelty detection
	+ Given pre-trained (deep) classifier,
	+ Detect whether a test sample is from in-distribution (i.e, training distribution by classifier) or not (e.g., out-of-distribution / adversarial samples)

---
# How to solve?
* Baseline detector
![Alt text](https://raw.githubusercontent.com/aisolab/Presentation/master/2019/imgs/baseline_detector.png)

---
# How to solve?
* ODIN detector
![Alt text](https://raw.githubusercontent.com/aisolab/Presentation/master/2019/imgs/odin_detector.png)

---
# How to solve?
* Mahalanobis distance-based confidence score
![Alt text](https://raw.githubusercontent.com/aisolab/Presentation/master/2019/imgs/mahala_dist1.png)

---
# How to solve?
* Mahalanobis distance-based confidence score
![Alt text](https://raw.githubusercontent.com/aisolab/Presentation/master/2019/imgs/mahala_dist2.png)

---
# Applying to NLP
* Applying mcb detection to below classfication models


![Alt text](https://raw.githubusercontent.com/aisolab/Presentation/master/2019/imgs/cls_implementation.png)
---
---
# Applying to NLP
* [Convolutional Neural Networks for Sentence Classification](https://arxiv.org/abs/1408.5882)

| 114 class  | tr (133,743) | val (44,581) | tst (9,386) |
| :--------: | :----------: | :----------: | :---------: |
|  softmax   |    96.57%    |    96.20%    |   96.06%    |
| generative |    99.23%    |    98.54%    |   98.42%    |

| ood_tr: 83.86% | precision | recall | f1-score | support |
|----------------------|:---------:|:------:|:--------:|:-------:|
| in distribtuion      |    0.82   |  0.90  |   0.86   |  44,581 |
| out of distribution  |    0.87   |  0.76  |   0.81   |  38,275 |

| ood_val: 82.98% | precision | recall | f1-score | support |
|------------------------|:---------:|:------:|:--------:|:-------:|
| in distribtuion        |    0.79   |  0.90  |   0.84   |  9,386  |
| out of distribution    |    0.89   |  0.76  |   0.82   |  9,569  |
---
# To do
* ensemble MCB features across text classfication model
	* variety tokenization (eg. subword, character, word)
* BERT based 

---