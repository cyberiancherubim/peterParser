# 🕸️ Peter Parser

## ⚙️ Installation & Quickstart

**Prerequisite**: [Anaconda or Miniconda](https://www.anaconda.com/products/distribution)

Clone the repository and run the setup script:

```powershell
git clone https://github.com/cyberiancherubim/peterParser.git
cd peterParser
.\setup.ps1
```

The script will:
- Detect or prompt for Conda installation
- Add Conda to your PATH if necessary
- Create and activate the Conda environment automatically
- Install all required packages from `environment.yml`

You're ready to start scraping!

---

## 📁 Repository Structure
```
├── scripts/
│   ├── html_cleaner.py       # Cleans extracted HTML to plain text
│   ├── importer.py           # Imports URLs from text/clipboard into config
│   └── peterParser.py        # Core scraper logic ("Peter" does the crawling)
├── books.json                # Bible-specific scraping config
├── environment.yml           # Conda environment definition
├── setup.ps1                 # Powershell bootstrap installer
├── .gitignore                # Standard ignores
└── README.md                 # This file
```

---

## 🧠 Usage Examples
### Scraping Bible Pages with Config:
```powershell
conda activate peterParser
python scripts/peterParser.py --config books.json
```

### Cleaning HTML Output to TXT:
```powershell
python scripts/html_cleaner.py --input ./output/genesis.html --output ./output/genesis.txt
```

### Importing URL List to JSON:
```powershell
python scripts/importer.py --input urls.txt --output books.json
```

---

## 🤖 What Makes This Special?
- **Modular Design**: Each part of the scraper is reusable in other projects.
- **PowerShell Setup**: Streamlined for Windows power users.
- **Anaconda Support**: Optimized for ML/NLP pipelines.
- **Flexible Config**: Load your own `.json` scrape instructions, not hardcoded!

---

## 📄 License
MIT. Go forth and scrape responsibly.

