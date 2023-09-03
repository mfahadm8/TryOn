## Useful links
- https://zero10.app/business
- https://medium.com/@yw_nam/%EB%85%BC%EB%AC%B8-%EB%A6%AC%EB%B7%B0-adgan-controllable-person-image-synthesis-with-attribute-decomposed-gan-51f105305297
- https://github.com/sgoldyaev/DeepFashion.ADGAN
- https://drive.google.com/drive/folders/1w1iF7UuI-drXZ1pNLcLg9pPT9Jmky9cy
- https://drive.google.com/drive/folders/0B7EVK8r0v71pQ2FuZ0k0QnhBQnc?resourcekey=0-NWldFxSChFuCpK4nzAIGsg
- https://mmlab.ie.cuhk.edu.hk/projects/DeepFashion/InShopRetrieval.html
- https://medium.com/syncedreview/deepfashion2-a-versatile-benchmark-for-fashion-image-understanding-4b1847518ddd
- https://github.com/TrickyGo/ADGAN-plus-plus
- https://menyifang.github.io/projects/ADGAN/ADGAN.html
- https://github.com/menyifang/ADGAN
# TryOn


## ADGAN
test.sh:
python test.py
--dataroot deepfashion
--dirSem deepfashion
--pairLst deepfashion/fashion-resize-pairs-test.csv
--checkpoints_dir ./checkpoints
--results_dir ./results
--name fashion_AdaGen_sty512_nres8_lre3_SS_fc_vgg_cxloss_ss_merge3
--model adgan
--phase test
--dataset_mode keypoint
--norm instance
--batchSize 1
--resize_or_crop no
--gpu_ids 0
--BP_input_nc 18
--no_flip
--which_model_netG ADGen
--which_epoch 800

folder structure:
ADGAN
├── checkpoints
│   ├── fashion_AdaGen_sty512_nres8_lre3_SS_fc_vgg_cxloss_ss_merge3
│   │   ├── 1000_net_netG.pth
│   │   ├── 800_net_netG.pth
│   │   ├── loss_log.txt
│   │   ├── opt.txt
├── cx
├── data
├── deepfashion
│   ├── fashion-resize-annotation-test.csv
│   ├── fashion-resize-annotation-train.csv
│   ├── fashion-resize-pairs-test.csv
│   ├── fashion-resize-pairs-train.csv
│   ├── resized
│   ├── semantic_merge2
│   ├── semantic_merge3
│   ├── test
│   ├── testK
│   ├── test.lst
│   ├── train
│   ├── trainK
│   ├── train.lst
│   ├── vgg19-dcbb9e9d.pth
│   └── vgg_conv.pth
├── gif
├── losses
├── models
├── options
├── README.md
├── scripts
├── ssd_score
├── test.py
├── tool
├── train.py
└── util