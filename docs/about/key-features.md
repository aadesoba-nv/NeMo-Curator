---
description: "Comprehensive overview of NeMo Curator's key features for text, image, and video data curation with deployment options"
categories: ["concepts-architecture"]
tags: ["features", "benchmarks", "deduplication", "classification", "gpu-accelerated", "distributed", "deployment-operations"]
personas: ["data-scientist-focused", "mle-focused", "admin-focused", "devops-focused"]
difficulty: "beginner"
content_type: "concept"
modality: "universal"
---

(about-key-features)=
# Key Features

NeMo Curator is an enterprise-grade platform for scalable, privacy-aware data curation across text, image, and video. It empowers teams to prepare high-quality, compliant datasets for LLM and AI training, with robust support for distributed, cloud-native, and on-premises workflows. NeMo Curator is trusted by leading organizations for its modular pipelines, advanced filtering, and seamless integration with modern MLOps environments.

## Why NeMo Curator?

- Trusted by leading organizations for LLM and generative AI data curation
- Open source, NVIDIA-supported, and actively maintained
- Seamless integration with enterprise MLOps and data platforms (Kubernetes, Slurm, Spark, Dask)
- Proven at scale: from laptops to multi-node GPU clusters

### Benchmarks & Results

- **Deduplicated 1.96 trillion tokens in 0.5 hours** using 32 NVIDIA H100 GPUs (RedPajama V2 scale)
- Up to **80% data reduction** and significant improvements in downstream model performance (see ablation studies)
- Efficient curation of Common Crawl: from 2.8TB raw to 0.52TB high-quality data in under 38 hours on 30 CPU nodes

---

## Text Data Curation

NeMo Curator offers advanced tools for text data loading, cleaning, filtering, deduplication, classification, and synthetic data generation. Built-in modules support language identification, quality estimation, domain and safety classification, and both rule-based and LLM-based PII removal. Pipelines are fully modular and can be customized for diverse NLP and LLM training needs.

::::{grid} 1 1 2 2
:gutter: 2

:::{grid-item-card} {octicon}`database;1.5em;sd-mr-1` Data Loading
:link: about-concepts-text-data-loading
:link-type: ref
Efficiently load and manage massive text datasets, with support for common formats and scalable streaming.
:::

:::{grid-item-card} {octicon}`gear;1.5em;sd-mr-1` Data Processing
:link: about-concepts-text-data-processing
:link-type: ref
Advanced filtering, deduplication, classification, and pipeline design for high-quality text curation.
:::

:::{grid-item-card} {octicon}`zap;1.5em;sd-mr-1` Synthetic Data & PII Removal
:link: about-concepts-text-data-gen
:link-type: ref
LLM-driven synthetic data generation, prompt engineering, and privacy-preserving PII removal for text datasets.
:::

:::{grid-item-card} {octicon}`rocket;1.5em;sd-mr-1` Text Curation Quickstart
:link: gs-text
:link-type: ref
Set up your environment and run your first text curation pipeline with NeMo Curator.
:::

::::

---

## Image Data Curation

NeMo Curator supports scalable image dataset loading, embedding, classification (aesthetic, NSFW, etc.), filtering, deduplication, and export. It leverages state-of-the-art vision models (for example, CLIP, timm) and DALI for efficient GPU-accelerated processing. Modular pipelines enable rapid experimentation and integration with text and multimodal workflows.

::::{grid} 1 1 2 2
:gutter: 2

:::{grid-item-card} {octicon}`database;1.5em;sd-mr-1` Data Loading
:link: about-concepts-image-data-loading
:link-type: ref
Load and manage large-scale image datasets for curation workflows.
:::

:::{grid-item-card} {octicon}`gear;1.5em;sd-mr-1` Data Processing
:link: about-concepts-image-data-processing
:link-type: ref
Embedding generation, classification (aesthetic, NSFW), filtering, and deduplication for images.
:::

:::{grid-item-card} {octicon}`device-camera;1.5em;sd-mr-1` Data Export
:link: about-concepts-image-data-export
:link-type: ref
Export, save, and reshard curated image datasets for downstream use.
:::

:::{grid-item-card} {octicon}`rocket;1.5em;sd-mr-1` Image Curation Quickstart
:link: gs-image
:link-type: ref
Set up your environment and install NeMo Curator's image modules.
:::

::::

---

## Deployment and Integration

NeMo Curator is designed for distributed, cloud-native, and on-premises deployments. It supports Kubernetes, Slurm, and Spark, and integrates easily with your existing MLOps pipelines. Modular APIs and CLI tools enable flexible orchestration and automation.

::::{grid} 1 1 2 2
:gutter: 2

:::{grid-item-card} {octicon}`cloud;1.5em;sd-mr-1` Deployment Options
:link: admin-overview
:link-type: ref
Deploy on Kubernetes, Slurm, or Spark. See the Admin Guide for full deployment and integration options.
:::

:::{grid-item-card} {octicon}`database;1.5em;sd-mr-1` Memory Management
:link: reference-infra-memory-management
:link-type: ref
Optimize memory usage and partitioning for large-scale curation workflows.
:::

:::{grid-item-card} {octicon}`zap;1.5em;sd-mr-1` GPU Acceleration
:link: reference-infra-gpu-processing
:link-type: ref
Leverage NVIDIA GPUs for faster data processing and pipeline acceleration.
:::

:::{grid-item-card} {octicon}`sync;1.5em;sd-mr-1` Resumable Processing
:link: reference-infra-resumable-processing
:link-type: ref
Continue interrupted operations and recover large dataset processing with checkpointing and batching.
:::

::::
