# UML Generation via LLaMA-3.2-1B with LoRA Fine-Tuning

## Overview

This repository presents a complete pipeline for **automatic generation of UML Use Case diagrams in PlantUML format from natural language requirements**.

The system is based on **LLaMA-3.2-1B**, fine-tuned using **LoRA (Low-Rank Adaptation)** on a custom dataset of software requirements and UML diagrams.

The objective is to evaluate the ability of large language models to transform textual requirements into structured UML representations.

---

## Dataset

The dataset used in this work is:

- File: `dataset_combine_final.json`
- Size: **6,884 requirement–PlantUML pairs**
- Format: JSON (input → output pairs)
- Domain: Software engineering requirements

### Structure

Each sample is defined as:

```json
{
  "input": "Natural language software requirement",
  "output": "@startuml ... @enduml"
}
