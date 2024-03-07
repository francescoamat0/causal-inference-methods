# Causal Inference Methods

This repository is a collection of notebooks & analyses exploring Bayesian and Frequentist statistical techniques to asses causal impact using observational (quasi-experimental) data, which is often encountered in real-world scenarios where controlled and fully randomised experiments are not feasible.

## Introduction to Causal Inference 🧑‍🏫

Unlike randomized controlled trials such as A/B tests, where causality can (generally) be straightforwardly inferred, observational data presents unique challenges. Causal inference methods for observational data come into play when we need to draw conclusions about causality in situations where controlled experimentation is not possible or ethical. These methods employ statistical techniques to mimic the conditions of a randomized experiment, thereby providing insights into causal relationships from naturally occurring datasets.

### Why Causal Inference?
Causal inference is crucial in fields like epidemiology, economics, social sciences, and more, enabling decision-makers to evaluate the effectiveness of interventions, policies, or treatments based on real-world evidence.

## Learning Resources 📚

To lear more abour the topic of causal inference and its applications, I  recommend this really well-done online book:
- [Python Causality Handbook](https://matheusfacure.github.io/python-causality-handbook/landing-page.html) by Matheus Facure. This comprehensive guide provides an excellent introduction to causal inference techniques with practical Python examples.

## Getting Started 🚀

To run the analyses and notebooks within this repository, follow these simple steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/francescoamat0/causal-inference-methods.git
   ```

2. **Set up a virtual environment:**
Navigate to the repository directory and create a virtual environment. You'll also need Python 3.11.8. For example, using conda:

    ```bash
    cd causal-inference-methods
    conda create --name myenv python=3.11.8
    ```

    Activate the virtual environment:
    ```bash
    conda activate myenv
    ```

3. **Install dependencies**:
    Install the required Python packages using the requirements.txt file:

    ```bash
    pip install -r requirements.txt
    ```