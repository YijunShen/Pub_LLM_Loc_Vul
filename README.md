## "Leveraging Public Vulnerability Semantic Information: A Large Model-Based Approach for Vulnerability Localization":

## Instruction of the our research pipeline:

#### 1. Download CVE records (2020-2024) from NVD website first.(https://nvd.nist.gov/vuln/data-feeds), storing to "./data/nvd_data/"

#### 2. Use 1_download_and_filter_source_file.ipynb to obtaining source code of each projects

#### 3. Use 2_construct_pre_dataset.ipynb to establish a preliminary fine-grained dataset "{language}_vul.jsonl"

#### 4. manually analyse vulnerable code blocks in "{language}_vul.jsonl" to get correct vulnerability dateset, which has been stored as "./data/{language}/{language}_vul_2.jsonl"

#### 5. manually analyse description text in "{language}_vul_2.jsonl" to extract vulnerability concepts, which have been stored as "./data/{language}/{language}_des_extract_fix/"

#### 6. Use 3_RQ1_and_RQ2_query.ipynb to localize vulnerable code blocks (based on algorithm in RQ1 and RQ2 described in the paper).

#### 7. Use 4_RQ3_query.ipynb to localize vulnerable code blocks (based on algorithm in RQ3 described in the paper).


## Instruction of the study data:
#### 1. Raw Data
The original dataset are shown in "./data/REEF_data/". The NVD and CWE data are stored under "./data/nvd_data/"

#### 2. Vulnerability Dataset:
Our fine-grained vulnerability dataset are listed in "./data/{language}/{language}_vul_2.jsonl".

#### 3. Isolated conceps extracted from descriptions:
The five dimention concepts are list in "./data/{language}/{language}_des_extract_fix/"
