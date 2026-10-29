# Cheminformatics Virtual Laboratory

A Streamlit educational application for molecular structure visualization and cheminformatics analysis using RDKit. It includes SMILES parsing, 2D/3D visualization, molecular descriptors, structure–property learning, assessments, and downloadable PDF reports.

## Run locally

Python 3.11 is recommended.

```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

python -m pip install --upgrade pip
pip install -r requirements.txt
streamlit run app.py
```

Then open the local URL printed by Streamlit (normally http://localhost:8501).

## Deploy with Docker

```bash
docker build -t cheminformatics-virtual-lab .
docker run --rm -p 8501:8501 cheminformatics-virtual-lab
```

Open http://localhost:8501.

## Deploy to Streamlit Community Cloud

1. Extract this project and push the contents of this folder to a GitHub repository.
2. In Streamlit Community Cloud, create an app from that repository.
3. Set the main file path to `app.py` and deploy. The platform installs dependencies from `requirements.txt`.

## Important notes

- Internet access is required for browser-based 3D rendering to load the py3Dmol viewer assets in some environments.
- This is an educational tool, not a validated source for clinical or regulatory decisions.
- The student profile fields are session inputs; this project does not implement a database or persistent student account system.
- For production use with real student data, add authentication, authorization, privacy controls, and persistent storage before deployment.
