## 参考

https://github.com/bubbliiiing/unet-pytorch
https://github.com/milesial/Pytorch-UNet.git
https://github.com/jfzhang95/pytorch-deeplab-xception.git

因为刚用github不知道license怎么用，这里标出了参考，若有冒犯,请多海涵


## 使用
trian_utils下的trainModule下的里边的unet存的是完整的训练，验证，测试，以及predict 模板，以此为模板在Customer建立对应的文件见去改<br>


<br>
集成的功能:<br>
   1.常用公开数据集和自定义数据集的载入（公开数据目前已完成cityscapes和pascal voc）<br>
   2.各种数据增强操作<br>
   3.不同模型的训练分离,具体表现为一个模型建立一个文件夹用于存放训练，验证，测试文件以及产生的训练日志和权重文件，
   其中训练日志支持wandb和tensorboard以及log的生成<br>
   4.小功能:模型参数和计算复杂度的计算，统计数据集的均值和方差，统计分割中各类别像素出现的频率以及形成类别权重
   5.分割的标签如果是单通道灰度图的化，支持单通道彩色化，onnx(感觉没用)<br>
   6.支持多种评价指标:iou ,miou,oa,准确率，召回率，dice系数，f1-score,fwiou<br>
   7.可视化,gradcam(能用但是不明白原理),hiddenlayer可视化网络结构（废了这个需要的依赖挺麻烦的）<br>
 
 
<br>
注意:所有新增的有关训练验证和测试的功能,比如新增了一些评价指标什么的 都在trainutils 下的trainModule下的unet示例下设置<br>
实际的训练实例可以按照trainModule下的unet来自主设置<br>


### 现有模型
unet<br>
transunet<br>
espnetv2<br>
mobilenetv2+deeplab<br>
hrnet+ocr<br>
