# Lab 1: Passing Pollinators

## Overview
This project analyzes pollinator activity data from a local farm to understand bee behavior, optimal weather conditions, and flower nectar production patterns.

## Project Structure
```
lab_1/
├── data/
│   └── pollinator_activity_data.csv    # Dataset with pollinator observations
├── index.md                            # Main dashboard (Observable Plot)
└── README.md                           # This file
```

## Dataset Description
The dataset contains 240 observations from June 1-30, 2024, across four garden plots with the following variables:

- **Date & Time**: Observation date, hour, and minute
- **Location**: Four garden plots (A, B, C, D)
- **Weather**: Temperature (14-32°C), humidity (30-90%), wind speed (1-19 km/h), conditions
- **Flowers**: Lavender, Sunflower, Coneflower with nectar production (0.3-1.1 μL)
- **Pollinators**: Honeybee, Bumblebee, Carpenter Bee with physical characteristics
- **Activity**: Visit counts and pollinator measurements

## Research Questions
The dashboard answers three key questions:

1. **What is the body mass and wing span distribution of each pollinator species observed?**
   - Honeybees: Smallest (0.08-0.13g, 15-19mm)
   - Bumblebees: Medium (0.26-0.31g, 24-28mm)
   - Carpenter Bees: Largest (0.42-0.49g, 35-39mm)

2. **What is the ideal weather for pollinating?**
   - Sunny conditions with 25-35°C temperature
   - 30-50% humidity
   - Wind speeds below 6 km/h

3. **Which flower has the most nectar production?**
   - Sunflowers: 0.95 μL average (highest)
   - Coneflowers: 0.75 μL average
   - Lavender: 0.65 μL average (lowest)

## Technologies Used
- **Observable Plot**: For interactive data visualizations
- **D3.js**: For data manipulation and statistical calculations
- **Markdown**: For documentation and narrative

## How to View
1. Open `index.md` in Observable or any Markdown viewer that supports Observable Plot
2. The dashboard will automatically load the CSV data and generate interactive visualizations
3. Each section addresses one of the three research questions with multiple chart types

## Key Insights
- Clear size hierarchy exists among the three bee species
- Weather conditions significantly impact pollinator activity
- Nectar production correlates with pollinator visit frequency
- Optimal conditions can be identified for maximum pollination efficiency

## Deployment
This project is designed to be deployed on GitHub Pages or Observable for easy sharing and collaboration.
