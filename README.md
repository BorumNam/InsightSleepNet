- Version:
  
  numpy 1.22.4
  
  scikit-learn 1.1.1
  
  python 3.8
  
  pytorch 2.0.0
  
- Necessary dependencies:
  TCN code from: https://github.com/locuslab/TCN

  Energy OOD code from: https://github.com/wetliu/energy_ood
  
  ResNet code from: https://github.com/hsd1503/resnet1d
  
  InceptionTime code from: https://github.com/TheMrGhostman/InceptionTime-Pytorch

  All dependencies must be located within the same directory as the main code.

- Configuration:

  Specify the input path below. Within this path, individual csv files containing continuous PPG samples must be included.

  MESA_PPG_PATH = '/PPG_SleepStaging/MESA_PPG_preprocessed'

  Specify the label path below. Within this path, labels for the continuous PPG samples must be included as individual csv files.

  The names of the individual label csv files should be the name of the ppg input sample csv file with '-profusion' appended.

  MESA_annot_PATH = '/PPG_SleepStaging/MESA_annot_preprocessed'
  
- Input:
  
  10hrs (1200epochs) continuous PPG with shape

  (batch_size=2, time_step=1228800(1200epochs),  feature=1(PPG 1 channel))
  
- Label:

  hypnogram (sleep stages) of 1200 epochs with shape

  (batch_size=2, feature=1, time_step=1200)
  
