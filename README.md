## Show, Attend and Distill: Knowledge Distillation via Attention-based Feature Matching
Official pytorch implementation of ["Show, Attend and Distill: Knowledge Distillation via Attention-based Feature Matching" (AAAI-2021)](http://34.94.61.102/paper_AAAI-9785.html)

## Requirements
- Python3
- PyTorch (> 1.2.0)
- torchvision
- numpy
- Pillow

## Training
We include a trained WRN-40-2 parameters at ```/trained/wrn40x2/model.pth```. \
Run ```main.py``` with student network as WRN-16-2 and teacher as WRN-40-2 to reproduce experiment result on CIFAR100.
```
python main.py --data_dir PATH_TO_DATA --data CIFAR100 --trained_dir /trained/wrn40x2/model.pth\
 --model wrn16x2 --model_t wrn40x2 --beta 200
```
## result  已经验证的

CIFAR 100 数据集

teacher wrn40*2 

student wrn16*2 
 ```
loss_afd 0.0817 * beta(200) = 16
loss_ce :4.6334 
loss_kl 13.4380 * 0.9
```

```
Epoch: 234 |Train Loss: 3.6809 |Train Top1: 0.9197 |Train Top5: 0.9926 |Test Top1: 0.7524 |Test Top5: 0.9386| Time:  79.0 (s)
Epoch: 235 |Train Loss: 3.6793 |Train Top1: 0.9200 |Train Top5: 0.9927 |Test Top1: 0.7534 |Test Top5: 0.9396| Time:  79.8 (s)
Epoch: 236 |Train Loss: 3.6719 |Train Top1: 0.9202 |Train Top5: 0.9932 |Test Top1: 0.7565 |Test Top5: 0.9388| Time:  78.0 (s)
Epoch: 237 |Train Loss: 3.6885 |Train Top1: 0.9186 |Train Top5: 0.9928 |Test Top1: 0.7551 |Test Top5: 0.9380| Time:  78.3 (s)
Epoch: 238 |Train Loss: 3.6878 |Train Top1: 0.9180 |Train Top5: 0.9928 |Test Top1: 0.7547 |Test Top5: 0.9390| Time:  78.8 (s)
Epoch: 239 |Train Loss: 3.6727 |Train Top1: 0.9203 |Train Top5: 0.9934 |Test Top1: 0.7546 |Test Top5: 0.9389| Time:  80.1 (s)
Epoch: 240 |Train Loss: 3.6781 |Train Top1: 0.9209 |Train Top5: 0.9928 |Test Top1: 0.7564 |Test Top5: 0.9377| Time:  79.0 (s)
```
## License

```
Copyright 2021-present NAVER Corp.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
