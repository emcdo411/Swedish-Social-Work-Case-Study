![image](https://github.com/user-attachments/assets/8085030a-e820-4b93-9da3-74a8dd22a6c8)


# Swedish-Social-Work-Case-Study

This repository contains a case study on the recent changes in Swedish social work, focusing on the new Social Services Act (Socialtjänstlagen) introduced in 2025. The study explores how social work practices are shifting to be more preventive, accessible, and knowledge-based, with a specific example of placing social workers in hospital emergency rooms. It includes detailed charts analyzing the changes and their implications, plus Python and R scripts to visualize public opinions on social work in Sweden.

## Motivation
I created this case study to support my girlfriend, a social worker in Sweden, who shared insights from a recent agency meeting about upcoming changes in the field. Her mention of social workers working more unobtrusively, being knowledge-based, and increasing accessibility (e.g., in emergency rooms) inspired me to research and document these developments. This study aims to provide a comprehensive overview for social workers, policymakers, and anyone interested in Sweden’s evolving social services landscape.

## Case Study Overview

### Introduction
Sweden’s new Social Services Act, the most significant reform in nearly 50 years, aims to modernize social work by making it more preventive, accessible, and knowledge-based. This case study examines these changes, their implications for social workers, and the potential impact on public perception.

### Background
Social work in Sweden faces challenges like high workloads, time constraints, and public mistrust due to disinformation campaigns since 2021. The new act seeks to address these issues by rebuilding trust and integrating social workers into community settings.

### Chart 1: Main Focus Points of Social Work in Sweden – Current Practices vs. New Social Services Act

| **Aspect**                | **Current Practices**                                                                 | **New Social Services Act**                                                                 | **Pros**                                                                 | **Cons**                                                                 | **Why It Matters**                                                                 |
|---------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| **Approach to Intervention** | Reactive: Social workers often intervene after issues escalate (e.g., child welfare cases). | Preventive: Emphasis on early intervention to address issues before they worsen.            | Reduces long-term costs and trauma by addressing issues early.           | Requires more resources for early detection and training.                | Early intervention can improve outcomes for vulnerable populations, aligning with Sweden’s welfare goals. |
| **Accessibility**         | Limited: Social workers are primarily office-based, requiring appointments or referrals. | Enhanced: Social workers in community settings (e.g., ERs, schools) for immediate support.  | Increases access for those in crisis, like in ERs, reducing barriers.    | High-pressure environments like ERs may strain social workers.           | Accessibility ensures timely support, reducing the risk of escalation in crises.   |
| **Knowledge-Based Practice** | Mixed: Some use evidence-based practices (EBP), but barriers like time (78% of social workers cite lack of time) hinder adoption. | Mandated: Strong focus on EBP, with potential for more training and resources.              | Improves decision-making with evidence, enhancing service quality.       | May require significant retraining; time constraints persist.            | Knowledge-based work ensures interventions are effective and trustworthy.         |
| **Work Environment**      | High workload: Primary healthcare studies show time pressure and poor job control.    | Unclear: Aims to improve conditions, but specifics on workload reduction are lacking.       | Potential for better support systems if resources are allocated.         | Risk of increased workload in new settings like ERs without support.     | A sustainable work environment is crucial for social workers to provide quality care. |

### Chart 2: Public Opinion on Social Work in Sweden and Impacts of the New Social Services Act

| **Aspect**                | **Public’s Current Opinion**                                                                 | **Potential Impacts of New Social Services Act**                                            | **Pros**                                                                 | **Cons**                                                                 | **Why It Matters**                                                                 |
|---------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| **Trust in Social Services** | Mixed: Disinformation since 2021 (e.g., false claims of targeting Muslim children) has eroded trust, leading to threats against social workers. | Aims to rebuild trust through transparency, accessibility, and less invasive interventions. | More community presence (e.g., in ERs) can foster trust through visibility. | Overcoming disinformation requires long-term effort and communication.   | Trust is essential for social workers to effectively support communities without resistance. |
| **Perception of Accessibility** | Limited: Many feel social services are hard to access, requiring formal processes.    | Increased presence in settings like ERs and schools makes services more approachable.       | Reduces stigma and barriers, encouraging people to seek help early.      | Public may initially be skeptical of new settings without awareness campaigns. | Accessibility ensures vulnerable populations receive timely support, reducing disparities. |
| **Effectiveness of Interventions** | Varied: Some view interventions as too invasive, especially in child welfare cases.   | Focus on unobtrusive, preventive work may reduce perceptions of overreach.                 | Less invasive approaches can improve public perception and cooperation.  | Preventive work may be less visible, leading to underappreciation of efforts. | Effective, unobtrusive interventions align with Sweden’s goal of a supportive welfare state. |

### Case Example: Social Workers in Emergency Rooms
The new act’s emphasis on accessibility includes placing social workers in hospital emergency rooms. In Sweden, hospitals like Swedish Edmonds already employ social workers in ERs to handle mental health evaluations, community referrals, and support for issues like substance abuse. This aligns with the act’s goals but requires addressing challenges like workload and training to ensure social workers can thrive in these settings.

### Visualizing Public Opinions with Python
To complement this case study, I’ve created scripts to visualize how the Swedish public views the social work system over the last five years (2020–2025). The original graphs focus on Swedish nationals and immigrants, with simulated data based on trends like disinformation campaigns and integration challenges.

#### Suggested Columns for the Data
- **Year:** 2020 to 2025, to track changes over time.
- **Trust_Level:** A percentage (0–100%) representing trust in the social work system.
- **Satisfaction_Score:** A score (0–10) representing overall satisfaction with social services.
- **Accessibility_Rating:** A score (0–10) reflecting perceived accessibility of social services.

#### Python Script 1: Swedish Nationals’ Views on the Social Work System
```python
import pandas as pd
import matplotlib.pyplot as plt

# Simulated data for Swedish nationals (2020–2025)
data_nationals = {
    "Year": [2020, 2021, 2022, 2023, 2024, 2025],
    "Trust_Level": [75, 70, 65, 62, 60, 63],  # Declining trust due to disinformation, slight recovery in 2025
    "Satisfaction_Score": [7.8, 7.5, 7.2, 7.0, 6.8, 7.0],  # High but declining, slight uptick in 2025
    "Accessibility_Rating": [7.0, 6.8, 6.5, 6.3, 6.2, 6.5]  # Declining due to perceived strain, slight improvement in 2025
}

# Create a DataFrame
df_nationals = pd.DataFrame(data_nationals)

# Plot the data
plt.figure(figsize=(10, 6))
plt.plot(df_nationals["Year"], df_nationals["Trust_Level"], marker='o', label="Trust Level (%)", color="blue")
plt.plot(df_nationals["Year"], df_nationals["Satisfaction_Score"], marker='o', label="Satisfaction Score (0–10)", color="green")
plt.plot(df_nationals["Year"], df_nationals["Accessibility_Rating"], marker='o', label="Accessibility Rating (0–10)", color="orange")

# Customize the graph
plt.title("Swedish Nationals' Views on the Social Work System (2020–2025)", fontsize=14)
plt.xlabel("Year", fontsize=12)
plt.ylabel("Score", fontsize=12)
plt.legend()
plt.grid(True)
plt.xticks(df_nationals["Year"])
plt.ylim(0, 100)

# Save the plot
plt.savefig("swedish_nationals_social_work_views.png")
plt.show()
```

#### Python Script 2: Swedish Immigrants’ Views on the Social Work System
```python
import pandas as pd
import matplotlib.pyplot as plt

# Simulated data for Swedish immigrants (2020–2025)
data_immigrants = {
    "Year": [2020, 2021, 2022, 2023, 2024, 2025],
    "Trust_Level": [60, 58, 55, 53, 50, 52],  # Lower trust due to integration challenges, slight improvement in 2025
    "Satisfaction_Score": [6.0, 5.8, 5.5, 5.3, 5.0, 5.2],  # Lower satisfaction, slight uptick in 2025
    "Accessibility_Rating": [5.5, 5.3, 5.0, 4.8, 4.5, 4.8]  # Lower due to systemic barriers, slight improvement in 2025
}

# Create a DataFrame
df_immigrants = pd.DataFrame(data_immigrants)

# Plot the data
plt.figure(figsize=(10, 6))
plt.plot(df_immigrants["Year"], df_immigrants["Trust_Level"], marker='o', label="Trust Level (%)", color="blue")
plt.plot(df_immigrants["Year"], df_immigrants["Satisfaction_Score"], marker='o', label="Satisfaction Score (0–10)", color="green")
plt.plot(df_immigrants["Year"], df_immigrants["Accessibility_Rating"], marker='o', label="Accessibility Rating (0–10)", color="orange")

# Customize the graph
plt.title("Swedish Immigrants' Views on the Social Work System (2020–2025)", fontsize=14)
plt.xlabel("Year", fontsize=12)
plt.ylabel("Score", fontsize=12)
plt.legend()
plt.grid(True)
plt.xticks(df_immigrants["Year"])
plt.ylim(0, 100)

# Save the plot
plt.savefig("swedish_immigrants_social_work_views.png")
plt.show()
```

#### New Terrain Map Visualizations
Two additional terrain maps enhance this case study with spatial visualizations of public opinion on Sweden’s social welfare system in 2025:

- **Sweden Terrain Map**: Displays trust levels (nationals vs. immigrants) across major cities (Stockholm, Gothenburg, Malmö, Uppsala) using Python and `plotly` for an interactive 3D view.
- **Gothenburg Terrain Map**: Focuses on trust levels in Gothenburg districts (Hisingen, Centrum, Majorna-Linné) using RStudio and `ggmap` with terrain tiles.

##### Python Script 3: Sweden Terrain Map – Nationals vs. Immigrants
```python
import plotly.graph_objects as go
import pandas as pd

# Simulated data for 2025 trust levels in major cities
data = {
    "City": ["Stockholm", "Gothenburg", "Malmö", "Uppsala"],
    "Latitude": [59.3293, 57.7089, 55.6040, 59.8586],
    "Longitude": [18.0686, 11.9746, 13.0038, 17.6389],
    "Nationals_Trust": [63, 62, 65, 64],
    "Immigrants_Trust": [52, 51, 53, 50]
}
df = pd.DataFrame(data)

# 3D Scatter plot
fig = go.Figure()
fig.add_trace(go.Scatter3d(
    x=df["Longitude"], y=df["Latitude"], z=df["Nationals_Trust"],
    mode="markers+text", name="Nationals Trust (%)",
    marker=dict(size=12, color="blue"), text=df["City"]
))
fig.add_trace(go.Scatter3d(
    x=df["Longitude"], y=df["Latitude"], z=df["Immigrants_Trust"],
    mode="markers+text", name="Immigrants Trust (%)",
    marker=dict(size=12, color="orange"), text=df["City"]
))

# Layout
fig.update_layout(
    title="Sweden: Trust in Social Welfare (2025)",
    scene=dict(
        xaxis_title="Longitude", yaxis_title="Latitude", zaxis_title="Trust (%)",
        xaxis=dict(range=[10, 20]), yaxis=dict(range=[55, 65]), zaxis=dict(range=[0, 100])
    )
)

# Save and show
fig.write_html("sweden_terrain_trust.html")
fig.show()
```

##### R Script: Gothenburg Terrain Map – Public Opinion
```R
# Install required packages if not already installed
if (!require(ggmap)) install.packages("ggmap")
if (!require(ggplot2)) install.packages("ggplot2")
if (!require(dplyr)) install.packages("dplyr")

library(ggmap)
library(ggplot2)
library(dplyr)

# Register Stadia Maps API key (replace with your own if needed)
register_stadiamaps("9c644007-0572-4892-915a-8da356fe40ae")

# Simulated data for Gothenburg districts (Trust_Level in % for 2025)
data <- data.frame(
  District = c("Hisingen", "Centrum", "Majorna-Linné"),
  Latitude = c(57.7333, 57.7089, 57.6910),
  Longitude = c(11.9167, 11.9746, 11.9333),
  Nationals_Trust = c(62, 63, 61),
  Immigrants_Trust = c(51, 52, 50)
)

# Define Gothenburg bounding box
gothenburg_bbox <- c(left = 11.8, bottom = 57.6, right = 12.1, top = 57.8)
gothenburg_terrain <- get_stadiamap(bbox = gothenburg_bbox, maptype = "stamen_terrain", zoom = 12)

# Create terrain map
terrain_map <- ggmap(gothenburg_terrain) +
  geom_point(data = data, aes(x = Longitude, y = Latitude, size = Nationals_Trust, color = "Nationals"), alpha = 0.8) +
  geom_point(data = data, aes(x = Longitude, y = Latitude, size = Immigrants_Trust, color = "Immigrants"), alpha = 0.8) +
  scale_size_continuous(range = c(5, 15), name = "Trust Level (%)") +
  scale_color_manual(values = c("Nationals" = "blue", "Immigrants" = "orange"), name = "Group") +
  geom_text(data = data, aes(x = Longitude, y = Latitude, label = District), vjust = -1.5, size = 4) +
  labs(title = "Gothenburg: Trust in Social Welfare (2025)", x = "Longitude", y = "Latitude") +
  theme_minimal() +
  theme(plot.title = element_text(hjust = 0.5, size = 14))

# Save and display
ggsave("gothenburg_terrain_trust.png", terrain_map, width = 10, height = 8, dpi = 300)
cat("Saved as 'gothenburg_terrain_trust.png'\n")
print(terrain_map)
```

#### Instructions for Running the Scripts
- **Python Scripts**: 
  1. Install Python and libraries: `pip install pandas matplotlib plotly`.
  2. Save as `.py` files (e.g., `swedish_nationals_social_work_views.py`, `sweden_terrain_trust.py`).
  3. Run: `python <filename>.py`.
  4. Outputs: PNG graphs and an HTML terrain map.

- **R Script**:
  1. Install R and RStudio.
  2. Install packages: Run the script’s `install.packages` lines.
  3. Save as `gothenburg_terrain_trust.R`.
  4. Run in RStudio: Set working directory (`setwd()`), then execute.
  5. Output: PNG terrain map.

### Conclusion
The new Social Services Act offers a transformative opportunity for social work in Sweden, but its success depends on addressing systemic challenges like workload and public mistrust. By integrating social workers into community settings and focusing on preventive, knowledge-based practices, Sweden can strengthen its welfare system for the benefit of both social workers and the public.

### References
- Swedish Government on Social Services: [Government.se - Social Services](https://www.government.se)
- Study on Evidence-Based Practice: [PubMed - Evidence-based practice among Swedish medical social workers](https://pubmed.ncbi.nlm.nih.gov)
- Swedish Healthcare System: [Commonwealth Fund - Sweden](https://www.commonwealthfund.org)
- Social Work in ERs: [Social Work Today - Making Caring Connections](https://www.socialworktoday.com)
- Swedish Primary Healthcare: [Human Resources Health - Psychosocial work environment](https://human-resources-health.biomedcentral.com)

### How to Use This Case Study
- **For Social Workers**: Understand upcoming changes and prepare for new roles.
- **For Policymakers**: Consider pros and cons to support social workers during this transition.
- **For the Public**: Learn about the evolving role of social services.

### Next Steps
I plan to share this with my girlfriend and her colleagues to spark discussions and incorporate these insights into my Volvo application, highlighting my understanding of Sweden’s social work landscape.

### Contact
Reach out on LinkedIn to discuss this case study or my relocation journey to Sweden!
```

---

### How to Update on GitHub
1. **Open Repository**: Go to `Swedish-Social-Work-Case-Study` on GitHub.
2. **Edit README**: Click `README.md`, then the “Edit” (pencil) icon.
3. **Replace Content**: Paste the above markdown, replacing the old content.
4. **Add Scripts as Files** (Optional):
   - Click “Add file” > “Create new file.”
   - Add `sweden_terrain_trust.py` and `gothenburg_terrain_trust.R` with their respective code.
5. **Commit**: Use a message like “Added terrain map visualizations for Sweden and Gothenburg” and commit.

---

### Notes
- **Integration**: The new terrain maps are nested under the existing visualization section, maintaining flow.
- **Consistency**: Data aligns with your README’s 2025 trust levels (nationals: ~63%, immigrants: ~52%).
- **Link**: You’ll need to add your GitHub URL (e.g., `https://github.com/yourusername/Swedish-Social-Work-Case-Study`)—share your username if you want it included!

What’s your GitHub username? Any tweaks—like adding satisfaction scores to the maps? This is ready to elevate your project! 😊
