# ABA-FWI
ABA-FWI is an algorithm of augmented Boundary Attention for Full Waveform Inversion.  The spatial attention module (SAM) is incorporated into every stage of resolution enhancement in the decoder.  In addition, the reflection coefficient tuned boundary loss (RCTB loss) is designed to supplement the penalty for boundary misfit.  

I. This project includes the code implementation of ABA-FWI, as well as comparative experiments InversionNet and VelocityGAN, and ablation experiments ABA-Net and ABA-Loss.The loss functions for the comparative experiments consist of joint L1 and L2 losses. The following is correspondence between ablation experiments and code:
1) ABA-Net = IAEDN + L1 and L2 losses;
2) ABA-Loss = InversionNet + RCTB Loss;
3) ABA-FWI = IAEDN + RCTB Loss.

II. Corresponding code files for training and validation methods:
1) train_valid_Inversion.py  --------> InversionNet   ABA-Net;
2) train_valid_Inversion_TV.py -------->  ABA-Loss ABA-FWI;
3) train_valid_velocityGAN.py -------->  VelocityGAN.

III. Test code files:
test_Inversion.py  --------> InversionNet  VelocityGAN  ABA-Net  ABA-Loss ABA-FWI
