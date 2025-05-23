# Academia–Practice Interaction Mapping Using NLP

This project uses Named Entity Recognition (NER) to extract non-academic organizations from social impact case studies submitted by Polish universities to the POL-on system. The goal is to identify practice partners and analyze the network of academic–nonacademic interactions in the context of societal impact.

---

##  What this project does

- Loads and cleans text from Polish-language impact case study reports
- Applies two NER models:
  - [`Stanza`](https://github.com/stanfordnlp/stanza) (Stanford NLP)
  - [`Davlan/xlm-roberta-base-finetuned-ner`](https://huggingface.co/Davlan/xlm-roberta-base-ner-hrl) via Hugging Face
- Extracts and compares named entities of type `ORG`
- Filters out academic institutions using keyword matching
- Outputs lists of potential non-academic partners for further analysis (in progress)

## Project Structure
```
academia-practice-nlp/
├── data/ # Input data (not tracked by Git)
├── output/ # Processed outputs, including NER and filtering results
├── notebooks/ # Modular notebooks (01–05) for each stage of the pipeline
│ ├── 01_data_preparation.ipynb
│ ├── 02_ner_extraction.ipynb
│ ├── 03_entity_analysis.ipynb
│ ├── 04_entity_preprocessing.ipynb
│ └── 05_entity_classification.ipynb
├── archive/ # Full legacy notebook (not pushed to GitHub)
├── scripts/ # Reusable Python scripts (planned or used)
├── requirements.txt # Python dependencies
├── .gitignore # Files and folders excluded from version control
└── README.md # Project overview and usage instructions
```

## Modular NLP Pipeline

This project is divided into five Jupyter notebooks, each handling a specific stage of the workflow:

| Notebook | Purpose |
|----------|---------|
| `01_data_preparation.ipynb` | Clean and structure raw Polish-language case study text |
| `02_ner_extraction.ipynb`   | Extract named entities (`ORG`) using two NER models |
| `03_entity_analysis.ipynb`  | Compare and evaluate entity extraction performance |
| `04_entity_preprocessing.ipynb` | Normalize and clean entity names |
| `05_entity_classification.ipynb` | Sample and label organization types for typology |


## How to Run This Project


1. Clone the repository and install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Add your input dataset (CSV format) to the `data/` folder.

3. Run each notebook in order:
   - `01_data_preparation.ipynb`
   - `02_ner_extraction.ipynb`
   - `03_entity_analysis.ipynb`
   - `04_entity_preprocessing.ipynb`
   - `05_entity_classification.ipynb`

4. Outputs are saved to the `output/` folder and can be used for further analysis or visualization.



---

## Author

**Kamila Lewandowska**  


---

## 📄 License

MIT License — free to use, adapt, and build upon.

