# Ambulatory-PPG-recordings-Dataset
# Ambulatory-PPG-recordings-Dataset
This dataset contains PPG recordings from 56 ambulatory subjects, which is intended to support the development of approaches for blood pressure estimation by analyzing PPG signals.
## Data Collection
The data were obtained on an outpatient basis, i.e., none of the individuals were hospitalized, and data collection was performed in a laboratory. Each of the 56 recordings in the data set contained a 2-min (120 s) PPG signal. These were sampled at 100 Hz (fs = 100 Hz).
## Data Files
The dataset is distributed in three formats:
1. CSV (comma-separated-value) format
2. Matlab (r) format
3. TXT (text file) format
### CSV Format
Separate CSV files are provided for each recording (where ## is the subject number), containing:

  - PPG_subj_##.csv: the physiological signal data are arranged in a column vector $(n:1)$, where n represents the floating value of the PPG signal for each sample along a single column.

### Matlab (r) format

The files in ".mat" format are independent for each recording (where ## is the subject number), containing:

  - PPG_subj_##.mat: the physiological signal data organized in a row vector $(1:n)$, where n represents the floating value of the PPG signal for each sample along a single row.
## Contributors
For more information about the dataset, please contact the autors at: erick.arguello00@usc.edu.co, santiago.vasquez01@usc.edu.co y luis.delgado01@usc.edu.co 
## Conflicts of interest
The autors have no conflicts of interest to declare.
## References
1. Chobanian, A. V., Bakris, G. L., Black, H. R., Cushman, W. C., Green, L. A., Izzo, J. L., Jr, Jones, D. W., Materson, B. J., Oparil, S., Wright, J. T., Jr, Roccella, E. J., Joint National Committee on Prevention, Detection, Evaluation, and Treatment of High Blood Pressure. National Heart, Lung, and Blood Institute, & National High Blood Pressure Education Program Coordinating Committee (2003). Seventh report of the Joint National Committee on Prevention, Detection, Evaluation, and Treatment of High Blood Pressure. Hypertension (Dallas, Tex. : 1979), 42(6), 1206–1252. https://doi.org/10.1161/01.HYP.0000107251.49515.c2
2. Whelton, P. K., Carey, R. M., Aronow, W. S., Casey, D. E., Jr, Collins, K. J., Dennison Himmelfarb, C., DePalma, S. M., Gidding, S., Jamerson, K. A., Jones, D. W., MacLaughlin, E. J., Muntner, P., Ovbiagele, B., Smith, S. C., Jr, Spencer, C. C., Stafford, R. S., Taler, S. J., Thomas, R. J., Williams, K. A., Sr, Williamson, J. D., … Wright, J. T., Jr (2018). 2017 ACC/AHA/AAPA/ABC/ACPM/AGS/APhA/ASH/ASPC/NMA/PCNA Guideline for the Prevention, Detection, Evaluation, and Management of High Blood Pressure in Adults: Executive Summary: A Report of the American College of Cardiology/American Heart Association Task Force on Clinical Practice Guidelines. Hypertension (Dallas, Tex.: 1979), 71(6), 1269–1324. https://doi.org/10.1161/HYP.0000000000000066
