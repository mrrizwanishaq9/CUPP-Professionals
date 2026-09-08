# 🛡️ CUPP Professional V11.3

### Professional 2026 Authorized-Lab Wordlist Generation Dashboard

CUPP Professional V11.3 is a modern Python-based wordlist generation and analysis dashboard designed for **authorized security labs, cybersecurity education, local testing, and research environments**.

The project provides a professional interactive interface for creating customized wordlists from user-provided profile data, applying transformations such as capitalization, reverse variants, leetspeak, numbers, symbols, dates, and combinations.

> 🛡️ **AUTHORIZED LAB MODE**
>
> This project is intended only for systems, accounts, datasets, and security testing environments that you own or are explicitly authorized to test.

---

## ✨ Features

### 👤 Profile Builder

Create a custom profile using fields such as:

* First Name
* Last Name
* Nickname
* Birthday
* Partner
* Pet
* Company
* City
* Keyword
* Custom Words

The generator uses these inputs as local data sources for creating wordlist candidates.

---

## ⚡ Generation Engine

CUPP Professional V11.3 includes multiple generation options:

* Lowercase variants
* UPPERCASE variants
* Capitalized variants
* Reverse variants
* Leetspeak transformations
* Number combinations
* Symbol combinations
* Date and year combinations
* Two-word combinations
* Separator combinations
* Duplicate removal
* Minimum length filtering
* Maximum length filtering
* Maximum output limit

The generation engine works locally inside the Google Colab runtime.

---

## 🧠 Advanced Settings

The dashboard provides configurable advanced controls:

| Setting    | Description                          |
| ---------- | ------------------------------------ |
| Min Length | Minimum generated word length        |
| Max Length | Maximum generated word length        |
| Max Words  | Maximum number of generated entries  |
| Year From  | Starting year for date/year variants |
| Year To    | Ending year for date/year variants   |
| Numbers    | Custom numeric patterns              |
| Symbols    | Custom symbols                       |
| Separators | Custom separators                    |
| Leet Map   | Custom character substitutions       |

Example leetspeak mapping:

```text
a=@
e=3
i=1
o=0
s=$
t=7
```

---

## 🎛️ Presets

The dashboard includes ready-to-use presets:

### Custom

Full manual control over generation settings.

### Balanced Lab

A balanced configuration designed for general authorized laboratory exercises.

### Compact Lab

Produces a smaller dataset with fewer transformations.

### Extended Lab

Produces a larger local dataset with additional transformations.

---

## 📊 Analytics

After generation, the dashboard provides basic statistics including:

* Total words
* Average word length
* Shortest word
* Longest word
* Generation time
* Word-length distribution

This makes it easier to inspect and understand the generated dataset.

---

## 🔎 Live Wordlist Search

The Live Wordlist section provides an interactive search box.

For example, if the generated dataset contains:

```text
rizwan
rizwan2026
Rizwan
RIZWAN
rizwan!
rizwan123
```

searching for:

```text
rizwan
```

will filter the displayed results.

---

## 📤 Export Formats

Generated datasets can be exported in three formats.

### TXT

Simple one-word-per-line format:

```text
rizwan
Rizwan
RIZWAN
rizwan2026
```

### CSV

Structured format containing:

```text
index
word
length
```

Example:

```text
1,rizwan,6
2,Rizwan,6
3,rizwan2026,10
```

### JSON

The JSON session can contain:

* Application information
* Version
* Generation timestamp
* Profile configuration
* Generation time
* Total words
* Generated words
* Session logs

---

## 🖥️ Professional Dashboard

The interface is organized into multiple sections:

```text
┌─────────────────────────────────────────────┐
│        🛡️ CUPP PROFESSIONAL V11.3          │
│             LOCAL GENERATION ENGINE         │
├───────────────┬─────────────────────────────┤
│ Dashboard     │                             │
│ Profiler      │      MAIN WORKSPACE         │
│ Generator     │                             │
│ Analytics     │      Live Results           │
│ Export        │      Statistics             │
│ Logs          │      Console                │
└───────────────┴─────────────────────────────┘
```

### Navigation

* ▣ Dashboard
* 👤 Profiler
* ⚡ Generator
* 📊 Analytics
* ⬇ Export
* ▤ Logs

---

## 🛠️ Technology Stack

CUPP Professional V11.3 is built using:

* **Python**
* **Google Colab**
* **ipywidgets**
* **HTML**
* **CSS**
* **JSON**
* **CSV**

### Main Python Components

```text
Python
 ├── ipywidgets
 ├── itertools
 ├── collections
 ├── datetime
 ├── json
 ├── csv
 └── re
```

---

## 🚀 Getting Started

### Option 1 — Google Colab

The project is designed to run directly inside Google Colab.

1. Open Google Colab.
2. Create a new notebook.
3. Create one code cell.
4. Paste the complete V11.3 code.
5. Run the cell.
6. Open the **Profiler** section.
7. Enter authorized test/lab data.
8. Open **Generator**.
9. Select the desired generation options.
10. Click **Generate Wordlist**.

The dashboard will generate the local dataset inside the Colab runtime.

---

## 📋 Example Configuration

For a fictional laboratory dataset:

```text
First Name: Rizwan
Last Name: Demo
Nickname: Riz
Keyword: Robotics

Custom Words:
Python
AI
YOLO
Colab
VSCode
```

Then select:

```text
✓ Lowercase
✓ UPPERCASE
✓ Capitalized
✓ Reverse
✓ Leetspeak
✓ Numbers
✓ Symbols
✓ Dates / Years
✓ Combinations
✓ Deduplicate
```

Finally click:

```text
⚡ GENERATE WORDLIST
```

---

## 📁 Generated Files

The application creates local files such as:

```text
/content/
│
├── cupp_v11_3_wordlist.txt
├── cupp_v11_3_wordlist.csv
└── cupp_v11_3_session.json
```

These files remain within the current Colab runtime unless you explicitly save or download them.

---

## 🔐 Security & Responsible Use

CUPP Professional V11.3 is a **wordlist generation and analysis tool**.

It does **not** provide:

* Brute-force execution
* Credential stuffing
* Login automation
* Authentication bypass
* Account takeover
* Unauthorized password attacks

The project should only be used for:

* Authorized penetration-testing labs
* Cybersecurity education
* CTF environments where permitted
* Your own accounts and systems
* Your own datasets
* Security research with explicit authorization

Never use generated data to attempt unauthorized access to another person's account or system.

---

## 🧪 Recommended Lab Usage

A safe workflow is:

```text
Profile Data
     ↓
CUPP V11.3
     ↓
Local Wordlist
     ↓
Analytics
     ↓
Authorized Security Lab
     ↓
Results / Research
```

Keep the project inside an isolated laboratory environment when performing security experiments.

---

## 🐛 Error Handling

### Button Callback Error

Earlier versions could produce:

```text
TypeError:
generate_words() takes 0 positional arguments
but 1 was given
```

V11.3 separates the UI callback from the generation engine.

The button callback accepts the widget event:

```python
def on_generate_clicked(button=None):
    generate_wordlist()
```

This prevents the callback argument from being incorrectly passed into the generation engine.

---

## 📈 V11.3 Improvements

Compared with the earlier dashboard version, V11.3 focuses on:

* Improved professional UI
* Cleaner navigation
* Separate generation engine
* Fixed widget callback handling
* Better profile management
* Preset configurations
* Advanced generation settings
* Live search
* Analytics dashboard
* Export center
* Session logs
* Better error reporting
* Authorized Lab Mode

---

## 🔮 Future Roadmap

Possible future improvements include:

* [ ] Import words from TXT
* [ ] Import CSV datasets
* [ ] Drag-and-drop file import
* [ ] Advanced word-frequency analytics
* [ ] Interactive charts
* [ ] Custom profile templates
* [ ] Session save/load
* [ ] Theme selector
* [ ] Multi-language interface
* [ ] Improved export manager
* [ ] Plugin architecture
* [ ] Local desktop version
* [ ] VS Code integration

---

## 📸 Screenshots

Add your screenshots here:

```markdown
![Dashboard](screenshots/dashboard.png)

![Profiler](screenshots/profiler.png)

![Generator](screenshots/generator.png)

![Analytics](screenshots/analytics.png)
```

Recommended repository structure:

```text
CUPP-Professional/
│
├── README.md
├── cupp_professional_v11_3.py
├── requirements.txt
├── LICENSE
├── screenshots/
│   ├── dashboard.png
│   ├── profiler.png
│   ├── generator.png
│   └── analytics.png
└── docs/
    └── usage.md
```

---

## 📦 Requirements

For the Google Colab version:

```text
Python 3.x
ipywidgets
Google Colab
```

Install the required widget package with:

```bash
pip install ipywidgets
```

---

## 👨‍💻 Project Purpose

The purpose of CUPP Professional V11.3 is to provide a clean and educational interface for learning how profile-based wordlist generation works.

It combines a configurable generation engine with a professional dashboard so users can understand how input data, transformations, filtering, combinations, and output formats affect a generated dataset.

---

## 🌟 Why This Project?

Traditional command-line tools can be difficult for beginners to understand.

CUPP Professional provides a visual workflow:

```text
INPUT
  ↓
PROFILE BUILDER
  ↓
GENERATION SETTINGS
  ↓
WORDLIST ENGINE
  ↓
FILTERING
  ↓
ANALYTICS
  ↓
EXPORT
```

This makes the project useful for students, cybersecurity learners, Python developers, and authorized security researchers.

---

## 🤝 Contributing

Contributions are welcome.

Before submitting a contribution:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Test the application.
5. Update documentation if necessary.
6. Submit a pull request.

For example:

```bash
git clone YOUR_REPOSITORY
cd CUPP-Professional

git checkout -b feature/new-ui

git add .
git commit -m "Improve professional dashboard"

git push origin feature/new-ui
```

---

## 📄 License

Choose an appropriate open-source license for your repository.

For example:

```text
MIT License
```

If you use the MIT License, add a `LICENSE` file containing the official license text rather than placing the full license inside this README.

---

## ⚠️ Disclaimer

This project is provided for educational, research, and authorized security-testing purposes.

The developer is not responsible for misuse of this software. Users are responsible for obtaining appropriate permission before testing systems, accounts, networks, or datasets.

**Use responsibly. Stay authorized.**

---

## ⭐ Support the Project

If you find this project useful:

* ⭐ Star the repository
* 🐛 Report bugs
* 💡 Suggest features
* 🤝 Contribute improvements
* 📚 Improve the documentation

---

## 🛡️ CUPP Professional V11.3

```text
LOCAL GENERATION ENGINE
PROFESSIONAL 2026 UI
AUTHORIZED LAB MODE

Python • Google Colab • ipywidgets
```

**Built for learning. Built for research. Built for authorized labs.**
