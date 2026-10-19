# Global COVID-19 Data Explorer — Week 4

Seven-stage analysis based on the supplied project brief, with Nigeria as a local case.

## Run
1. Extract this complete folder. Use Python 3.11 or newer and a virtual environment.
2. Run `python -m pip install -r requirements.txt`.
3. Open `notebooks/Global_COVID19_Data_Explorer.ipynb` in Jupyter, VS Code or Colab. For Colab, upload the project folder or allow the notebook to download the raw CSV.
4. Select Restart Kernel and Run All. A notebook-only download will fetch the raw file into `data/raw`; the full ZIP includes the exact snapshot used.
5. Review `outputs/findings_summary.md`, `outputs/one_page_summary.png` and interactive HTML maps. Map boundaries require internet access.

Source: https://catalog.ourworldindata.org/garden/covid/latest/compact/compact.csv
Download date: 2026-10-18 UTC. See data/raw/source_metadata.json and outputs/run_manifest.json for provenance and SHA-256. This latest endpoint can change: retain the bundled snapshot to reproduce the included results. Raw CSV is approximately 174 MB uncompressed.

## Structure
- data/raw: unchanged raw data and download record
- data/clean: derived country summaries and clusters
- notebooks: executed seven-stage notebook
- outputs: charts, HTML maps, metrics, missingness, cleaning log, findings and environment manifest
- data_dictionary.csv: column meanings, types, readiness
- peer_test.md: independent test checklist (pending)

## Git workflow
Initialize with `git init`. Commit real work as it occurs using messages such as: Stage 1: validate compact schema and audit missingness; Stage 2: compare categories and case waves; Stage 3: describe mortality and associations; Stage 4: map counts and rates; Stage 5: evaluate regression and clustering; Stage 6: document environment and peer run; Stage 7: redesign charts and summarize findings. Do not fabricate past commits. Consider Git LFS or external data storage for the raw CSV, which exceeds GitHub's normal 100 MB file limit; exclude it from ordinary Git commits while preserving the local snapshot and source hash.

## Interpretation
Latest nonmissing values have different observation dates. Models are exploratory, not causal or prospective. Reporting differences and ecological confounding limit policy comparisons. No teammate test has been claimed; complete the peer checklist independently before submission.

## Build validation
All code cells were executed sequentially from a clean in-process IPython session, with chart and table outputs embedded. This build environment blocks Jupyter kernel sockets, so an external Jupyter Restart/Run All remains part of the independent teammate checklist rather than a claimed completed test.
