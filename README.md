# 方法启动方式
1.需要下载并解压TA_MER_FOR_CCAC2024.zip压缩包。
2.需要下载shape_predictor_68_face_landmarks.dat文件，放置到TA_MER/model文件夹下，其链接是: https://pan.baidu.com/s/1V8hyT8kuv3gHjDV7Aug_ig 提取码: nkb6。
3.运行CCAC_TEST.py文件对CCAC_TEST_B数据集预测，在运行前需要设定B榜测试集的位置，例如：本代码设置为”I:\CCAC\test_data_B\test_data_B“。

# 基于局部区域运动时序分析的微表情识别方法
本方法主要分为两步：第一步，提取特征；第二步，分析特征时序信息并进行分类。
在CCAC_TEST.py中通过运行get_ccac_feature.py文件中的get_test_B_feature()函数用于提取特征，并存储到flow_data/ccac_test_B文件夹下。若已经在flow_data/ccac_test_B存储过特征，则不需要重复计算特征。
# Citation
If you find our work useful, please consider citing our paper:
```bash
@article{HE202257,
title = {Micro-expression spotting based on optical flow features},
journal = {Pattern Recognition Letters},
volume = {163},
pages = {57-64},
year = {2022},
issn = {0167-8655},
doi = {https://doi.org/10.1016/j.patrec.2022.09.009},
url = {https://www.sciencedirect.com/science/article/pii/S0167865522002720},
author = {Yuhong He and Zhongliang Xu and Lin Ma and Haifeng Li},
keywords = {Micro-expression spotting method, Farneback optical flow method, Nose tip location-based image alignment, Overlap index},
abstract = {Expression is the changes of facial organs due to facial muscle movement and an important way of human emotional interaction. Neurophysiological studies show that micro-expressions (MEs) are not controlled by subjective consciousness and reflect people's real emotions. That is why MEs have significant value in public security applications. This paper proposes an automatic ME spotting method of high accuracy and interpretability. Firstly, we design the nose tip location-based image alignment method to remove global displacement caused by head shaking. Secondly, according to the action unit definition in the face coding system (FACS), we select fourteen regions of interest (ROI) to capture subtle facial movements. The dense optical flow is introduced to estimate local movements and time-domain variations of the ROIs. Thirdly, we design a peak detection method on the time-domain variation curves to locate the movement intervals precisely. Lastly, we propose an overlapping index to measure the consistency of changes in different organs. Evaluation on the CAS(ME)2 and SAMM Long Video database shows that our ME spotting method may achieve better accuracy with a relatively lower computation cost and can be applied to similar facial image processing applications.}
}
```
