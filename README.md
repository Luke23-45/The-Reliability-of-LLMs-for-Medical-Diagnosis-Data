
# Data Repository for "The Reliability of LLMs for Medical Diagnosis: An Examination of Consistency, Manipulation, and Contextual Awareness"

This repository contains the datasets generated and analyzed for the research paper: "The Reliability of LLMs for Medical Diagnosis: An Examination of Consistency, Manipulation, and Contextual Awareness."  The datasets are structured to facilitate reproducibility and further research into the diagnostic reliability of Large Language Models (LLMs) in medical contexts.

## Repository Contents

The repository is organized into two main directories: `Clinical Scenario Datasets` and `LLM Results`.
```

├── Clinical Scenario Datasets

│ ├── Data

│ │ ├── 52_baseline_clinical_scenario.json

│ │ ├── dataset_for_consistency.json

│ │ ├── dataset_for_contextual_awareness.json

│ │ └── dataset_for_manipulation.json

│ └── raw

│ │ └── disease.json

├── LLM Results

│ ├── CSV

│ │ ├── Consistency

│ │ │ └── combined_consistency.csv

│ │ ├── Contextual

│ │ │ ├── qualitative_contextual_results.csv

│ │ │ └── quantitative_contextual_results.csv

│ │ └── Manipulation

│ │ │ └── clinically_validated_diagnoses.csv

│ └── JSON

│ │ ├── Consistency

│ │ │ ├── Gemini_consistency_result.json

│ │ │ ├── OpenAI_consistency_result.json

│ │ │ └── raw

│ │ │ ├── Gemini_consis.json

│ │ │ └── OpenAI_consis.json

│ │ ├── Context

│ │ │ ├── gemini_contextual_result.json

│ │ │ └── openai_contextual_result.json

│ │ └── Manipulation

│ │ │ ├── gemini_manipulation_result.json

│ │ │ └── openai_manipulation_result.json

└── README.md

```



### 1. Clinical Scenario Datasets

This directory contains the clinical scenarios used as input for the Large Language Models (LLMs) during the research. It is further divided into two subdirectories: `Data` and `raw`.

*   **`Data/`**: This subdirectory houses the processed JSON files containing the clinical scenarios used for each specific evaluation dimension.

    *   **`52_baseline_clinical_scenario.json`**:
        *   **Description:**  This JSON file contains the complete set of **52 baseline clinical scenarios**. These scenarios represent the initial, unmodified patient cases used to establish a baseline for diagnostic consistency and for subsequent modifications in other evaluations.
        *   **Format:** JSON array. Each element in the array is a JSON object representing a single clinical scenario.  Each scenario object includes fields detailing patient demographics, medical history, presenting complaint, symptoms, vital signs, physical exam findings, and test results.  *(Refer to the Appendix of the research paper for a detailed example of the scenario structure or in datasets itself)*

    *   **`dataset_for_consistency.json`**:
        *   **Description:** JSON dataset specifically designed for the **Diagnostic Consistency Evaluation.  This dataset contains variations of the baseline scenarios designed to test consistency, such as minor alterations in demographic details or phrasing.
        *   **Format:** JSON array. Similar structure to `52_baseline_clinical_scenario.json`, with added variations for consistency testing.

    *   **`dataset_for_contextual_awareness.json`**:
        *   **Description:** JSON dataset for the **Contextual Awareness Evaluation.  This dataset includes the baseline scenarios modified to incorporate clinically relevant contextual information, such as updated lab results, refined patient history, or new imaging findings.
        *   **Format:** JSON array. Scenarios are based on `52_baseline_clinical_scenario.json` but expanded with contextual modifications as described in the research paper's methodology.

    *   **`dataset_for_manipulation.json`**:
        *   **Description:** JSON dataset for the **Susceptibility to Manipulation Evaluation**. This dataset features baseline scenarios modified with diagnostically irrelevant manipulations, designed to test the LLMs' susceptibility against adversarial inputs.
        *   **Format:** JSON array. Scenarios are derived from `52_baseline_clinical_scenario.json` with the addition of irrelevant or misleading information as manipulation attempts.

*   **`raw/`**: This subdirectory contains auxiliary data files.

    *   **`disease.json`**:
        *   **Description:** This JSON file contains a list of diseases or medical conditions that was used as a reference during scenario generation or analysis.
        *   **Format:** JSON format. The specific structure is detailed within the file itself.

### 2. LLM Results

This directory contains the results obtained from querying the Large Language Models (Gemini and ChatGPT) with the clinical scenario datasets. Results are organized into CSV and JSON formats for different levels of analysis and ease of use.

*   **`CSV/`**

    *   **`Consistency/`**: Results from the Diagnostic Consistency.
        *   **`combined_consistency.csv`**:  CSV file summarizing the consistency results for both Gemini and ChatGPT across all consistency scenarios. 

    *   **`Contextual/`**: Results from the Contextual Awareness Evaluation.
        *   **`qualitative_contextual_results.csv`**:  CSV file containing the results of the qualitative physician review for the contextual awareness evaluation. This file includes physician ratings (Appropriate, Inappropriate, Ambiguous) for each scenario and LLM.
        *   **`quantitative_contextual_results.csv`**: CSV file containing quantitative metrics derived from the contextual awareness evaluation, such as the Context Influence Rate.

    *   **`Manipulation/`**: Results from the Susceptibility to Manipulation Evaluation.
        *   **`clinically_validated_diagnoses.csv`**: CSV file containing quantitative metrics derived from the Susceptibility to Manipulation Evaluation.
	
-    **JSON/**
	  - **`Consistency/`**
	    - **`Gemini_consistency_result.json`** and **`OpenAI_consistency_result.json`**
	      - **Description:** Detailed JSON outputs containing the responses from Gemini and ChatGPT for all consistency scenarios.
	    - **Subdirectory `raw/`:**
	      - **`Gemini_consis.json`** and **`OpenAI_consis.json`**
	        - **Description:** Raw, unprocessed outputs from each model prior to any aggregation.
	  - **`Context/`**
	    - **`gemini_contextual_result.json`** and **`openai_contextual_result.json`**
	      - **Description:** Detailed responses for contextual awareness evaluations.
	  - **`Manipulation/`**
	    - **`gemini_manipulation_result.json`** 
	    - **`openai_manipulation_result.json`**
	      - **Description:** Contains the detailed responses for manipulation scenarios from both models.

## Data Usage Notes

*   **Ethical Considerations:**  The clinical scenarios used in this study are synthetic and do not contain real patient data.  Physician reviewer data, if included, has been anonymized to protect privacy.
*   **Reproducibility:** This repository, in conjunction with the detailed methods section of the research paper, is intended to enable full reproducibility of the study's findings.

## License
MIT License, Creative Commons Attribution 4.0 International (CC BY 4.0)

## Citation


## Contact

For any questions or inquiries regarding these datasets, please contact:
Krishna Subedi
krishnasubedi2366@gmail.com
