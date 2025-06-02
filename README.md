# Cartoon Network? 

### Reconstructing Marcel Antoine's Cultural Context through Named Entity Recognition and Network Analysis

This repository contains all materials related to the Master's thesis project on the Belgian cartoonist **Marcel Antoine** (active in the 1930s), exploring how digital methods, specifically **Named Entity Recognition (NER)** and **network visualisation**, can be used to reconstruct fragmented historical cultural contexts from digitised newspaper data.

---

## Repository Structure

### Manual Annotation Datasets

These JSON files contain manually annotated newspaper articles used to train and evaluate NER models.

- `Labeled_Marcel50.json` – First batch of 50 annotated articles.
- `Marcel100.json` – Expanded dataset with 100 articles.
- `Marcel150_clean.json` – Final version with 150 cleaned and consistently annotated articles.

---

### NER Notebooks

#### Executing NER

Notebooks that run NER on the newspaper articles using different models:

- `NER_camembert(training).ipynb` – Fine-tuning CamemBERT.
- `NER_camembert.ipynb` – Applying pretrained CamemBERT.
- `NER_flair.ipynb` – Applying Flair NER.
- `NER_spacy.ipynb` – Applying spaCy NER.
- `llama_NER_code.ipynb` – Running prompt-based NER using LLaMA.
- `verbeterde_articles.ipynb` – Extracting random articles for manual annotation.

#### Evaluating NER

Notebooks for evaluating NER model performance (precision, recall, F1) against manually annotated data.

- `Evaluating_NER_csvfiles.ipynb` – Evaluation of the CSV outputs against the annotated JSON dataset.
- `Evaluating_NER_trainedJSON.ipynb` – Evaluation of the fine-tuned CamemBERT models against the annotated JSON dataset.
- `evaluating_NER_flatNERjsonfile.ipynb` – Evaluation of flat JSON results (e.g., from LLaMA) against the annotated JSON dataset.

---

### NER Results

NER model outputs and evaluation scores.

- `flair_ner_results.csv`
- `spacy_ner_results.csv`
- `flat-llama-results.csv` / `flat_llama_results.json`
- `ner_results_camembert.json`
- `ner_results_trained_5.csv`, `ner_results_trained7.csv`, `ner_results_trained10.csv`

---

### Network Files

Files used to build and visualise the co-occurrence network of people across the articles.

- `Marcel_final.gexf` – Final network graph file (used in Gephi/Retina).
- `edges_marcel_Categories.csv` – Edge list with article-based category labels.
- `NetworkCode_Marcel.ipynb` – Code for building the edge list to build the network.
- `Marcel_final.gephi` – file to view network with Gephi.

**Interactive Network Visualisation**  
The network can also be explored interactively online at the following link:  
  [View the network in Retina]([https://your-link-here.com](https://ouestware.gitlab.io/retina/1.0.0-beta.1/#/graph/?url=https%3A%2F%2Fraw.githubusercontent.com%2FBauke-V%2FCartoonNetwork-MarcelAntoine%2Frefs%2Fheads%2Fmain%2FMarcel_final.gexf&sa[]=ha&sa[]=b&sa[]=a&sa[]=hu&sa[]=p&sa[]=cu&sa[]=t&sa[]=ei&ca[]=d-s&ca[]=w-s&ca[]=ec-s&ca[]=co-s&ca[]=m-s&ca[]=s-s&ec=o))

---

### Original Article Data

Raw and cleaned article data used throughout the project.

- `Alto-xml/` – ALTO-XML files (OCR structured output).
- `Text-2_blocks/` – Block-level extracted text.
- `articles/` – Raw text articles.
- `cleaned articles/` – Manually cleaned article texts.
- `jpeg_stock-download_20250210/` – Associated scanned page images.
- `Marcel Antoine in Newspapers(Categories test)_latest.csv` – Article metadata and categorisation.

---

### Final Datasets

- `final_dataset.csv` – Combined cleaned data with extracted NER.
- `final_dataset_without_metadata.csv` – Version without added metadata.

---

## How to Use

1. Clone the repository.
2. Use the Jupyter notebooks in the **NER Notebooks** section to run or evaluate NER on historical articles.
3. Use `NetworkCode_Marcel.ipynb` to generate a the edge list used to build the network.
4. Open `Marcel_final.gexf` in Gephi or visualise it in Retina for interactive exploration.

---

## About the Thesis

This repository supports the Master’s thesis *"Reconstructing Marcel Antoine’s Cultural Context with NER and Network Analysis"*, submitted in 2025. The project explores how modern NLP and data visualisation tools can support historical inquiry into lesser-known figures using digitised, unstructured sources.



