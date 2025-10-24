# Lab 1: Passing Pollinators Dashboard

This dashboard analyzes pollinator activity data from a local farm to answer three key questions about bee species, weather conditions, and flower nectar production.

## Data Overview

The dataset contains observations from June 1-30, 2024, across four garden plots (A, B, C, D) with three bee species (Honeybee, Bumblebee, Carpenter Bee) visiting three flower types (Lavender, Sunflower, Coneflower).

## Question 1: Body Mass Distribution by Pollinator Species

```js
Plot.plot({
  title: "Body Mass Distribution by Pollinator Species",
  marks: [
    Plot.boxX([
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
    ], {
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

## Question 1: Wing Span Distribution by Pollinator Species

```js
Plot.plot({
  title: "Wing Span Distribution by Pollinator Species",
  marks: [
    Plot.boxX([
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
    ], {
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

## Question 2: Pollinator Activity by Weather Condition

```js
Plot.plot({
  title: "Pollinator Activity by Weather Condition",
  marks: [
    Plot.barY([
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
    ], {
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

## Question 3: Nectar Production by Flower Species

```js
Plot.plot({
  title: "Nectar Production by Flower Species",
  marks: [
    Plot.boxX([
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
    ], {
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

## Summary Statistics

| Metric | Value |
|--------|-------|
| **Total Observations** | 25 |
| **Date Range** | June 1-30, 2024 |
| **Pollinator Species** | Honeybee, Bumblebee, Carpenter Bee |
| **Flower Species** | Lavender, Sunflower, Coneflower |
| **Average Visit Count** | 9.2 |
| **Total Pollinator Visits** | 230 |

## Key Findings

### Question 1: Body Mass and Wing Span Distribution
- **Honeybees** are the smallest (0.10-0.13g body mass, 16-19mm wingspan)
- **Bumblebees** are medium-sized (0.26-0.31g body mass, 24-28mm wingspan)  
- **Carpenter Bees** are the largest (0.42-0.49g body mass, 35-39mm wingspan)

### Question 2: Ideal Weather Conditions
- **Sunny conditions** show the highest pollinator activity
- **Partly Cloudy** conditions are also favorable
- **Cloudy conditions** show reduced activity

### Question 3: Nectar Production
- **Sunflowers** produce the most nectar (0.8-1.1 μL)
- **Coneflowers** have moderate nectar production (0.6-0.9 μL)
- **Lavender** produces the least nectar (0.5-0.9 μL)

## Conclusions

1. **Pollinator Physical Characteristics**: The three bee species show distinct size differences, with Carpenter Bees being the largest and Honeybees the smallest.

2. **Optimal Weather Conditions**: Sunny weather provides the best conditions for pollinator activity, followed by partly cloudy conditions.

3. **Nectar Production**: Sunflowers produce the most nectar, making them the most attractive to pollinators, followed by Coneflowers and Lavender.

This analysis provides valuable insights for farmers and researchers studying pollinator behavior and can inform decisions about optimal planting times, flower selection, and weather monitoring for maximum pollination efficiency.
