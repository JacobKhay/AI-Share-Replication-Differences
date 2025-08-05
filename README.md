# AI Jobs Weighting Analysis

**🔗 [View the Project Website](https://jacobkhaykin.github.io/ai-jobs-weighting-analysis/)**

## Overview

When studying AI job adoption across U.S. counties, should we weight by population or log-population? This analysis uses county-level data from Lightcast job postings, U.S. Census demographics, and USPTO patent records spanning 2014-2023, originally analyzed by Andreadis et al. (2025). I re-estimated their regression models comparing standard population weights against log-population weights to assess whether large metropolitan areas drive the key relationships. I fitted linear regression models predicting AI job share as a function of county demographics, innovation indicators, and industry characteristics, comparing results between population-weighted and log-population-weighted specifications. Labor market tightness emerges as the most robust predictor of AI adoption across all county sizes, while education effects appear concentrated in large metropolitan areas.

## Key Findings

- **Labor market tightness** is the most robust predictor of AI job adoption across all weighting schemes
- **Bachelor's degree effects** are substantially reduced under log-population weighting, suggesting they may be driven by large metropolitan areas
- **STEM education** remains consistently important across county sizes
- **Manufacturing intensity** shows persistent negative relationships with AI adoption
- **Innovation capacity** (patents per employee) matters regardless of county size

## Repository Structure

```
├── README.md
├── _quarto.yml                 # Quarto website configuration
├── index.qmd                   # Home page with key findings
├── about.qmd                   # About the author and project
├── sources.qmd                 # Data sources and methodology
├── model.qmd                   # Statistical model details
├── data/                       # Data files (if included)
├── scripts/                    # R analysis scripts
│   ├── data_cleaning.R
│   └── weighting_analysis.R
└── plots/                      # Generated visualizations
    ├── ai_share_coefficients.png
    └── ai_change_coefficients.png
```

## Data Sources

- **Lightcast**: Job posting data from 40,000+ online sources
- **U.S. Census ACS**: County demographics (2013-2022)
- **USPTO PatentsView**: Innovation indicators
- **BLS**: Labor market statistics
- **FHFA**: Housing price data

## Methodology

This project extends the analysis by Andreadis et al. (2025) by comparing two weighting schemes:

1. **Population weights**: `w = Population`
2. **Log-population weights**: `w = log(Population)`

The comparison reveals how county size affects the interpretation of key predictors of AI job adoption.

## Technical Details

- **Models**: Linear regression with county and year fixed effects
- **Time Period**: 2014-2023
- **Observations**: 24,645 county-year observations
- **Standard Errors**: Clustered at county level
- **Software**: R with tidymodels framework

## Key Visualizations

The project includes coefficient comparison plots showing how estimates change between weighting schemes across five different model specifications, highlighting the sensitivity of findings to methodological choices.

## Implications

These findings suggest that:
- Policymakers should focus on creating tight labor market conditions to encourage AI adoption
- Education-focused strategies may be less universally applicable than previously thought
- Different approaches may be needed for large metropolitan areas vs. smaller counties

## Author

**Jacob Khaykin**  
📧 [jacob.khaykin@example.com](mailto:jacob.khaykin@example.com)  
🐙 [GitHub](https://github.com/jacobkhaykin)

## Acknowledgments

This project was created as part of [Kane's Data Science Bootcamp](https://bootcamp.davidkane.info/). I thank Andreadis et al. (2025) for their transparent methodology that enabled this extension analysis.

## License

This project is open source and available under the [MIT License](LICENSE).

---

*Created: August 2025*
