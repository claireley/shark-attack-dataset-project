# BlueWave Ocean Sports
## Business Context
BlueWave Ocean Sports is an international company specializing in surfing, diving, and ocean sports equipment. The company also develops marine safety products and smart wearable devices designed to improve customer safety during water activities.

As global participation in ocean sports continues to grow globally, consumers are becoming increasingly aware of marine safety risks and environmental hazards. 

BlueWave aims to better understand how activity patterns, regional conditions, and safety perceptions influence customer needs, product demand, and market opportunities.

## Data Wrangling and Cleaning
Extensive pre-processing was involved:
1. Removing unnecessary columns and duplicates
2. Applying uniform column names, letter cases
3. Standardising dates, countries, genders, activity types

## Business Questions and Hypotheses
### Market Expansion
The company plans to expand into additional international coastal markets but lacks sufficient insight into which regions combine strong ocean sports participation with demand for marine safety solutions.

#### Objective
Identify coastal markets with strong growth potential and opportunities for safety-focused product positioning.

#### Question
Which countries have the highest frequency of shark attacks?
#### Approach
1. Focused on identifying countries with highest incidences
2. Visually inspected unique values to identify variations and misspellings of country names
3. Replaced values to match globally accepted standard, focusing on countries which featured in the top 20 as this was most critical to accurately determining the true highest incidence countries.
4. Within the top 5 countries we also looked at the incidence of the top 5 activities.
#### Results
The United States, Australia and South Africa emerged as having the highest incidences. The distribution of each of the top 5 activities was relatively stable across the top 5 countries, this suggests that similar products can be sold in each market.

### Product Development
Current product offerings do not fully address customer concerns about ocean safety.
The company lacks sufficient insight into which activities, locations, and situational risk factors are most associated with increased safety concerns and demand for protective products and wearable technologies.

#### Objective
Develop safety-oriented products that better align with customer activity patterns, safety concerns, and high-exposure ocean environments.
#### Question
Which ocean activities are most associated with shark attacks?
#### Approach
1. Focused on identifying which types of sports result in the highest number of attacks, driven by the hypothesis that board sports are at highest risk.
2. Developed groups of sports based on fundemental similarities. This resulted in grouping board-related sports such as paddleboarding and surfing, swimming activities, which included swimming, snorkeling and bathing, as well as all forms of fishing and diving.
3. Used regular expressions to standardise these into boarding, swimming, fishing and diving. This replaced the existing value.
#### Results
Boarding and swimming were the highest risk activities. The difference was not pronounced. This suggests that demand for protective swimwear and shark-repelling boards may be similar. We also saw a large risk associated with fishing, suggesting a potential new area for product development.

### Marketing Strategy
Marketing campaigns are generating inconsistent results across different regions and customer groups, making it difficult to design effective targeted promotions.
The company also lacks a clear understanding of the demographic and behavioral characteristics of customers involved in high-exposure ocean activities.

#### Objective
Improve marketing effectiveness through data-driven customer and regional analysis.
#### Question
Which customer groups (age and gender) are most frequently involved in shark attacks?
Are shark attacks more frequent during specific time period?
#### Approach
1. Standardised male and female values to M and F.
2. The age category contained many strings alongside numbers. Regex was used to clean the values. This was used to capture leading numbers and replace strings. Before undertaking this step, any values containing the word months were replaced with zero. The first number replaced each entry, this applies to cases with a '?', values with 20s were replaced by 20, values with multiple numbers only retained the first number.
3. Standardised the date formats.
4. Looked at the frequency of attacks by month, then further looked at the country level to determine whether countries in the Northern and Southern hemisphere showed peaks in differing months.
#### Results
1. We found that men were more likely to be attacked than females.
2. The distribution of attacks across ages was conserved, with similar means and standard deviations.
3. More than half of women were attacked while swimming. In contrast, there was much more variation in sports for men, suggesting they may be more likely to participate in diving and fishing.
4. Shark attacks peaked during summer months. For the United States this meant a peak in July, for Australia, the peak was seen in January.

## Conclusions and Insights

Our findings suggest that market expansion should be focused in the USA, Australia and South Africa.

In terms of product development, boards and swimwear are of equal priority. Fishing equipment represents a third area of potential growth.

These results suggest that marketing efforts should be focused on a customer profile of a young male, likely English speaking, across a broad range of ocean sports. Marketing targetting at women should follow a similar age, and should be tailored to swimming.

Shark attacks peak in summer months, marketing spend should be focused during the lead up to summer, and summer itself.

### Team
Claire Leyden

Zhiwen MO

## Presentation link:
https://docs.google.com/presentation/d/1S4-Dp7hUE5fuvDM1wnxrG_bx-HsWqrsjZrHfotUjU5c/edit?usp=sharing








