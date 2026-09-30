![Build Status](https://github.com/ISE-FIZKarlsruhe/nfdi-dsai-ontology/actions/workflows/qc.yml/badge.svg)

# NFDI DSAI Ontology

The **NFDI DSAI Ontology** is a domain ontology for describing machine learning models, the processes through which they are developed and used, the machine learning tasks they perform, and the data, resources, and information artifacts associated with these processes.

The ontology is developed in the context of **NFDI4DataScience (NFDI4DS)** and aims to support the semantic description, integration, discovery, and reuse of research data and resources in Artificial Intelligence and Data Science.

> **Status: Work in Progress**  
> The ontology is under active development. Concepts, definitions, axioms, and alignments may change before a stable release.

## Goals and Scope

The ontology is centered around the **Machine Learning Model** and aims to describe:

- machine learning models and their characteristics;
- processes through which models are developed, trained, adapted, evaluated, deployed, and maintained;
- machine learning tasks performed by models;
- datasets, algorithms, computational resources, hyperparameters, evaluation metrics and results;
- provenance and relationships between models and the processes that produce or modify them.

The scope includes traditional machine learning models as well as pretrained and fine-tuned models, foundation models, large language models (LLMs), multimodal models, reinforcement learning models, and models trained from scratch.

## Research Data Lifecycle

The ontology represents the AI research data lifecycle through formally described processes:

**Preparation / Development → Training → Adaptation → Evaluation → Deployment / Use → Maintenance / Evolution**

Currently represented processes include preprocessing, random initialization, training, pre-training, training steps, fine-tuning, and evaluation. These processes connect ML models to their inputs, outputs, datasets, algorithms, computational resources, hyperparameters, checkpoints, metrics, and evaluation results.

Lifecycle coverage is still being extended.

## Machine Learning Tasks

A **Machine Learning Task** represents a computational problem performed by a machine learning model and is modeled as a planned process with specified inputs and outputs.

The task vocabulary originates primarily from **Hugging Face Tasks**, complemented by comparison with the **Artificial Intelligence Ontology (AIO)** and adapted according to NFDI DSAI competency questions and requirements.

The taxonomy covers several dimensions:

- **objective** — classification, generation, retrieval, detection, segmentation, etc.;
- **modality** — text, image, audio, video, tabular, etc.;
- **input-output transformation** — Image-to-Text, Audio-to-Text, Text-to-Image, etc.;
- **domain** — e.g. Natural Language Processing and Computer Vision;
- **multimodality**.

Rather than maintaining a large manually asserted polyhierarchy, **OWL axioms and reasoning** are used to derive relevant task classifications from their formal characteristics.

## Ontology Design

The ontology follows a **competency-question-driven development approach**. Competency questions determine which entities, relationships, and distinctions need to be represented.

The ontology reuses and aligns with established resources where appropriate, including **BFO, IAO, and OBI**.

A major design principle is to make classifications **derivable rather than manually asserted**. Inputs, outputs, modalities, and other characteristics are formally represented using OWL restrictions, allowing a reasoner to infer multiple perspectives on the same entity.

## Current Status and Roadmap

The NFDI DSAI Ontology is currently a **work in progress**, but already provides a substantial semantic resource for describing ML models, tasks, lifecycle processes, data items, modalities, and evaluation information.

Current development focuses on:

- refining definitions and logical axioms;
- validating the ML task taxonomy and reasoning results;
- extending lifecycle process coverage;
- refining modality and multimodality modeling;
- improving external ontology alignments;
- validation against competency questions and use cases;
- ontology quality and consistency checking.

The goal is to consolidate these developments into a **stable ontology release**.

Feedback, use cases, competency questions, and suggestions are welcome.

## Ontology Files

- **Editors' version:** [src/ontology/nfdi-dsai-edit.owl](src/ontology/nfdi-dsai-edit.owl)
- **Release versions** (OWL, Turtle, JSON; `-base` and `-full` variants) are published in the repository root and under [Releases](https://github.com/ISE-FIZKarlsruhe/nfdi-dsai-ontology/releases) once a stable release is available.

## Contact

Please use this GitHub repository's [Issue tracker](https://github.com/ISE-FIZKarlsruhe/nfdi-dsai-ontology/issues) to request new terms/classes, report errors, or share feedback and use cases.

## Acknowledgements

The NFDI DSAI Ontology is developed in the context of **NFDI4DataScience (NFDI4DS)**.

This ontology repository was created using the [Ontology Development Kit (ODK)](https://github.com/INCATools/ontology-development-kit).
