# RW-Steering: Rescorla-Wagner Steering of LLMs under Disproportionate Inappropriate Context

## Overview

Welcome to the repository for RW-Steering: Rescorla-Wagner Steering of LLMs under Disproportionate Inappropriate Context. This repository contains datasets and resources supporting our research on LLM robustness when helpful context is blended with inappropriate content (fake news, hate speech, non-factual statements, and privacy-sensitive information). The included files provide raw source pools, derived training/evaluation sets, and prompt templates to facilitate replication and extension of our results.

The paper, RW-Steering: Rescorla-Wagner Steering of LLMs under Disproportionate Inappropriate Context, has been uploaded to this repository. You may refer to the paper to understand the research objectives, data construction methodology, evaluation metrics, and key findings.

We use LMFlow for training and evaluation: https://github.com/OptimalScale/LMFlow
.

## Repository Contents

This repository contains the following files and datasets:

### 1. raw_data/

This directory contains the raw source pools used to build all downstream datasets. It is organized by content type:

fakenews_output/

hate_speech_output/

non_factual_output/

privacy_output/

For details of the data construction and validation pipeline, please see our paper.

### 2. datasets/alignment_finetuning/

This directory provides supervised alignment data constructed from mixed contexts. It is intended for alignment fine-tuning experiments where models learn to produce preferred answers despite the presence of inappropriate context.

### 3. datasets/enhancing_awareness/

This directory contains auxiliary datasets that teach models to judge context appropriateness (e.g., identify and discount inappropriate segments) to enhance safety awareness during generation.

### 4. datasets/generalizable/ (RW-Steering)

This directory includes data for generalizable approaches based on RW-Steering, where targets first elicit an appropriateness judgment and then the final answer, improving robustness across contamination levels.

### 5. datasets/mixtures_0_to_10/

This directory offers evaluation splits where the proportion of inappropriate information is systematically varied from 0% to 10%, enabling controlled stress tests and behavior-curve analyses.

### 6. evaluation_prompt/

This directory contains prompt templates for automatic evaluation:

cleanliness_evaluation/ — prompts for the Cleanliness metric (answers free of inappropriate content).

consistency_evaluation/ — prompts for the Consistency metric (semantic agreement with reference answers).

Feel free to open an issue or contact us for any questions or clarifications.

**Contributors:** Rushi Wang, Jiateng Liu, Cheng Qian, Yifan Shen, Yanzhou Pan, Zhaozhuo Xu, Ahmed Abbasi, Heng Ji, Denghui Zhang\
