# Ambulatory-PPG-recordings-Dataset
This dataset contains PPG recordings from 56 ambulatory subjects, which is intended to support the development of approaches for blood pressure estimation by analyzing PPG signals.

## When using this resource, please cite the original publication:
...

## Data Collection
The data were obtained on an outpatient basis, i.e., none of the individuals were hospitalized, and data collection was performed in a laboratory. Each of the 56 recordings in the data set contained a 2-min (120 s) PPG signal. These were sampled at 100 Hz (fs = 100 Hz).

## Description of subjects

56 subjects (22 men and 34 women) were recruited to capture PPG signals and estimate their blood pressure (BP). The average age was 52.48 ± 7.16 years. In addition, information was collected on whether they had been diagnosed with any cardiovascular risk factor and whether they were undergoing any treatment. In the MSExcel file, "Datos_Registros_PPG.xlsx", the information regarding each subject is summarized as follows:
  - Record #: name of the record associated with each individual, 'PPG_subj_##" (where ## is the subject number).
  - Age: range between 44 - 65 years old.
  - Gender: Male or Female.
  - Diagnosed: 'y' for diagnosed, and 'n' for undiagnosed.
  - Treatment: 'y', is under treatment, on the other hand, 'n', isn’t under treatment.
  - Systolic BP: pressure over the arteries when the heart beats (measured in mm Hg)
  - Diastolic BP: pressure between beats when the heart is filling with blood (measured in mm Hg)
  - Heart Rate: number of heart contractions for a given time (measured in BPM).
  - JNC: Classification by JNC 7 guideline (N = normotensive, E = prehypertensive and H = hypertensive)
  - AHA: Classification by AHA 2017 guideline (N = normotensive, E = prehypertensive/elevated and H = hypertensive)

**Note:** A Markdown file for quick table display was also added inside the dataset folder, named [readme.md](https://github.com/sanvsquezsz/Ambulatory-PPG-recordings-Dataset/blob/main/Dataset/readme.md)
## Background of blood pressure classification (JNC and AHA)
Blood pressure is related to the force exerted by the blood on the walls of the blood vessels, and is considered one of the main vital signs of the body. The relationship between high blood pressure (hypertension) and the likelihood of cardiovascular disease has been studied and demonstrated, highlighting hypertension as a major medical and public health problem [1, 2]. Organizations such as the JNC (Joint National Committee on the Prevention, Detection, Evaluation, and Treatment of High Blood Pressure) and the AHA (American Heart Association) have proposed evidence-based clinical guidelines for the prevention and treatment of hypertension.   

The JNC 7 classification introduces the term "prehypertensive" as the designation to identify persons at high risk of developing hypertension (with systolic BP values between 120-139 mm Hg or 80-89 mm Hg of diastolic BP) [1]. Whereas, the 2017 AHA lowered the cutoff values for defining hypertension at 130 mm Hg systolic pressure or 80 mm Hg diastolic pressure [2]. The classification methods of each guide are summarized in the following table.

| **Systolic BP (mm Hg)** |   | **Diastolic BP (mm Hg)** | **JNC 7** | **ACC/AHA 2017** |
| :---------------: | :-: | :----------------: | :---------: | :----------------: |
| <120 | and | <80 | Normal | Normal |
| 120-129 | and | <80 | Prehypertension | Elevated |
| 130-139 | or | 80-89 | Prehypertesion | Stage1/Hypertension|
| 140-159 | or | 90-99 | Stage 1/Hypertesion | Stage2/Hypertension |
| ≥160 | or | ≥100 | Stage 2/Hypertension | Stage 3/Hypertension |


## Data Files
The dataset is distributed in three formats:
1. CSV (comma-separated-value) format
2. Matlab (r) format
3. JSON (JavaScript Object Notation) format
### CSV Format
For CSV format files, two subfolders are provided within the dataset, 'PPG_csv' and 'PPG_csv_info', which contain: 

  - PPG_csv: only the physiological signal data organized in a vector of $(n:1)$ columns for each record, where n represents the floating value of the PPG signal for each sample along a single column. In this subfolder the files are named 'PPG_subj_##.csv' (where ## is the subject number).

### Matlab (r) format

The *PPG_subj_completa.mat* file contains the following subset of the dataset in a single Matlab (r) variable named *data*. The following are provided for each of the 56 recordings:
  - PPG: photoplethysmogram signal. Each signal is provided in a structure, where the *'signal'* field denotes the signal values in a row vector $(1:n)$, and *'fs'* is the sampling     frequency.
  - info: a structure of all variables related to participant information (e.g., ID, age, gender, sys_bp, dis_bp, HR, etc.). 
### JSON format
Separate JSON files are provided for each of the records, 'PPG_subj_##.json' (where ## is the subject number), and contain the following structure:

    {
      "signal": [...],             
      "id": "string id",       
      "age": int,                 
      "gender": "M or F",          
      "diagnosed": "y or n",  
      "treatment": "y or n",  
      "sys_BP": int,   
      "dis_BP": int,  
      "HR": int,   
      "JNC": "N, E or H",          
      "AHA": "N, E or H"           
    }

**Note:** For its reading in:
  - **Python:**the following lines of code can be used:
  ```Python
  import json
  with open(r"Folder_Name/PPG_subj_##.json", "r") as j:
    mydata = json.load(j)
  ```
  - **Matlab:**you can use the following lines of code having in the same local folder the JSON files:
  ```Matlab
  json_file = fileread('PPG_subj_##.json');
  ppg = jsondecode(json_file);
  ```
     
## Contributors
For more information about the dataset, please contact the autors at: erick.arguello00@usc.edu.co, santiago.vasquez01@usc.edu.co and luis.delgado01@usc.edu.co 
## Conflicts of interest
The autors have no conflicts of interest to declare.
## References
1. Chobanian, A. V., Bakris, G. L., Black, H. R., Cushman, W. C., Green, L. A., Izzo, J. L., Jr, Jones, D. W., Materson, B. J., Oparil, S., Wright, J. T., Jr, Roccella, E. J., Joint National Committee on Prevention, Detection, Evaluation, and Treatment of High Blood Pressure. National Heart, Lung, and Blood Institute, & National High Blood Pressure Education Program Coordinating Committee (2003). Seventh report of the Joint National Committee on Prevention, Detection, Evaluation, and Treatment of High Blood Pressure. Hypertension (Dallas, Tex. : 1979), 42(6), 1206–1252. https://doi.org/10.1161/01.HYP.0000107251.49515.c2
2. Whelton, P. K., Carey, R. M., Aronow, W. S., Casey, D. E., Jr, Collins, K. J., Dennison Himmelfarb, C., DePalma, S. M., Gidding, S., Jamerson, K. A., Jones, D. W., MacLaughlin, E. J., Muntner, P., Ovbiagele, B., Smith, S. C., Jr, Spencer, C. C., Stafford, R. S., Taler, S. J., Thomas, R. J., Williams, K. A., Sr, Williamson, J. D., … Wright, J. T., Jr (2018). 2017 ACC/AHA/AAPA/ABC/ACPM/AGS/APhA/ASH/ASPC/NMA/PCNA Guideline for the Prevention, Detection, Evaluation, and Management of High Blood Pressure in Adults: Executive Summary: A Report of the American College of Cardiology/American Heart Association Task Force on Clinical Practice Guidelines. Hypertension (Dallas, Tex.: 1979), 71(6), 1269–1324. https://doi.org/10.1161/HYP.0000000000000066
## Files
Total uncompressed size: ... MB.
### Access the files
  - [Download the ZIP file](https://github.com/sanvsquezsz/Ambulatory-PPG-recordings-Dataset/archive/refs/heads/main.zip)
