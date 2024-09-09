# ABA-FWI
Deep learning full waveform inversion (DL-FWI) is an end-to-end and time-efficient high-resolution imaging technique for subsurface media. Popular methods are often plagued by location drift and significant velocity misfits at the stratigraphic boundaries. In this study, we propose an augmented boundary attention algorithm (ABA-FWI) to focus on the key boundary information. Regarding network composition, the wavelet convolution (WTconv) layer and the spatial attention module (SAM) are incorporated into the encoder and the decoder, respectively. The WTconv layer captures low frequencies by obtaining a large receptive field without suffering from overparameterization. SAM extracts distinctive information by utilizing the inter-spatial relationship of features for resolutionenhancement. For loss function design, our reflection coefficient tuned boundary (RCTB) loss introduces the reflection coefficientto adjust the gradient map weight of low-contrast areas. It focuses on boundary regions characterized by speed transitions to minimize errors. Results on OpenFWI, the SEG simulation, and the Marmousi II slice datasets show that our method is superior to state-of-the-art data-driven methods, especially on boundary details. 

I. This project includes the code implementation of ABA-FWI, as well as comparative experiments InversionNet, VelocityGAN, DD-Net70, DD-Net, FCNVMB, and ablation experiments (ABA-Net and ABA-Loss) .The loss functions for the comparative experiments consist of joint L1 and L2 losses. The following is correspondence between ablation experiments and code:

II. Corresponding code files for training and validation methods:
1) train_valid_Inversion.py  --------> InversionNet   ABA-Net;
2) train_valid_Inversion_TV.py -------->  ABA-Loss ABA-FWI;
3) train_valid_velocityGAN.py -------->  VelocityGAN.

III. Test code files:
test_Inversion.py  --------> InversionNet  VelocityGAN  ABA-Net  ABA-Loss  ABA-FWI
![image](https://github.com/user-attachments/assets/46148544-5e1c-4189-ba48-d276f29d19de)
