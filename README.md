# ABA-FWI
ABA-FWI is an algorithm of augmented Boundary Attention for Full Waveform Inversion.  The spatial attention module (SAM) is incorporated into every stage of resolution enhancement in the decoder.  In addition, the reflection coefficient tuned boundary loss (RCTB loss) is designed to supplement the penalty for boundary misfit.  

This project includes the code implementation of ABA-FWI, as well as comparative experiments InversionNet and VelocityGAN, and ablation experiments ABA-Net and ABA-Loss.The loss functions for the comparative experiments consist of joint L1 and L2 losses. The following is correspondence between ablation experiments and code:
ABA-Net = IAEDN + L1 and L2 losses
ABA-Loss = InversionNet + RCTB Loss
ABA-FWI = IAEDN + RCTB Loss

Corresponding code files for training and validation methods:
train_valid_Inversion.py  --------> InversionNet   ABA-Net
train_valid_Inversion_TV.py -------->  ABA-Loss ABA-FWI
train_valid_velocityGAN.py -------->  VelocityGAN

Test code files:
test_Inversion.py  --------> InversionNet  VelocityGAN  ABA-Net  ABA-Loss ABA-FWI
