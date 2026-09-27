# DesiData

DesiData publishes India-focused datasets and tools for exploring and working with them. This repository contains dataset notebooks and examples for using DesiData data in Google Colab and Python.

- **Website:** [desidata.in](https://www.desidata.in/)
- **Browse datasets:** [DesiData datasets](https://www.desidata.in/datasets)
- **Weekly model benchmark:** [DesiData Bench](https://www.desidata.in/bench)
- **Community announcements and discussion:** [DesiData Community](https://www.desidata.in/community)
- **Python package:** [desidata on PyPI](https://pypi.org/project/desidata/)

## Use a dataset notebook

Open a notebook under [`notebooks/`](./notebooks/) and run it in Colab or your own Python environment. The notebook collection is refreshed as datasets are added.

Some notebook download examples may need updating to use the current authenticated download flow. See [Download data with a DD token](#download-data-with-a-dd-token) before running a download cell.

## Download data with a DD token

DesiData datasets are free. To associate programmatic downloads with your DesiData account, create a free DD token from your [DesiData profile](https://www.desidata.in/profile).

1. Sign in to DesiData and create a token in your profile.
2. Copy and save it when it is shown. Treat it like a password; do not paste it into a notebook that you share or commit it to GitHub.
3. Set it as the `DD_TOKEN` environment variable in your local environment, or add it to Colab's **Secrets** as `DD_TOKEN`.
4. Use the token in the DesiData Python package or authenticated download examples.

For example, in a local terminal:

```bash
# macOS or Linux
export DD_TOKEN="your-token"
```

```powershell
# Windows PowerShell
$env:DD_TOKEN = "your-token"
```

In Google Colab, add `DD_TOKEN` under the notebook's **Secrets** panel and grant the notebook access to it. Do not put the token directly in a notebook cell.

A token is free. Authenticated download requests are associated with your account so DesiData can show download activity and counts. The count records a download request; it does not prove that a file finished downloading or was used.

## Weekly benchmark

The DesiData benchmark page compares selected open models on the current benchmark set. The plan is to run and publish a refreshed model comparison each Saturday afternoon, using the latest DesiData benchmark data. Check [DesiData Bench](https://www.desidata.in/bench) for the current results and methodology.

## Updates

This repository is a public place to follow notebook and data-access changes. New dated entries will be added here as the project changes.

### 2026-09-27 — DD token downloads

Programmatic dataset downloads now use a free DD token linked to a DesiData account. This lets download activity be attributed to the account while keeping the datasets free. Create a token from your [profile](https://www.desidata.in/profile); never commit it to a notebook or repository.

### Planned — Weekly model benchmark

The plan is to publish updated open-model benchmark results on Saturday afternoons. Results and details will be posted on the [benchmark page](https://www.desidata.in/bench).

## Contributing and feedback

Have a dataset request, notebook correction, or benchmark suggestion? Open a GitHub issue or join the conversation on the [DesiData Community page](https://www.desidata.in/community).
