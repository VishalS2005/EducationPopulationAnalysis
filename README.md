# 📊 Global Education & Population Analysis in R

An R-based exploration of teacher distribution and population growth, with specific focus on the United States and four high-GDP countries. Built using tidyverse pipelines and enriched through animated and exportable data visuals.

---

## 📂 Datasets Used

### 🎓 Education Dataset

- 🔗 Source: [Our World in Data – Global Education](https://ourworldindata.org/global-education)
- 📊 Includes: 
  - Country Name
  - Country Code
  - Teacher counts by level (Pre-Primary, Primary, Secondary, Tertiary)
  - Years: 1970–2014
- ⚠️ Null Values: Especially prevalent in older years and smaller countries

### 🌍 Population Dataset

- 🔗 Source: [Our World in Data – Population Explorer](https://ourworldindata.org/explorers/population-and-demography)
- 📊 Includes:
  - Country Name
  - Country Code
  - Yearly population data from 1950–2021

---

## 📘 Focus Topics

### 🇺🇸 United States

- 📈 **Education Trends**
  - Increase in tertiary-level teachers from 1980 onwards
  - Dip in pre-primary staffing around late 1970s
- 👥 **Population Growth**
  - Steady rise post-1950, crossing 300M around 2006
- 🧮 Metrics created:
  - Teacher-per-capita ratios per year
  - Visualization of education staffing relative to total population

### 💰 Four High-GDP Countries

Analyzed based on World Bank GDP rankings:

| Country       | GDP Rank | Key Education Insights |
|---------------|----------|-------------------------|
| 🇩🇪 Germany     | Top 5    | Strong tertiary presence post-2000 |
| 🇯🇵 Japan       | Top 5    | High primary teacher density |
| 🇺🇸 United States | Top 1    | Already covered separately |
| 🇬🇧 United Kingdom | Top 10   | Notable growth in secondary education staffing |

- 🧮 Created teacher-to-population ratios
- 📊 Compared total teachers per education level, normalized by population
- 🪄 Used `gganimate` to visualize changes over time per country

---

## 🛠️ R Libraries Used

```r
library(tidyverse)
library(janitor)
library(scales)
library(extrafont)
library(gganimate)
library(gifski)
library(knitr)
library(english)
library(png)
```

---

## 🧼 Cleaning & Preparation
- Unified country_code field for joins
- Removed null-heavy records, especially pre-1975
- Tidy structure ensured using pivot_longer(), clean_names(), and mutate()

## 🔗 Joining Datasets
- Merged by country_code and year
- Constructed new feature: teachers_per_10k_people
- Filtered complete years: 1970–2014 for education, 1950–2021 for population

## 📦 Outputs

- 🎞️ Animated plots showing teacher trends by GDP level
- 📈 Time-series of population growth vs teacher availability
- 📊 Summary tables with ranked per-capita staffing
- 🖼 PNG exports for reports or dashboards using png and knitr::kable()

## 🚀 Next Steps
- Integrate GDP data for direct correlation testing
- Add student enrollment stats for measuring system capacity
- Develop shiny dashboard for region/year exploration

# 🧑‍💻 Run Instructions
Make sure to have R ≥ 4.0 and run:

---

## License
GNU GENERAL PUBLIC LICENSE
Version 3, 29 June 2007

---

## Contact
vishalsaran2021@gmail.com
chenyiningchris@gmail.com
