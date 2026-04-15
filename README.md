# Fabric-assignment_Synapx
## 📘 Setup Instructions Before Running Notebooks & Pipeline

Before executing the notebooks and pipeline, please ensure the following setup steps are completed.

---

### 1. Workspace Setup
Create a new workspace or use an existing workspace where all resources (notebooks, pipelines, and lakehouse) will be deployed.

---

### 2. Lakehouse Setup
Create a new Lakehouse or attach an existing Lakehouse to your workspace.

---

### 3. Notebook Configuration
Open the notebook at least once and connect it to the Lakehouse:

- Go to **Data Items**
- Attach your Lakehouse

Ensure the Lakehouse contains a folder named:

```
Files
```

This folder is required for pipeline execution and data storage.

---

## 🚀 Running the Pipeline

Once the above setup is complete:

### Step 1: Create Pipeline
Create a new pipeline in your workspace.

### Step 2: Add JSON Definition
Paste the provided pipeline JSON into the pipeline editor.

### Step 3: Configure Parameters
Add the required pipeline parameters:

```json
{
  "tables_str": "<your_table_list>",
  "bronze": "<bronze_layer_name>",
  "silver": "<silver_layer_name>",
  "gold": "<gold_layer_name>",
  "workspace": "<workspace_name>",
  "lakehouse": "<lakehouse_name>"
}
```

---

## ✅ You're Ready!

Once everything is configured, you can execute the pipeline successfully. All notebooks will run in sequence and process data through Bronze → Silver → Gold layers.
