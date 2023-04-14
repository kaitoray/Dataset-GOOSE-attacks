# Dataset GOOSE attacks

There are three types of datasets, Original, Normalised, and Final.

## Original 
Remain as raw datasets collected from the testbed, includes original network traffics (/Network traffics/\*.pcapng), original features extracted from PCAP (/Network traffics/\*.csv), and physical measurement records (/Simulink/\*.csv). There are no labels.

### A total of 31 scenarios were collected, include:
### 15 benign scenarios (training datasets)
* 1 scenario under normal operation (when no events happen) -- label 0
* 10 scenarios under simple emergency operation (when a line-to-line fault happens, related overcurrent protetcion triggered) -- label 101-110
* 4 behaviours under simple emergency operation (when overcurrent protection failed; breaker failure protection triggered) -- label 111-114
### 8 malicious behaviours from IED1 (training datasets)
* 2 false data injection attacks under normal operation -- label 901, 903
* 2 message modification attacks under normal operation -- label 902, 904
* 2 false data injection attacks under emergency operation -- label 905, 907
* 2 message modification attacks under emergency operation -- label 906, 908
### 8 malicious behaviours from IED2 (testing datasets)
* 2 false data injection attacks under normal operation -- label 901, 903
* 2 message modification attacks under normal operation -- label 902, 904
* 2 false data injection attacks under emergency operation -- label 905, 907
* 2 message modification attacks under emergency operation -- label 906, 908



## Normalised 
are normalised datasets after feature engineering process, including format conversion, data merging, data normalisation, feature selection, feature extraction, and most importantly labelling.


## Final
are one-sheet datasets summarised from all benign and malicious scenarios. It includes six groups of datasets which are explained in details below:

|  | Applied sliding window | Labelling methods | # of training scenarios | # of testing scenarios | # of training samples | # of testing samples | # of features | # of different labels |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Group 1 | No | Type 3 | 23 | 8 | 27919 | 9902 | 27 | 10 |
| Group 2 | Time-based | Sequential labelling | 23 | 8 | various | various | 27 | 10 |
| Group 3 | Quantity-based | Sequential labelling | 23 | 8 | various | various | 27 | 10 |
| Group 4 | No | Type 3 | 23 | 8 | 27919 | 9902 | 16 | 10 |
| Group 5 | Time-based | Sequential labelling | 23 | 8 | various | various | 16 | 10 |
| Group 6 | Quantity-based | Sequential labelling | 23 | 8 | various | various | 16 | 10 |


## If you are using these datasets, please cite the paper:
Wang, X., Fidge, C., Nourbakhsh, G., Foo, E., Jadidi, Z., & Li, C. (2022). Anomaly detection for insider attacks from untrusted intelligent electronic devices in substation automation systems. IEEE Access, 10, 6629-6649. https://doi.org/10.1109/ACCESS.2022.3142022  
