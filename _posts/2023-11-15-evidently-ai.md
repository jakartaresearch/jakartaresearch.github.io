---
layout: post
title: Hands-On - Evidently AI
---

[Official Website](https://www.evidentlyai.com/)<br>
Evidently AI is a platform that specializes in explaining machine learning models, providing transparency and interpretability in their predictions. It helps data scientists and machine learning practitioners understand, visualize, and communicate the behavior of their models. By offering insights into model performance and potential biases, Evidently AI contributes to building more trustworthy and understandable artificial intelligence applications.

## Core Concepts
[Core Concepts](https://docs.evidentlyai.com/readme/core-concepts)<br><br>

This is an explanatory page to describe the key features and concepts at Evidently.<br>

**TL;DR**

Evidently helps evaluate, test and monitor ML models in production.
- A **Metric** is a core component of Evidently. You can combine multiple **Metrics** in a **Report**. Reports are best for visual analysis and debugging of your models and data.
- A **Test** is a metric with a condition. Each test returns a pass or fail result. You can combine multiple **Tests** in a **Test Suite**. Test Suites are best for automated model checks as part of an ML pipeline.

For both Tests and Metrics, Evidently has **Presets**. These are pre-built combinations of metrics or checks that fit a specific use case.

- A **Snapshot** is a JSON version of the **Report** or a **Test Suite** which contains measurements and test results for a specific period. You can log them over time and run an Evidently Monitoring Dashboard for continuous monitoring.


## Tutorials

- [What is Evidently?](https://docs.evidentlyai.com/)
- [Hello Word Example](https://docs.evidentlyai.com/get-started/hello-world)
- [Quickstart for Reports and Tests](https://docs.evidentlyai.com/get-started/tutorial)
- [Quickstart for ML Monitoring](https://docs.evidentlyai.com/get-started/tutorial-monitoring)
