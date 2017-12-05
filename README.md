# MS-Celeb-1M WashList
This repository is a slightly cleaner wash list of [MS-Celeb-1M](https://www.microsoft.com/en-us/research/project/ms-celeb-1m-challenge-recognizing-one-million-celebrities-real-world/).
As we know, there are lots of noises in it. For example, some images belong to one celebrity while those are included in other celebrities. Some images are very blurry and even clearly not human faces.

We provide a wash list to clean the dataset, and you can download from [OneDrive](https://1drv.ms/t/s!AlKg0t0qyMOIrOxn0Mg_qbhjXtAf-Q) or [Baidu Yun](https://pan.baidu.com/s/1eS92rBG).

## Some Details

This list is based on [XiangWu's repo](https://github.com/AlfredXiangWu/face_verification_experiment), so it will may be slightly cleaner.

We extracted feature of every image by a CNN, and rudely use hierarchical clustering algorithm to find out the cluster contains the most images in each celebrity folder. The images of this cluster will be regard as no noise data of one celebrity. If the elements of this largest cluster equal or less than 5 images, the whole folder will be dropped.

| Datasets | Celebrities |  Images  |
| :--------: | :--------:| :------: |
| Original Dataset |  99,892  |  8,456,240 |
| XiangWu's Cleaned Dataset |  98,693  |  5,049,825 |
| Our Cleaned Dataset |  80,260 |  4,076,912  |

## Some Results
Before:

![](https://github.com/inlmouse/MS-Celeb-1M_WashList/blob/master/imshow/m.05rjwm_preclean.png)

After(and Aligned)

![](https://github.com/inlmouse/MS-Celeb-1M_WashList/blob/master/imshow/m.05rjwm_clean.png)

## Future Work

- Considering our CNN model is not good enough, this clean list certainly still exist some noises, and some images which are not noises were deleted. We will update this list if we get a better CNN model;
- We will try to find out the over 1000 overlap identities between MS-Celeb-1M and LFW. 


**The released list is only allowed for non-commercial use.**