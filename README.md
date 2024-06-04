# Anchoring Bias in Text Generation Models

This repository contains code for evaluating and mitigating anchoring bias in text generation models. The project explores how text generation models, such as GPT-2 and GPT-3 variants, exhibit anchoring bias and attempts to mitigate this bias through prompt engineering.

## Table of Contents

- [Introduction](#introduction)
- [Setup Environment](#setup-environment)
- [Testing for Anchoring Bias - Creating Benchmark](#testing-for-anchoring-bias---creating-benchmark)
- [Model Initialization](#model-initialization)
- [Extracting Numeric Value](#extracting-numeric-value)
- [Generating Results](#generating-results)
- [Statistical Analysis](#statistical-analysis)
- [De-Biasing Using Prompt Engineering](#de-biasing-using-prompt-engineering)
- [De-Biasing Results](#de-biasing-results)
- [Summary and Discussion](#summary-and-discussion)

## Introduction

Anchoring bias is a cognitive bias that can affect decision-making processes. In the context of text generation models, anchoring bias may lead models to rely too heavily on the first piece of information provided (the anchor) when generating text. This project aims to investigate anchoring bias in text generation models and mitigate it through prompt engineering techniques.

## Setup Environment

The project environment setup includes installing necessary libraries and dependencies for running the code. It uses libraries such as `bitsandbytes`, `transformers`, and `accelerate` for model training and evaluation.

## Testing for Anchoring Bias - Creating Benchmark

A benchmark is created to test anchoring bias in text generation models. It consists of prompts related to various product categories, with each prompt containing a basic value estimation and an anchored value based on a specific sale price.

## Model Initialization

Text generation models are initialized and prepared for execution using the specified model names. Models such as "TinyPixel/Llama-2-7B-bf16-sharded", "EleutherAI/gpt-j-6B", and "mistral-community/Mistral-7B-v0.2" are used in the project.

## Extracting Numeric Value

A function is implemented to extract numeric values from the generated text output of text generation models. Regular expressions are used to identify numerical patterns in the text and extract relevant information.

## Generating Results

The models are run on the benchmark dataset, and results including model predictions, anchored prices, and extracted values are saved to a CSV file for further analysis.

## Statistical Analysis

Statistical analysis is performed on the benchmark results to evaluate anchoring bias in text generation models. Metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and t-tests are used to assess bias and compare model predictions.

## De-Biasing Using Prompt Engineering

Prompt engineering techniques are employed to mitigate anchoring bias in text generation models. Additional context is added to prompts to encourage models to consider a broader range of factors when generating text.

## De-Biasing Results

The effectiveness of prompt engineering in reducing anchoring bias is evaluated through statistical analysis comparing model predictions with engineered prompts to anchored prices.

## Summary and Discussion

The project concludes with a summary and discussion of the findings, highlighting the impact of anchoring bias in text generation models and the potential of prompt engineering to mitigate bias.

