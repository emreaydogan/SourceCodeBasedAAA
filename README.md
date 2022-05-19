# SourceCodeBasedAAA


1. Download "lite_dataset_10.csv" from "https://github.com/buptkick/AppAuth/tree/master/Data" and put the file to Data folder.

2. Create "feature", "result" and "smali" folder in the working directory.


Feature Extraction
-- Use Python 2.7

class FeatureType(enum.Enum):
    Apktool = 0
    CustomSmali = 1
    AllSmali = 2
    Permission = 3
    Library = 4
    Metadata = 5
    Java = 6
    
-- python feature_extraction.py 1 3 4           # extract customsmali_perm_lib features



CrossValidation
-- Use Python 3.6
-- change "feature_type" variable               # feature_type = 'customsmali_perm_lib'
-- python accuracy_results.py
