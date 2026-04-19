# UML-LLAMA-LoRA: Automated UML Use Case Generation via Fine-Tuning LLaMA-3.2-1B

## Overview

This repository contains the dataset, fine-tuned model components, and inference pipeline used in the research:

**"From Requirements to Diagrams: Automated UML Use Case Generation via Domain-Adaptive Fine-Tuning of Large Language Models"**

The objective is to automatically generate UML use case diagrams in **PlantUML format** from natural language software requirements using **LLaMA-3.2-1B** fine-tuned with **LoRA (Low-Rank Adaptation)**.

To ensure reproducibility, all dataset resources, model adapters, and evaluation scripts are publicly released.

---

## Dataset

The dataset contains:

- **6,884 requirement–PlantUML pairs**
- Natural language software requirements
- Corresponding UML use case diagrams in PlantUML
- Multiple domains (e.g., healthcare, education, e-commerce, systems)

### File

- `dataset_combine_final.json`

---

## Data Format

Each sample follows a structured JSON format:

```json
{
  "input": "The user logs into the system using email and password. The system validates credentials.",
  "output": "@startuml\nactor User\nUser -> System : Login request\nSystem -> User : Authentication result\n@enduml"
}
