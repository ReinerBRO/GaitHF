This repository includes GaitHF's data pretreatment codes for CASIA-B and OU-MVLP gait datasets. 

It is recommended to go to download the dataset and follow the website's instructions to get the password to run the repository.

OU-MVLP: http://www.am.sanken.osaka-u.ac.jp/BiometricDB/GaitMVLP.html

CASIA-B: http://www.cbsr.ia.ac.cn/china/Gait%20Databases%20CH.asp

To prepare CASIA-B dataset for GaitHF pretreatment method
  1. Run：

    python GaitHF_casiab_padding.py -i CASIA-B-raw-path -o GaitHF_CASIA-B_pretreatment-path -x CASIA-B-subjects-info-pub.xls-path
  2. If you are training or testing your model with OpenGait(https://github.com/ShiqiYu/OpenGait), pickled datasets are needed. Run:

    python imagetopkl.py -i GaitHF_CASIA-B_pretreatment-path -o pkled-CASIA-B-datapath

To prepare OU-MVLP dataset for GaitHF pretreatment method
  1. Run OUMVLP_rearrange1.py
  2. Run:

    python GaitHF_OUMVLP_padding.py -i rearrange1-output-path -o GaitHF_OUMVLP_preatreatment-path
  3. Run OUMVLP_rearrange2.py
  4. If you are training or testing your model with OpenGait, pickled datasets are needed. Run:

    python imagetopkl.py -i rearrange2-output-path -o pkled-OUMVLP-path

You could train or test your gait recognition models with prepared datasets and achieve higher accuracies.

Due to database requirements, we provide restricted access to the HI-CASIA-B and HI-OU-MVLP datasets (https://doi.org/10.5281/zenodo.11513494). 
