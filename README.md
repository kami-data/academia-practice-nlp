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
- Outputs lists of potential non-academic partners for further analysis

## Project Structure
```
academia-practice-nlp/
├── data/                       # Input data (not tracked by Git)
├── output/                     # Results from NER models
├── notebooks/                  # Jupyter notebooks
├── scripts/                    # Reusable Python scripts
├── requirements.txt            # Python dependencies
├── .gitignore                  # Ignore large files and checkpoints
└── README.md                   # Project description
```

## How to Run

1. Clone this repo  
2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Place your dataset in the `/data` folder  
4. Open the main notebook:

    ```
    notebooks/ics_NER_extraction_PL.ipynb
    ```

5. Run all cells and review outputs in the `/output` folder.


---

## Author

**Kamila Lewandowska**  


---

## 📄 License

MIT License — free to use, adapt, and build upon.

