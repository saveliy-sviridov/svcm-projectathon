# SVCM Projectathon 2026

Jupyter notebooks for the **SVCM Terminology Consumer** test cases — ANS Projectathon 2026.

- **System under test**: `PAT_DEVICE_COLLECTEUR_ANALYSEUR_DE_DONNEES_CAD_CDM`
- **Target server**: SMT national ANS (`smt.esante.gouv.fr`)

## Usage

1. `pip install requests jupyter nbstripout`
2. `nbstripout --install` (strips outputs before commits)
3. `export SMT_API_KEY="your-key"` then `jupyter notebook`
4. Run each notebook top to bottom

## Notebooks

| File | Gazelle test |
|------|-------------|
| `01_nominal.ipynb` | SVCM_Cas de test nominal |
| `02_iti95_valueset.ipynb` | SVCM_ITI-95_Recuperation ValueSet |
| `03_iti96_codesystem.ipynb` | SVCM_ITI-96_Recuperation CodeSystem |
| `04_iti97_expand.ipynb` | SVCM_ITI-97_Recuperation Liste de code du JDV |
| `05_iti98_lookup.ipynb` | SVCM_ITI-98_Recuperation détails CodeSystem |
| `06_iti99_validate.ipynb` | SVCM_ITI-99_Validation Code |

Each run saves artifacts to `runs/{notebook}_{timestamp}/`, prefixed by step number.
