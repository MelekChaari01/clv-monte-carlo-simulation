# Customer Lifetime Value — Monte Carlo Simulation

A Monte Carlo simulation framework for estimating Customer Lifetime Value (CLV), built around a Markov-chain model of the customer journey (Visitor → Lead → Customer → Inactive → Churned).

Business Simulation course group project, MSc AI for Business Transformation (SKEMA Business School / ESIEA).

## Approach
- Customers move between engagement states according to a transition matrix (`P`).
- While in the "Customer" state, purchases arrive as a Poisson process, with log-normal purchase amounts.
- Future cash flows are discounted at a fixed rate to estimate each simulated customer's CLV and lifetime.
- 20,000 Monte Carlo replications are used to estimate expected CLV, expected lifetime, and the associated standard errors / convergence diagnostics.

## Contents
- `CLV_Monte_Carlo_Simulation.Rmd` — full R Markdown source (model definition, simulation code, statistical analysis).
- `Customer_Lifetime_Value_Estimation_Report.pdf` — knitted final report.

## Reproducing
Open the `.Rmd` in RStudio and knit to PDF (requires a working LaTeX installation, e.g. via `tinytex::install_tinytex()`). A fixed seed (`set.seed(123)`) makes the simulation reproducible.

## Team
Group project — add your teammates' names here.
