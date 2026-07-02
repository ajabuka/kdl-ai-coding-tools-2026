# Text Analysis Toolkit

Analyse the frequency of words in early modern English texts (e.g. Shakespeare's *Hamlet*) using stop word filtering, n-gram modelling, lemmatisation, and interactive visualisation.

## Project Overview

The project consists of the following components:

| Component | Description |
|---|---|
| `text_analysis_notebook.ipynb` | Jupyter notebook implementing the full text analysis pipeline |
| `data/` | Contains input text files (`Hamlet.txt`), custom stop word list (`earlyModernStopword.txt`), and test data (`test_data.txt`) |
| `requirements.txt` | Python package dependencies |

## How It Works

The notebook performs these steps:

1. **Load dependencies** — imports required Python packages (nltk, gensim, spaCy, plotly, pandas)
2. **Download language resources** — downloads nltk stop words and the spaCy English language model
3. **Configure paths** — sets up input (`data/`) and output (`results/`) directories
4. **Build stop word list** — combines nltk stop words, custom early modern English stop words, and additional domain-specific terms
5. **Build n-gram models** — detects common bigrams and trigrams in the text
6. **Lemmatise tokens** — reduces words to their base forms using spaCy
7. **Compute frequencies** — counts occurrences of each unique word
8. **Visualise** — generates an interactive histogram of the top N words

A tutorial notebook (`example.ipynb`) is also provided with usage examples and configuration guidance. Open it alongside the main analysis notebook:

```bash
jupyter notebook example.ipynb
```

## Getting Started

### Prerequisites

- Python 3.10 or later
- pip (Python package installer)

### Installation

1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd kdl-ai-coding-tools
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebook:
   ```bash
   jupyter notebook text_analysis_notebook.ipynb
   ```

4. Run all cells in the notebook. The first run will download nltk stop words and the spaCy English model automatically. An interactive histogram will be generated and saved to the `results/` directory.

### Testing with Test Data

A file `data/test_data.txt` is provided to verify that the pipeline runs correctly:

1. In the notebook, change the `documentName` variable (near the top of the main cell) to `'test_data.txt'`
2. Re-run all cells
3. The output histogram will show word frequencies for the test passage
4. To reset, change `documentName` back to `'Hamlet.txt'`

## Output

The analysis produces an interactive HTML histogram showing the top N most frequent words, saved to the `results/` directory. The chart displays word counts and percentage contributions, and can be opened in any web browser.

## FAIR Software Checklist

[![FAIR checklist badge](badge.svg)](?f=11&a=10111&i=00100&r=011)

*Self-assessment conducted using the [FAIR Software Checklist](https://fairsoftwarechecklist.net/v0.2/).*

### Findable

| Question | Answer | Score |
|---|---|---|
| 1. Is information from the metadata consumed by search engines to help rank their results? | Published on GitHub (minimal SEO) | Partial |
| 2. Are the software's identifiers globally unique? | The GitHub URL provides a unique identifier | Yes |
| **Findable score** | | **Moderate** |

### Accessible

| Question | Answer | Score |
|---|---|---|
| 3. Can someone use the software's identifiers to get a copy? | Public GitHub repository | Yes |
| 4. A few years from now, will the identifiers resolve to exactly the same content? | URL only — no persistent identifier (DOI) | No |
| 5. Is the software retrievable using a protocol that is open, free, and universally implementable? | HTTPS | Yes |
| 6. Does the protocol allow for authentication and authorization? | Openly available | Yes |
| 7. Does the metadata include an identifier to reference the associated software? | README does not explicitly include a repository URL | No |
| **Accessible score** | | **Moderate** |

### Interoperable

| Question | Answer | Score |
|---|---|---|
| 8. What type of data formats are being used? | Plain text and HTML (open formats) | Partial |
| 9. What approach does the software take to versioning? | No versioning or releases | No |
| 10. How are the software's dependencies specified? | Listed by name in `requirements.txt` | Partial |
| 11. How is the software's relationship to related software described? | Not described | No |
| 12. How is the software's relationship to related data described? | Not described | No |
| **Interoperable score** | | **Low** |

### Reusable

| Question | Answer | Score |
|---|---|---|
| 13. Is the software executable? | Runnable with `pip install -r requirements.txt` | Yes |
| 14. Is the software available in a form that allows modification or extension? | Source files available with documentation | Partial |
| 15. Which of the following best describes the software's usage rights? | No license file included | No |
| **Reusable score** | | **Low** |

## Contributing

Contributions are welcome! If you would like to improve this project, please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Make your changes
4. Run the analysis with the test data to verify nothing is broken
5. Commit your changes (`git commit -m 'Add your feature'`)
6. Push to the branch (`git push origin feature/your-feature`)
7. Open a Pull Request

Please ensure your code follows the existing style conventions and includes appropriate comments and docstrings.

## License

This project is distributed under the terms of the [LICENSE](LICENSE.txt) file.

## Citation

If you use this software in your research, please cite it appropriately. See `CITATION.cff` for citation metadata.
