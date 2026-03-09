# SVCM Projectathon 2026

Jupyter notebooks implementing all **SVCM Terminology Consumer** test cases for the ANS Projectathon 2026.

- **System under test**: `PAT_DEVICE_COLLECTEUR_ANALYSEUR_DE_DONNEES_CAD_CDM`
- **Target server**: SMT national ANS (`smt.esante.gouv.fr`)

## Usage

1. Install dependencies: `pip install requests jupyter`
2. Open: `jupyter notebook`
3. Fill in your SMT API key in the **Configuration** cell of each notebook (`API_KEY = "..."`)
4. Run all cells top to bottom

> The API key is only needed for notebooks that call `/api/` or `/wp-json/` endpoints (01, 04 onward). Pure FHIR endpoints (`/fhir/`) are public.

## Notebooks

| File | Gazelle test | Transactions | Description |
|------|-------------|--------------|-------------|
| `01_nominal.ipynb` | SVCM_Cas de test nominal | ITI-95 | CapabilityStatements, TRE-R256 + history diff, SNOMED download |
| `02_iti95_valueset.ipynb` | SVCM_ITI-95_Recuperation ValueSet | ITI-95 | GET ValueSet `JDV-J245-Civilite-CISIS` by canonical URL |
| `03_iti96_codesystem.ipynb` | SVCM_ITI-96_Recuperation CodeSystem | ITI-96 | GET CodeSystem `TRE-R02-SecteurActivite` by canonical URL |
| `04_iti97_expand.ipynb` | SVCM_ITI-97_Recuperation Liste de code du JDV | ITI-97 | `$expand` (GET) + `$lookup`/`$validate-code`/`$subsumes` (POST) on CIM-11 |
| `05_iti98_lookup.ipynb` | SVCM_ITI-98_Recuperation détails CodeSystem | ITI-98 | `$lookup` CIM-11 code `DA63`, children, SNOMED `425803006` (POST) |
| `06_iti99_validate.ipynb` | SVCM_ITI-99_Validation Code | ITI-99 | `$validate-code` GET + POST (valid) + negative test `SA100` (invalid) |

## Output files (01_nominal only)

Generated at runtime, not committed to VCS:

- `smt-cs.json` — CapabilityStatement général
- `smt-tc.json` — CapabilityStatement terminologique
- `smt-tre256.json` — CodeSystem TRE-R256-TypeMessagerie
- `snomed-ct.zip` — SNOMED CT International
- `snomed-ct-fr.zip` — SNOMED CT France
