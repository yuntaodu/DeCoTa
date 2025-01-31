## [ICCV21: Deep Co-Training with Task Decomposition for Semi-Supervised Domain Adaptation](https://arxiv.org/abs/2007.12684)

<br />
<br />
<img src="https://github.com/LoyoYang/mico/blob/master/overall_framework.png" width="500">

### Requirements
The code is developed under Python 3.6.5 and PyTorch 1.4.0

To install,
```pip install -r requirements.txt```

<br />

### Prepare dataset
To reproduce the DomainNet results, download DomainNet from http://ai.bu.edu/M3SDA/ following the instructions on the page.

Your dataset root is expected to contain folders named after all the domains, for example: 

```PATH-TO-DATASET-ROOT/clipart```

<br />

### Train your own model
There are seven adaptation scenarios in the DomainNet experiment.

Specify the Source and Target domain by either

```--source X --target Y``` or ```--st X_Y_index```

Example to reproduce the DomainNet 3-shot result, from *Real* to *Clipart* (X_Y_index=1), saving checkpoint:

```python
python main.py --root PATH-TO-DATASET-ROOT/ --st 1 --save_check
```

Results will be saved at 
```./record/multi/mico```
Checkpoint will be saved at
```./checkpoint```


<br />

### Eval

Example to evaluate a saved model at iteration 20000 from ```./checkpoint```, from *Real* to *Clipart*:

```python
python main.py --root PATH-TO-DATASET-ROOT/ --st 1 --eval --net_resume Net_iter_model_mico_real_to_clipart_step_20000.pth.tar
```




# TL_seminar

|No.| Time| Title|
|  ----  | ----  | ----|
|Week 1|2021.11.12| Domain adaptation via transfer component analysis|
|Week 2|2021.11.19| Transfer feature learning with joint distribution adaptation|
|Week 3|2021.11.26| 1. How transferable are features in deep neural networks? <br> 2. Learning transferable features with deep adaptation networks|
|Week 4|2021.12.2|Analysis of representations for domain adaptation|
|Week 5|2021.12.9|Unsupervised domain adaptation by backpropagation|
|Week 6|2021.12.16|Maximum classifier discrepancy for unsupervised domain adaptation|



