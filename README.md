# ABA-FWI
ABA-FWI is an algorithm of augmented Boundary Attention for Full Waveform Inversion.  The spatial attention module (SAM) is incorporated into every stage of resolution enhancement in the decoder.  In addition, the reflection coefficient tuned boundary loss (RCTB loss) is designed to supplement the penalty for boundary misfit.  

1. This project includes the code implementation of ABA-FWI, as well as comparative experiments InversionNet and VelocityGAN, and ablation experiments ABA-Net and ABA-Loss.The loss functions for the comparative experiments consist of joint L1 and L2 losses. The following is correspondence between ablation experiments and code:
1.1 ABA-Net = IAEDN + L1 and L2 losses;
1.2 ABA-Loss = InversionNet + RCTB Loss;
1.3 ABA-FWI = IAEDN + RCTB Loss.

2. Corresponding code files for training and validation methods:
2.1 train_valid_Inversion.py  --------> InversionNet   ABA-Net;
2.2 train_valid_Inversion_TV.py -------->  ABA-Loss ABA-FWI;
2.3 train_valid_velocityGAN.py -------->  VelocityGAN.

3. Test code files:
test_Inversion.py  --------> InversionNet  VelocityGAN  ABA-Net  ABA-Loss ABA-FWI
