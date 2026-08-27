# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

# Health Insurance Cost Analysis - Exploratory Data Analysis (EDA)

## Project Overview

This project performs an Exploratory Data Analysis (EDA) on a medical insurance dataset to identify the primary factors driving healthcare costs. The primary goal is to determine which customer attributes have the biggest impact on insurance charges and prepare the data for future predictive modelling.

## Dataset Content

The dataset (insurance.csv) contains 1,338 records with demographic, physical, and lifestyle features:

- age: Age of the primary beneficiary.
- sex: Gender of the insurance contractor (female, male).
- bmi: Body mass index, providing an understanding of body weights relative to height.
- children: Number of children covered by health insurance.
- smoker: Smoking status (yes, no).
- region: The beneficiary's residential area in the US (northeast, southeast, southwest, northwest).
- charges: Individual medical costs billed by health insurance.

## Project Setup & Execution

To run this project locally:

1. Clone this repository to your local system.
2. Create a virtual environment (.venv).
3. Install the required dependencies using the terminal command:
   pip3 install -r requirements.txt
4. Open the Jupyter Notebook in the jupyter_notebooks directory and select the Python environment kernel to execute the cells.

> Note on Interactive Visualisations: GitHub README files do not render interactive Plotly graphs. To interact with the 3D scatter plot, please open and run Health_Insurance.ipynb locally in VS Code or Jupyter.

## Business Requirements

To understand how different geographical, personal, and lifestyle factors affect healthcare insurance costs in the United States, in order to improve cost estimation.

### Hypotheses & Validation Strategy

1. Smoker Status: People who smoke are likely to have much higher medical charges than non-smokers.
2. BMI: Higher BMI is linked to higher medical charges.
3. Age: Insurance charges increase as age increases.
4. Demographics (Region, Sex, Children): Geographical region, sex, and number of children may also influence medical charges.

## Rationale Mapping: Business Requirements to Data Visualisations

Visualisation was the primary tool used to explore patterns, compare groups, and test hypotheses:

| Business Question / Hypothesis              | Visualisation Used                        | Rationale for Chart Selection                                                                                                                                            |
| :------------------------------------------ | :---------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Are smokers charged more than non-smokers?  | Boxplots, Histograms, Scatter Plots       | Clearly shows the separation and spread of charges between smokers and non-smokers. Scatter plots reveal how smoking multiplies costs across other continuous variables. |
| Does BMI affect medical charges?            | 2D Scatter Plots, Interactive 3D Plot     | BMI is continuous; scatter plots highlight trends and reveal critical threshold triggers (such as BMI >= 30).                                                            |
| Do charges increase with age?               | Scatter Plots                             | Shows the steady, linear increase in baseline charges as age increases.                                                                                                  |
| Do region, sex, or children affect charges? | Side-by-Side Bar Charts (with Smoker Hue) | Bar charts allow easy comparison of group averages across demographic categories, revealing that demographic variations are negligible compared to smoking status.       |
| How do all factors interact together?       | 6-Panel Summary Grid                      | Consolidates all 2D and distribution visualisations onto a single canvas for a 360-degree analytical review.                                                             |

## Project Plan

1. Data Collection & Setup: Downloaded raw dataset (insurance.csv) into the project folder structure.
2. Data Cleaning & Preprocessing: Checked for missing values, validated data types, and removed duplicate records (insurance_cleaned.csv).
3. Exploratory Data Analysis: Built individual continuous and categorical charts, interactive 3D plots, and multi-panel grids to test all hypotheses.
4. Summary Insights & Documentation: Consolidated analytical conclusions into Markdown cells, prepared next steps for modeling, and documented repository setup in the README.

## Analysis Techniques Used

Visual Exploratory Data Analysis (EDA) was structured step-by-step:

## Analysis Techniques Used

To explore the dataset, I picked specific charts based on the type of information I was looking at:

- **Single & Pair Charts:**
  - **Histograms & Boxplots:** Used to see how overall insurance charges are split up and spot extreme outliers in the data.
  - **Scatter Plots:** Used for continuous numbers like age and BMI to see if charges went up gradually as people got older or their BMI increased.
  - **Bar Charts:** Used to group people by categories (like region, sex, or number of kids) to compare average costs and distributions across groups.

- **Multi-Variable Charts:**
  - **Color Coding:** Added colour to charts (like colouring scatter points by "smoker") to see how smoking changes the relationship between age, BMI, and total cost.
  - **Interactive 3D Scatter Plot (Plotly):** Used to spin and look at Age, BMI, and Charges all at once in three dimensions.
  - **6-Panel Summary Grid:** Combined 6 different key plots onto one single figure to compare all major findings side-by-side.

- **AI Assistance:** Used Gemini and GitHub Copilot to troubleshoot code errors, suggest the best chart types for different variables, and refine analytical write-ups.

## Ethical Considerations

The dataset consists of anonymised data from Kaggle and poses no direct personal privacy risks.

## Unfixed Bugs & Knowledge Gaps

- Plotly VS Code Rendering: Initial issues with Plotly 3D graphs rendering inside VS Code were resolved by updating environment display settings (ipykernel).
- Knowledge Gaps Addressed: Improved understanding of multi-variable subplot layout management (plt.subplots) through experimentation, AI guidance, and Code Institute LMS documentation.

## Development Roadmap

- Challenges Overcome: Effectively combining multiple categorical and continuous variables onto figures.
- Learning which plots to use for each type of data.
- Next Steps for Skill Development: Learn predictive analysis and predictive modelling.

## Main Data Analysis Libraries

- Pandas: Data loading, cleaning, and describing.
- Matplotlib & Seaborn: scatter, bar, box and 6-panel summary plots.
- Plotly Express: Interactive 3D scatter plot.

## Credits & Acknowledgments

- Educational Materials & LMS: Code Institute Data Analytics with AI course modules:
  - Virtual Environments in Python, Version Control Basics, Working with Git, and Documentation (Introduction to the README).
  - Data Manipulation: Pandas, Visualisation with Matplotlib, Advanced visualisation with Seaborn, and Interactive web-based visualisation with Plotly.
  - Logo image
- Base Repository Template: Code Institute Data Analytics Capstone Template.
- AI:
  - Gemini (Generative AI): Used as an interactive AI tutor and assistant to structure, draft, and refine the final README.md file as well as assist with plot selection guidance, environment troubleshooting, user stories and text formatting for insights.
  - GitHub Copilot: Used for inline code completion and syntax assistance throughout notebook development.
  - Jayne Lawley for code to save cleaned data.
  - Pete Daniel Smith for the idea of showing a 3d scatter plot.
- Acknowledgements: Special thanks to my husband, my tutors and colleagues from Code Institute for their support.
