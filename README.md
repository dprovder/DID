# DID Framework

### 🚀 Just Another Ducking ELT Framework 🦆
![Just Another Ducking ELT Framework](https://raw.githubusercontent.com/dprovder/DID/refs/heads/main/DALL·E%202025-01-24%2017.28.08%20-%20A%20minimalistic%20and%20cute%20illustration%20of%20a%20group%20of%20ducks%20working%20collaboratively%20around%20a%20table.%20The%20ducks%20are%20cartoonish%20and%20pastel-colored%2C%20with%20sim.webp)
---

**DID** is a lightweight, metadata-driven Extract-Load-Transform (ELT) framework designed for simplicity and efficiency.

- 💻 **No terminals, no SQL editors**: Everything happens within your favorite Python environment (e.g., Jupyter notebooks).
- 📂 **Metadata-driven ELT**: Easily manage your pipeline using YAML configurations and dbt manifests.
- ⚡ **Powered by DuckDB, Intake, and dbt**: Three open-source tools combined to deliver blazing-fast ELT workflows.

DID makes ELT approachable for analysts, engineers, and data enthusiasts alike. It's designed to just get ELT done.

---

## 🌟 Key Features

- **Seamless Metadata Integration**:

  - Use YAML files to define input catalogs and dbt manifests.
  - Save and reuse output catalogs for consistent workflows.

- **Python-Powered Simplicity**:

  - No need for external tools—write, run, and manage ELT pipelines directly in Python.

- **Blazing Performance**:

  - Leverage DuckDB for fast, in-memory data transformations.

---

## 🛠️ Example Workflow

With DID, you can execute an entire ELT workflow provided an intake catalog with your sources, and a dbt project in just a few lines of Python:

```
# Run it all with one method:
DID.do(
    input_cat_path='input_cat_file.yml',
    manifest_path=dbt_manifest_path,
    output_cat_path='output_cat_file.yml'
)
```

---

## 🤔 Why DID?

### ✨ Simplicity

- Focus on building pipelines—not wrestling with infrastructure.
- No need to learn additional tools or query languages.

### 🔄 Flexibility

- **Integrate easily**: Compatible with existing dbt projects and YAML-based catalogs.
- **Modular design**: Pick and choose components to fit your use case.

### 📈 Scalability

- From small datasets to enterprise-scale workloads, DID grows with you.

---

## 📥 Installation

DID is Python-based and can be installed directly via pip:

```bash
pip install did-framework
```

---

## 🚀 Getting Started

1. Define your **Input Catalog**:

   - Create a YAML file (`input_cat_file.yml`) describing your raw data sources.

2. Load your **dbt Manifest**:

   - Provide the path to the `manifest.json` generated by your dbt project.

3. Save your **Output Catalog**:

   - Use DID to generate a new YAML file with transformed data.

4. Automate with the `do` method:

   - Combine extraction, loading, and transformation in one step.

---

## 🤝 Contributing

We’re excited to build DID into the most developer-friendly ELT framework out there. Contributions are welcome! Feel free to submit issues, feature requests, or pull requests.

---

## 📧 Contact

Have questions or feedback? Reach out to us on GitHub or at [**did-support@eltducks.com**](mailto\:did-support@eltducks.com).

Let’s get ELT done—the ducking way!

# Underneath the hood 
## Extracts and Loads raw sources into duckdb

```
from did.do import extractload

raw_catalog = extractload('input_cat_file.yml')
```
# Tranform
## Transform raw sources, export materialized tables and views as an intake catalog
```
from did.do import transform

output_catalog = transform('path_to_manifest.json')
```




