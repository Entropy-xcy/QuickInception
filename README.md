# Quick Application about retraining the Google Inception v3 model
## Abstract
>This repo is a quick demo for beginners to get used to retraining the Google Inception v3 model(or so called Tensorflow for Poets). With this repo, you will be able to quickly configure the environment and do a quick demo about how to classify images using the Inception model.
>For more infos check the Google official docs about 'Tensorflow for Poets'
## Installation
### Ubuntu(x64 only)
```
wget http://entropy-xcy.bid/configure.sh
chmod +x ./configure.sh

# Requires root
./configure 

# you can also use the method same as Windows and Mac OS
```
### Windows and Mac OS
```
# Precondition: Tensorflow(Python) and git are already configured

git clone https://github.com/Entropy-xcy/QuickInception.git
# use git for this repo might be a bit time consuming
```
## Contents
>
>Inception_for_Overwatch
>>bottlenecks `Empty folder to cache the training`
>>
>>data `Image data folder`
>>>Junkrat `Junkrat training images`
>>>
>>>Soldier76 `Soldier76 training images`
>>>
>>>Mercy `Mercy training images`
>>
>>inception `Empty folder to restore the Inception v3 model`
>>
>>label.py `The python program for labeling`
>>retrain.py `The python program for training`

## Training
```
# cd ./QuickInception
# or 
# cd ./Inception_for_Overwatch

python ./retrain.py \
--bottleneck_dir=./bottlenecks \
--how_many_training_steps 4000 \
--model_dir=./Inception \
--output_graph=./retrained_graph.pb \
--output_labels=./retrained_labels.txt \
--image_dir ./data
```
It may take a while to finish the training
After the training 'retrained_graph.pb' and 'retrained_labels.txt' will be generated.
## Labeling
```
# python ./label.py [image]
# for example
python ./label.py ./data/Mercy/pic_123.jpg
```

## Tutorial Video:http://www.bilibili.com/video/av10178446/

## Contact me
#### email:entropy.xcy@hotmail.com
#### qq:554809345
#### Bilibili:http://space.bilibili.com/34270358/

