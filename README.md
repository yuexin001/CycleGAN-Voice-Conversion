

# CycleGAN Voice Conversion

### Repo: Project for DD2424

### Paper and Dataset

**Paper：**[CycleGAN-VC: Non-parallel Voice Conversion Using Cycle-Consistent Adversarial Networks  ](https://ieeexplore.ieee.org/abstract/document/8553236?casa_token=nEkt-SBQoPoAAAAA:9VLqcVdeP_O4Cuhr6GLreLo8Y8Ph1eo0SGdVwd_24Dq0PaAEnEmjIpZQ6PkulcoH92zcbL4)

**Dataset：**[VCC2018](https://erepo.uef.fi/handle/123456789/7185)

<br/>

### Model Structure

![image](https://github.com/alpharol/Voice_Conversion_CycleGAN/raw/master/figure/CycleGAN.png)

*Note: The channel of residual block may be wrong in the origin paper.* 

<br/>

### Dependencies

tensorflow 1.14.0

PyWorld 0.2.8

numpy 1.15.4

librosa 0.5.1

<br/>

### File Structure

```bash
|--convert.py
|--model.py
|--module.py
|--preprocess.py
|--train.py
|--utils.py
|--data--|vcc2016_training
       --|evaluation_all
```

<br/>

### Usage

#### Preprocess

```python
python preprocess.py
```

<br/>

#### Train

```python
python train.py
```

If the other speakers are involved, please change the directory below.

```bash
train_A_dir_default = './data/vcc2016_training/SF1'
train_B_dir_default = './data/vcc2016_training/TM1'
```

<br/>

#### Inference

```python
python convert.py
```

The converted voice can be found in the directory below:

```bash
|--converted_voices
```



