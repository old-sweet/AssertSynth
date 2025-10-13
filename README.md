# 🧩 AssertSynth Prompt and Experimental Dataset

> **Tian, E., Ci, Y., Yang, Q., Li, Y., & Lyu, Z. (2025).**
> *AssertSynth: LLM-Based Assertion Synthesis via Multimodal Specification Extraction.*

This repository provides **all prompt templates** and **experiment design data (RTL + SPEC)** used in our paper.  
It aims to ensure full reproducibility of the *AssertSynth* framework’s LLM-driven assertion synthesis process.

---

## 🔍 Repository Contents

| Folder | Description |
|---------|--------------|
| [`prompts/`](./prompts) | All LLM prompt templates used in AssertSynth pipeline |
| [`designs/`](./designs) | Three experimental hardware designs (I2C, AES, OpenMSP430), including RTL and multimodal specifications |

---

## 🧠 AssertSynth Prompt Hierarchy

| Stage | Prompt File | Purpose |
|--------|--------------|----------|
| **1️⃣ Preprocessing** | `preprocess_prompt.txt` | Unified modality + semantic classification |
| **2️⃣ Multimodal Extraction** | `text_extraction_prompt.txt` / `table_extraction_prompt.txt` / `diagram_extraction_prompt.txt` / `formula_extraction_prompt.txt` | Extract structured data from heterogeneous spec formats |
| **3️⃣ SVA Generation** | `sva_generation_prompt.txt` | 4-step CoT prompting to synthesize assertions |
| **Optional Refinement** | `sva_refinement_prompt.txt` | Mutation-guided feedback refinement |

Each prompt is documented with example input/output and expected LLM behavior in [`prompts/README_prompts.md`](./prompts/README_prompts.md).

---

## ⚙️ Experimental Designs

The `designs/` directory contains the three RTL modules used in our experiments:

| Design | Source | Description |
|---------|---------|-------------|
| **I2C** | OpenCores (Herveille, 2003) | Small-scale control module with timing-critical behavior |
| **AES** | OpenCores (Hsing, 2013) | Medium-scale crypto datapath design |
| **OpenMSP430** | OpenCores (Girard, 2009) | Large-scale processor subsystem |

Each subdirectory includes:
- `rtl/` — the Verilog design and testbench files  
- `spec/` — multimodal specification documents used as input for AssertSynth

---

## 📘 Citation

If you use these prompts or datasets in your research, please cite:
