# COVID VACCINE OPTIMIZATION ANALYSIS

## Overview

This project focuses on analyzing and optimizing the distribution of COVID-19 vaccines across different countries. The analysis involves exploring key features such as country, total population, people vaccinated, date, vaccines used, data sources, and the percentage of the population remaining unvaccinated. To enhance decision-making in vaccine allocation, the project employs linear programming to minimize the total number of unvaccinated people while considering constraints on the total vaccine supply.

## Project Structure

### Data Exploration

The project starts with data exploration, utilizing the pandas library to load and analyze the dataset. The dataset, presumably named 'covid_vaccine_population.csv,' is inspected to understand its structure and contents. The basic information, descriptive statistics, missing values, and column names are displayed to provide an initial understanding of the data.

### Data Visualization

Visualizations are created to offer a more intuitive understanding of the dataset. Three visualizations are generated:

1. **Bar chart for Total Population by Country:** This visualization provides a comparative view of the total population across different countries, facilitating a quick understanding of population distribution.

2. **Pie chart for Percentage of Population Unvaccinated (Top Ten Countries):** Focusing on the top ten populous countries, this pie chart visually represents the percentage of the population that remains unvaccinated in each country.

3. **Scatter plot for Total Population vs. People Vaccinated (Top Ten Countries):** This scatter plot illustrates the relationship between total population and the number of people vaccinated for the top ten countries. Each point represents a country, and the color distinguishes between them.

### Linear Programming for Vaccine Allocation

The core of the project involves optimizing vaccine allocation using linear programming. The `pulp` library is utilized to create a linear programming problem with the objective of minimizing the total number of unvaccinated people. The decision variables are defined for each country, representing the number of vaccines allocated and the number of unvaccinated people.

#### Objective Function and Constraints:

1. **Objective Function:** The primary goal is to minimize the total number of unvaccinated people.

2. **Constraint 1: Total Vaccine Supply:** A constraint is set on the total vaccine supply, assuming a fixed total of 7 billion units.

3. **Constraint 2: Number of Unvaccinated People:** For each country, the number of unvaccinated people is constrained by the total population minus the people already vaccinated and the vaccines allocated.

#### Solving the Linear Programming Problem:

The linear programming problem is solved, and the optimal vaccine allocation is printed, indicating the number of vaccines to be allocated to each country.

#### Evaluation and Validation:

The results are evaluated by calculating the objective value (total number of unvaccinated people) and validating the constraints. The validation includes checking whether the total allocated vaccines are within the specified supply limit and verifying that the number of unvaccinated people aligns with the defined constraints.

## Conclusion

In conclusion, this analysis provides valuable insights into COVID-19 vaccine distribution. By leveraging linear programming, the project offers an optimal vaccine allocation strategy aimed at minimizing the number of unvaccinated individuals. The inclusion of visualizations enhances the interpretability of the findings, while the linear programming model provides a systematic approach to decision-making in vaccine distribution.
