# SVCM Projectathon 2026

Jupyter notebook implementing the **SVCM Terminology Consumer** nominal test case for the ANS Projectathon 2026.

- **System under test**: `PAT_DEVICE_COLLECTEUR_ANALYSEUR_DE_DONNEES_CAD_CDM`
- **Target server**: SMT national ANS (`smt.esante.gouv.fr`)
- **Gazelle reference**: [SVCM_Cas de test nominal](https://interop.esante.gouv.fr/tm/testing/testsDefinition/viewTestPage.seam?id=12231&cid=29222)

## Usage

1. Install dependencies: `pip install requests jupyter`
2. Open the notebook: `jupyter notebook`
3. Fill in your SMT API key in the **Configuration** cell (`API_KEY = "..."`)
4. Run all cells top to bottom
