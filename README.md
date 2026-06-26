# The-data-and-AI-challenge

-- # IR-Candidate-Ranker

An automated candidate ranking and scoring engine optimized for **Information Retrieval (IR) and Machine Learning** engineering roles. This system processes large-scale candidate datasets to identify top-tier talent using a multi-stage evaluation pipeline.

## 🚀 Key Features

- **Honeypot Detection:** Automatically filters out profiles with unrealistic skill proficiencies (e.g., 'Expert' status with 0 months experience).
- **Technical Verification Engine:** Calculates 'Technical Years of Experience' (Tech YoE) by analyzing career history descriptions rather than just relying on total tenure.
- **Strategic Weighting:**
  - **Company Size Multipliers:** Favors candidates from high-growth scale-ups (50-1,000 employees) over large corporate consulting firms.
  - **Geographic Bonuses:** Applies multipliers for candidates located in primary tech hubs (e.g., Noida, Pune, Delhi).
- **Non-Templated Reasoning:** Uses a linguistic compiler to generate unique justifications for every candidate to ensure human-like evaluation notes.
- **Normalized Scoring:** Outputs a relative score (0.0 to 1.0) to facilitate easy comparison across candidate pools.

## 🛠️ Tech Stack

- **Python 3.10+**
- **Pandas** (for data validation)
- **JSONL** (streaming data processing)

## 📋 Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/IR-Candidate-Ranker.git
   cd IR-Candidate-Ranker
   ```

2. **Prepare your data:**
   Place your `candidates.jsonl` file in the root directory.

3. **Run the ranker:**
   ```bash
   python code.py
   ```

4. **Output:**
   The script will generate a `sample_submission.csv` containing the Top 100 ranked candidates.

## 🧠 How the Scoring Works

| Factor | Impact | Description |
| :--- | :--- | :--- |
| **Core Keywords** | +25 pts | Matches for `milvus`, `vector`, `ranking`, `elasticsearch`, etc. |
| **Tenure Sweet-spot** | +40 pts | Targets candidates with 5-9 years of total experience. |
| **Notice Period** | Multiplier | Incentivizes candidates with <30 days notice (1.25x). |
| **Recency** | Multiplier | Decays score based on candidate inactivity over 12 months. |

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
