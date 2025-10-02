# Paper Airplane Flight Distance Experiment

## Overview

This project investigates how the placement of paper clips affects the
**gliding distance of paper airplanes**. Using a **full factorial design
(2³)**, the study evaluates main effects and interaction effects of
placing clips on the **nose, middle, and rear** of the airplane.

The goal is to understand the role of **mass distribution** in flight
stability and performance, while also providing an accessible example of
**experimental design, ANOVA, and interaction effects**.

------------------------------------------------------------------------

## Dataset

-   **Pilot data**: `pilot_data.xlsx` --- preliminary study with 8 cells
    × 3 replicates.
-   **Main data**: `airplane_data.xlsx` --- full factorial study with 8
    cells × 8 replicates.
-   **Variables**:
    -   `nose` --- binary factor: paperclip at nose (yes/no)
    -   `middle` --- binary factor: paperclip at middle (yes/no)
    -   `rear` --- binary factor: paperclip at rear (yes/no)
    -   `distance` --- gliding distance (cm)

------------------------------------------------------------------------

## Methods

1.  **Design**: Complete **2³ factorial design** (3 binary factors, 8
    treatment combinations).
2.  **Randomization**: Throw order randomized in R to avoid bias.
3.  **Measurement**: Distance measured in cm from launch to first ground
    contact.
4.  **Statistical Analysis**:
    -   Pilot regression model to estimate coefficients and plan sample
        size (80% power).
    -   Linear regression (`lm`) and **ANOVA** for main and interaction
        effects.
    -   Residual checks: histogram, Q--Q plot, Shapiro--Wilk test,
        fitted vs residual plots.
5.  **Validation**: Confirmed assumptions of normality, independence,
    and homoscedasticity.

------------------------------------------------------------------------

## Key Findings

-   **Rear clip**: Strong negative effect on flight distance (**p \<
    0.0001**).
-   **Middle clip**: Moderate negative effect (**p ≈ 0.0004**).
-   **Nose clip**: No significant main effect (p ≈ 0.079), but strong
    **interaction effects**.
-   **Interactions**:
    -   Nose × Middle (p \< 0.0001)
    -   Nose × Rear (p \< 0.0001)
    -   Nose × Middle × Rear (p \< 0.0001)
-   **Best performance**: No clips attached --- mean glide ≈ **662.8
    cm**.
-   **Worst performance**: Rear clip attached --- mean glide ≈ **404.3
    cm**.

------------------------------------------------------------------------

## Installation & Requirements

The analysis is conducted in **R**. Required packages:

``` r
install.packages(c("readxl", "ggplot2", "dplyr", "broom", "knitr"))
```

Clone/download this repo, then run `Final Project.Rmd` in RStudio.

------------------------------------------------------------------------

## Usage

1.  Place `pilot_data.xlsx` and `airplane_data.xlsx` in your working
    directory.
2.  Open `Final Project.Rmd` in RStudio.
3.  Knit the R Markdown file to generate plots, ANOVA tables, and
    summary outputs.

------------------------------------------------------------------------

## Deliverables

-   `Final Project.Rmd` --- reproducible R Markdown with analysis.
-   `Final-Project.pdf` --- formatted final report with results.
-   `pilot_data.xlsx` --- pilot dataset.
-   `airplane_data.xlsx` --- main factorial dataset.

------------------------------------------------------------------------

## Educational Value

This experiment doubles as an **educational demonstration** of:
- Factorial design and interaction effects.
- Hands-on exploration of aerodynamics and physics.
- Use of ANOVA and regression diagnostics in R.

------------------------------------------------------------------------

## License

This project is for academic and educational purposes only.
