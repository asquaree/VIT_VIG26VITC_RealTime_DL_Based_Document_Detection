For real time instance segmentation we came to yoalact++. We mainly went for this approach in two subtasks
(i) generating a set of prototype masks
(ii) predicting per instance mask coefficients.
Then we produce instance masks by linearly combining the protypes with mask coefficients. We find that the 
process doesn't depend on repooling this approach produces very high quality masks and exhibit stability.
We use resnet 50 model that runs at 33.5 fps. In order to use yolact++ , we compile DCN version 2 code.

We downloaded coco dataset to train our model , further we downloaded pretrained weights to test our datset.

The output we were getting with pretrained weights. The photos segments the documents and in video it is
detecting the object in real time. We could not work on custom dataset. So we move to mask rcnn our final
algorithm.


For testing dataset we used 160 images from the link below
https://drive.google.com/file/d/18hMcTt5efzKua-Ikua2B80kcHsC_wydD/view?usp=sharing