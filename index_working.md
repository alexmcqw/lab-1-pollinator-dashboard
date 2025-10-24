# Lab 1: Passing Pollinators Dashboard

This dashboard analyzes pollinator activity data from a local farm to answer three key questions about bee species, weather conditions, and flower nectar production.

## Data Overview

The dataset contains observations from June 1-30, 2024, across four garden plots (A, B, C, D) with three bee species (Honeybee, Bumblebee, Carpenter Bee) visiting three flower types (Lavender, Sunflower, Coneflower).

## Question 1: Body Mass and Wing Span Distribution by Pollinator Species

What is the body mass and wing span distribution of each pollinator species observed?

```js
// Complete dashboard in one block
data = [
  {pollinator_species: "Honeybee", avg_body_mass_g: 0.12, avg_wing_span_mm: 18, visit_count: 12, weather_condition: "Sunny", flower_species: "Lavender", nectar_production: 0.8},
  {pollinator_species: "Bumblebee", avg_body_mass_g: 0.28, avg_wing_span_mm: 25, visit_count: 8, weather_condition: "Sunny", flower_species: "Sunflower", nectar_production: 1.1},
  {pollinator_species: "Carpenter Bee", avg_body_mass_g: 0.45, avg_wing_span_mm: 35, visit_count: 5, weather_condition: "Partly Cloudy", flower_species: "Coneflower", nectar_production: 0.9},
  {pollinator_species: "Honeybee", avg_body_mass_g: 0.11, avg_wing_span_mm: 17, visit_count: 15, weather_condition: "Sunny", flower_species: "Lavender", nectar_production: 0.7},
  {pollinator_species: "Bumblebee", avg_body_mass_g: 0.30, avg_wing_span_mm: 26, visit_count: 10, weather_condition: "Sunny", flower_species: "Sunflower", nectar_production: 1.0},
  {pollinator_species: "Carpenter Bee", avg_body_mass_g: 0.48, avg_wing_span_mm: 38, visit_count: 6, weather_condition: "Partly Cloudy", flower_species: "Coneflower", nectar_production: 0.8},
  {pollinator_species: "Honeybee", avg_body_mass_g: 0.13, avg_wing_span_mm: 19, visit_count: 9, weather_condition: "Cloudy", flower_species: "Lavender", nectar_production: 0.6},
  {pollinator_species: "Bumblebee", avg_body_mass_g: 0.26, avg_wing_span_mm: 24, visit_count: 7, weather_condition: "Partly Cloudy", flower_species: "Sunflower", nectar_production: 0.9},
  {pollinator_species: "Honeybee", avg_body_mass_g: 0.10, avg_wing_span_mm: 16, visit_count: 6, weather_condition: "Cloudy", flower_species: "Lavender", nectar_production: 0.5},
  {pollinator_species: "Bumblebee", avg_body_mass_g: 0.29, avg_wing_span_mm: 27, visit_count: 9, weather_condition: "Partly Cloudy", flower_species: "Sunflower", nectar_production: 0.8},
  {pollinator_species: "Carpenter Bee", avg_body_mass_g: 0.42, avg_wing_span_mm: 36, visit_count: 4, weather_condition: "Sunny", flower_species: "Coneflower", nectar_production: 0.7},
  {pollinator_species: "Honeybee", avg_body_mass_g: 0.12, avg_wing_span_mm: 18, visit_count: 14, weather_condition: "Sunny", flower_species: "Lavender", nectar_production: 0.9},
  {pollinator_species: "Bumblebee", avg_body_mass_g: 0.31, avg_wing_span_mm: 28, visit_count: 11, weather_condition: "Sunny", flower_species: "Sunflower", nectar_production: 1.1},
  {pollinator_species: "Carpenter Bee", avg_body_mass_g: 0.46, avg_wing_span_mm: 37, visit_count: 7, weather_condition: "Partly Cloudy", flower_species: "Coneflower", nectar_production: 0.8},
  {pollinator_species: "Honeybee", avg_body_mass_g: 0.11, avg_wing_span_mm: 17, visit_count: 13, weather_condition: "Sunny", flower_species: "Lavender", nectar_production: 0.7},
  {pollinator_species: "Bumblebee", avg_body_mass_g: 0.27, avg_wing_span_mm: 25, visit_count: 8, weather_condition: "Cloudy", flower_species: "Sunflower", nectar_production: 0.9},
  {pollinator_species: "Carpenter Bee", avg_body_mass_g: 0.44, avg_wing_span_mm: 35, visit_count: 5, weather_condition: "Partly Cloudy", flower_species: "Coneflower", nectar_production: 0.6},
  {pollinator_species: "Honeybee", avg_body_mass_g: 0.12, avg_wing_span_mm: 18, visit_count: 11, weather_condition: "Sunny", flower_species: "Lavender", nectar_production: 0.8},
  {pollinator_species: "Bumblebee", avg_body_mass_g: 0.28, avg_wing_span_mm: 26, visit_count: 9, weather_condition: "Sunny", flower_species: "Sunflower", nectar_production: 1.0},
  {pollinator_species: "Carpenter Bee", avg_body_mass_g: 0.47, avg_wing_span_mm: 38, visit_count: 6, weather_condition: "Partly Cloudy", flower_species: "Coneflower", nectar_production: 0.9},
  {pollinator_species: "Honeybee", avg_body_mass_g: 0.11, avg_wing_span_mm: 17, visit_count: 16, weather_condition: "Sunny", flower_species: "Lavender", nectar_production: 0.7},
  {pollinator_species: "Bumblebee", avg_body_mass_g: 0.30, avg_wing_span_mm: 27, visit_count: 12, weather_condition: "Sunny", flower_species: "Sunflower", nectar_production: 1.1},
  {pollinator_species: "Carpenter Bee", avg_body_mass_g: 0.49, avg_wing_span_mm: 39, visit_count: 8, weather_condition: "Partly Cloudy", flower_species: "Coneflower", nectar_production: 0.8},
  {pollinator_species: "Honeybee", avg_body_mass_g: 0.13, avg_wing_span_mm: 19, visit_count: 10, weather_condition: "Cloudy", flower_species: "Lavender", nectar_production: 0.6},
  {pollinator_species: "Bumblebee", avg_body_mass_g: 0.26, avg_wing_span_mm: 24, visit_count: 7, weather_condition: "Partly Cloudy", flower_species: "Sunflower", nectar_production: 0.9}
]

// Body mass distribution by species
Plot.plot({
  title: "Body Mass Distribution by Pollinator Species",
  marks: [
    Plot.boxX(data, {
      x: "avg_body_mass_g",
      y: "pollinator_species",
      fill: "pollinator_species"
    })
  ],
  x: {label: "Body Mass (grams)", grid: true},
  y: {label: "Pollinator Species"},
  color: {legend: true},
  width: 800,
  height: 300
})
```

```js
// Wing span distribution by species
Plot.plot({
  title: "Wing Span Distribution by Pollinator Species",
  marks: [
    Plot.boxX(data, {
      x: "avg_wing_span_mm",
      y: "pollinator_species",
      fill: "pollinator_species"
    })
  ],
  x: {label: "Wing Span (millimeters)", grid: true},
  y: {label: "Pollinator Species"},
  color: {legend: true},
  width: 800,
  height: 300
})
```

**Key Findings:**
- **Honeybees** are the smallest (0.10-0.13g body mass, 16-19mm wingspan)
- **Bumblebees** are medium-sized (0.26-0.31g body mass, 24-28mm wingspan)  
- **Carpenter Bees** are the largest (0.42-0.49g body mass, 35-39mm wingspan)

## Question 2: Ideal Weather Conditions for Pollinating

What is the ideal weather (conditions, temperature, etc) for pollinating?

```js
// Visit count by weather condition
Plot.plot({
  title: "Pollinator Activity by Weather Condition",
  marks: [
    Plot.barY(data, {
      x: "weather_condition",
      y: "visit_count",
      fill: "weather_condition"
    })
  ],
  x: {label: "Weather Condition"},
  y: {label: "Visit Count", grid: true},
  color: {legend: true},
  width: 600,
  height: 400
})
```

**Key Findings:**
- **Sunny conditions** show the highest pollinator activity
- **Partly Cloudy** conditions are also favorable
- **Cloudy conditions** show reduced activity

## Question 3: Flower with Most Nectar Production

Which flower has the most nectar production?

```js
// Nectar production by flower species
Plot.plot({
  title: "Nectar Production by Flower Species",
  marks: [
    Plot.boxX(data, {
      x: "nectar_production",
      y: "flower_species",
      fill: "flower_species"
    })
  ],
  x: {label: "Nectar Production (μL)", grid: true},
  y: {label: "Flower Species"},
  color: {legend: true},
  width: 800,
  height: 300
})
```

**Key Findings:**
- **Sunflowers** produce the most nectar (0.8-1.1 μL)
- **Coneflowers** have moderate nectar production (0.6-0.9 μL)
- **Lavender** produces the least nectar (0.5-0.9 μL)

## Summary Dashboard

```js
// Summary statistics table
html`<table style="border-collapse: collapse; width: 100%; margin: 20px 0;">
  <thead>
    <tr style="background-color: #f2f2f2;">
      <th style="border: 1px solid #ddd; padding: 12px; text-align: left;">Metric</th>
      <th style="border: 1px solid #ddd; padding: 12px; text-align: left;">Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px; font-weight: bold;">Total Observations</td>
      <td style="border: 1px solid #ddd; padding: 12px;">${data.length}</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px; font-weight: bold;">Date Range</td>
      <td style="border: 1px solid #ddd; padding: 12px;">June 1-30, 2024</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px; font-weight: bold;">Pollinator Species</td>
      <td style="border: 1px solid #ddd; padding: 12px;">Honeybee, Bumblebee, Carpenter Bee</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px; font-weight: bold;">Flower Species</td>
      <td style="border: 1px solid #ddd; padding: 12px;">Lavender, Sunflower, Coneflower</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px; font-weight: bold;">Average Visit Count</td>
      <td style="border: 1px solid #ddd; padding: 12px;">${(data.reduce((sum, d) => sum + d.visit_count, 0) / data.length).toFixed(1)}</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px; font-weight: bold;">Total Pollinator Visits</td>
      <td style="border: 1px solid #ddd; padding: 12px;">${data.reduce((sum, d) => sum + d.visit_count, 0)}</td>
    </tr>
  </tbody>
</table>`
```

## Conclusions

1. **Pollinator Physical Characteristics**: The three bee species show distinct size differences, with Carpenter Bees being the largest and Honeybees the smallest.

2. **Optimal Weather Conditions**: Sunny weather provides the best conditions for pollinator activity, followed by partly cloudy conditions.

3. **Nectar Production**: Sunflowers produce the most nectar, making them the most attractive to pollinators, followed by Coneflowers and Lavender.

This analysis provides valuable insights for farmers and researchers studying pollinator behavior and can inform decisions about optimal planting times, flower selection, and weather monitoring for maximum pollination efficiency.
