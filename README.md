# Causal Inference Methods [WIP]

This work-in-progress 🚧 repository is a collection of notebooks & analyses exploring Bayesian and Frequentist statistical techniques to asses causal impact using observational (quasi-experimental) data, which is often encountered in real-world scenarios where controlled and fully randomised experiments are not feasible.

## Brief Introduction to Causal Inference 🧑‍🏫

Unlike randomized controlled trials such as A/B tests, where causality can (generally) be straightforwardly inferred, observational data presents unique challenges. Causal inference methods come into play when we need to draw conclusions about causality in situations where controlled experimentation is not possible, practical or ethical, thus when we aim to evaluate the causal impact of an intervention or treatment but lack the element of random assignment of participants to treatment and control groups found in true experiments. These methods employ statistical techniques to mimic the conditions of a randomized experiment, thereby providing insights into causal relationships from naturally occurring datasets.

### Why Causal Inference?
Causal inference is crucial in fields like epidemiology, economics, social sciences, and more, enabling decision-makers to evaluate the effectiveness of interventions, policies, or treatments based on real-world evidence.

### Commom Methods for Causal Inference
Below are some common statistical methods used for causal inference. The folder structure of this repository will follow this list accordingly.

#### Synthetic Control

The synthetic control method creates a synthetic version of the treatment group (the entity that received the intervention) from a weighted combination of control units (entities that did not receive the intervention). This method is particularly useful for case studies where there is only one unit or a few units in the treatment group, making traditional comparative studies challenging. It can be used, for example, for 'geolift' studies, where we analyse the impact of an intervention (eg. a new marketing campaign, changes in local operations, etc.) in a given geographical region and have other untreated units that we can use to build a counterfactual for what would have happened had the intervention not taken place. 
The key assumption of this method is that the synthetic control is a good approximation of the treated unit in the absence of treatment. 

#### Difference in Differences (DiD)

Difference in Differences (DiD) is a quasi-experimental technique that compares the changes in outcomes over time between a group that is exposed to a treatment and a group that is not. This method is best suited for situations where data is available for both treatment and control groups before and after an intervention. 
This method relies on the "parallel trends" assumption, which posits that, in the absence of treatment, the treatment and control groups would have followed parallel paths over time. This assumption might be violated, for example, if there are other events happening after the treatment time that differentially affect the treatment and control groups.

#### Regression Discontinuity (RD)

Regression Discontinuity (RD) design is used when the assignment of treatment is based on a cutoff point in an assignment variable. It compares the outcomes for observations just below and just above the cutoff to estimate the treatment effect. RD is particularly powerful when there's a clear, predefined rule for assigning treatments, making it ideal for evaluating the effects of scholarship programs, eligibility criteria for programs, and more. 
The fundamental assumption of this method is that units just above and below the cutoff are essentially identical in all respects except for the treatment. This implies a continuity in the baseline characteristics around the cutoff point, allowing for a credible comparison. For instance, if individuals can precisely control their position relative to the cutoff (e.g., scoring just above a test threshold), the assumption of randomness around the cutoff would be violated.

#### Instrumental Variable Regression (IV)

Instrumental Variable Regression is a technique used when controlled experimentation isn't possible and there's potential for endogeneity or confounding in the relationship between the treatment and outcome variables. An instrumental variable (IV) is a variable that is correlated with the treatment but not directly with the outcome variable, except through its effect on the treatment.
For this method to work well, the instrument must have an (ideally) strong correlation with the treatment variable (relevance), should be not directly associated with the outcome except through the treatment (exclusion restriction), and should not share common causes with the outcome (independence). These assumptions ensure that the instrument effectively isolates the variation in the treatment variable that is exogenous to the outcome.

_Note: we won't cover here the field of Causal Graphical Modelling, an approach that utilises causal diagrams, also known as Directed Acyclic Graphs (DAGs), to represent and reason about causal relationships._

## Learning Resources 📚

To learn more about the topic of causal inference and its applications, I recommend this really well-done online book:
- [Python Causality Handbook](https://matheusfacure.github.io/python-causality-handbook/landing-page.html) by Matheus Facure. This comprehensive guide provides an excellent introduction to causal inference techniques with practical Python examples.

## Getting Started 🚀

To run the analyses and notebooks within this repository, follow these simple steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/francescoamat0/causal-inference-methods.git
   ```

2. **Set up a virtual environment:**
Navigate to the repository directory and create a virtual environment. You'll also need Python 3.11.8 to ensure full compatibility. For example, using conda:

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