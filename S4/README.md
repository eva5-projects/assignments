EVA5 Batch 2 - Assignment 4 - Solution
======================================

Dataset
--------

MNIST


Description
------------

- 5 Convolution layers with (3x3) kernel and 1 with (1x1) kernel. The number of parameters were reduced with the (1x1) kernel
- Batch normalization and drop-out was applied to the convolution layers.
- Parameter used was 16242.
- Highest Accuracy achieved for an epoch : 99.49%

Final Architecture 
------------------

```
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1            [-1, 8, 28, 28]              80
       BatchNorm2d-2            [-1, 8, 28, 28]              16
         Dropout2d-3            [-1, 8, 28, 28]               0
            Conv2d-4            [-1, 8, 28, 28]             584
       BatchNorm2d-5            [-1, 8, 28, 28]              16
         Dropout2d-6            [-1, 8, 28, 28]               0
         MaxPool2d-7            [-1, 8, 14, 14]               0
            Conv2d-8           [-1, 16, 12, 12]           1,168
       BatchNorm2d-9           [-1, 16, 12, 12]              32
        Dropout2d-10           [-1, 16, 12, 12]               0
        MaxPool2d-11             [-1, 16, 6, 6]               0
           Conv2d-12             [-1, 32, 4, 4]           4,640
      BatchNorm2d-13             [-1, 32, 4, 4]              64
        Dropout2d-14             [-1, 32, 4, 4]               0
           Conv2d-15             [-1, 32, 2, 2]           9,248
      BatchNorm2d-16             [-1, 32, 2, 2]              64
AdaptiveAvgPool2d-17             [-1, 32, 1, 1]               0
           Conv2d-18             [-1, 10, 1, 1]             330
================================================================
Total params: 16,242
Trainable params: 16,242
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.37
Params size (MB): 0.06
Estimated Total Size (MB): 0.44
----------------------------------------------------------------
```

Results
-------

```
epoch=12 loss=0.013219334185123444 batch_id=468: 100%|██████████| 469/469 [00:15<00:00, 29.39it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0221, Accuracy: 9934/10000 (99.34%)

epoch=13 loss=0.06130304932594299 batch_id=468: 100%|██████████| 469/469 [00:16<00:00, 28.96it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0179, Accuracy: 9942/10000 (99.42%)

epoch=14 loss=0.021636178717017174 batch_id=468: 100%|██████████| 469/469 [00:16<00:00, 28.54it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0180, Accuracy: 9945/10000 (99.45%)

epoch=15 loss=0.015911979600787163 batch_id=468: 100%|██████████| 469/469 [00:16<00:00, 28.46it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0189, Accuracy: 9949/10000 (99.49%)

epoch=16 loss=0.03617653623223305 batch_id=468: 100%|██████████| 469/469 [00:16<00:00, 29.03it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0208, Accuracy: 9930/10000 (99.30%)

epoch=17 loss=0.013591603375971317 batch_id=468: 100%|██████████| 469/469 [00:16<00:00, 28.63it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0189, Accuracy: 9938/10000 (99.38%)

epoch=18 loss=0.007915089838206768 batch_id=468: 100%|██████████| 469/469 [00:16<00:00, 28.61it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0181, Accuracy: 9944/10000 (99.44%)

epoch=19 loss=0.021861771121621132 batch_id=383:  81%|████████  | 381/469 [00:13<00:03, 28.78it/s]
```

