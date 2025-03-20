![image](https://github.com/user-attachments/assets/8085030a-e820-4b93-9da3-74a8dd22a6c8)




### Updated GitHub README (in English)

```markdown
# Swedish-Social-Work-Case-Study

This repository contains a case study on the recent changes in Swedish social work, focusing on the new Social Services Act (Socialtjänstlagen) introduced in 2025. The study explores how social work practices are shifting to be more preventive, accessible, and knowledge-based, with a specific example of placing social workers in hospital emergency rooms. It includes two detailed charts analyzing the changes and their implications for social workers and the public, as well as Python scripts to visualize public opinions on social work in Sweden.

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
To complement this case study, I’ve created two Python scripts that generate graphs showing how the Swedish public views the social work system over the last five years (2020–2025). The first graph focuses on Swedish nationals, and the second on immigrants in Sweden. Since specific survey data was not available, the data was simulated based on trends from available sources, such as disinformation campaigns since 2021 and integration challenges for immigrants.

#### Suggested Columns for the Data
For both graphs, the following columns are used:
- **Year:** 2020 to 2025, to track changes over time.
- **Trust_Level:** A percentage (0–100%) representing trust in the social work system.
- **Satisfaction_Score:** A score (0–10) representing overall satisfaction with social services.
- **Accessibility_Rating:** A score (0–10) reflecting perceived accessibility of social services.

These columns were chosen because they reflect key themes in the new Social Services Act (accessibility, trust) and public perception.

#### Python Script 1: Swedish Nationals’ Views on the Social Work System
This script generates a graph showing Swedish nationals’ trust, satisfaction, and perceived accessibility of the social work system over time.

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
plt.ylim(0, 100)  # Adjust y-axis to accommodate Trust_Level percentage

# Save the plot
plt.savefig("swedish_nationals_social_work_views.png")
plt.show()
```

#### Python Script 2: Swedish Immigrants’ Views on the Social Work System
This script generates a graph showing immigrants’ trust, satisfaction, and perceived accessibility of the social work system over time.

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
plt.ylim(0, 100)  # Adjust y-axis to accommodate Trust_Level percentage

# Save the plot
plt.savefig("swedish_immigrants_social_work_views.png")
plt.show()
```

#### Instructions for Saving and Running the Scripts

##### Saving the Scripts
You should save each script as a separate Python file with a `.py` extension:
1. **Open a Text Editor:** Use a text editor like Notepad (Windows), TextEdit (Mac), or a code editor like VS Code, PyCharm, or Sublime Text.
2. **Save the Files:**
   - For the first script (Swedish nationals), copy the code and paste it into your text editor. Save it as `swedish_nationals_social_work_views.py`.
   - For the second script (Swedish immigrants), copy the code and paste it into a new file in your text editor. Save it as `swedish_immigrants_social_work_views.py`.
   - When saving, ensure the file extension is `.py` (e.g., select “All Files” in Notepad and manually type the `.py` extension).

##### Running the Scripts
1. **Install Python:** Ensure Python is installed on your computer (version 3.6 or later). You can download it from [python.org](https://www.python.org/downloads/).
2. **Install Required Libraries:** Open a terminal or command prompt and install the required libraries:
   ```
   pip install pandas matplotlib
   ```
3. **Run the Scripts:**
   - Open a terminal or command prompt.
   - Navigate to the directory where you saved the files (e.g., `cd C:\Users\YourUsername\Documents`).
   - Run each script:
     ```
     python swedish_nationals_social_work_views.py
     ```
     ```
     python swedish_immigrants_social_work_views.py
     ```
4. **View the Output:** Each script will generate a graph and save it as a PNG file (`swedish_nationals_social_work_views.png` and `swedish_immigrants_social_work_views.png`) in the same directory. The graphs will also display on your screen.

### Conclusion
The new Social Services Act offers a transformative opportunity for social work in Sweden, but its success depends on addressing systemic challenges like workload and public mistrust. By integrating social workers into community settings and focusing on preventive, knowledge-based practices, Sweden can strengthen its welfare system for the benefit of both social workers and the public.

## References
- Swedish Government on Social Services: [Government.se - Social Services](https://www.government.se)
- Study on Evidence-Based Practice Among Swedish Medical Social Workers: [PubMed - Evidence-based practice among Swedish medical social workers](https://pubmed.ncbi.nlm.nih.gov)
- Swedish Healthcare System Overview: [Commonwealth Fund - Sweden](https://www.commonwealthfund.org)
- Social Work in Emergency Departments: [Social Work Today - Making Caring Connections](https://www.socialworktoday.com)
- Swedish Primary Healthcare Work Environment: [Human Resources Health - Psychosocial work environment in Swedish primary healthcare](https://human-resources-health.biomedcentral.com)

## How to Use This Case Study
- **For Social Workers:** Use this study to understand the upcoming changes and prepare for new roles in settings like emergency rooms.
- **For Policymakers:** Consider the pros and cons to ensure adequate support for social workers during this transition.
- **For the Public:** Learn about the evolving role of social services and how they aim to better support communities.

## Next Steps
I plan to share this case study with my girlfriend and her colleagues to spark discussions on how to navigate these changes. I also aim to incorporate these insights into my Volvo application, showing my understanding of Sweden’s social work landscape as part of my relocation journey.

## Contact
Feel free to reach out to me on [LinkedIn](https://www.linkedin.com/in/yourusername) to discuss this case study or my relocation journey to Sweden!
```

---

### How to Update the README on GitHub
1. **Open the Repository:** Go to your `Swedish-Social-Work-Case-Study` repository on GitHub.
2. **Edit the README:** Click on `README.md` and select the “Edit” (pencil) icon.
3. **Replace the Content:** Delete the existing content and paste the updated README content above.
4. **Replace Placeholders:** Replace `yourusername` in the LinkedIn link with your actual LinkedIn profile URL (e.g., `https://www.linkedin.com/in/johndoe`).
5. **Commit Changes:** Add a commit message like “Updated README to English and added Python scripts for visualizing public opinions” and click “Commit changes.”
6. **Optional – Add the Scripts as Files:** If you want to include the Python scripts as separate files in the repository:
   - Click “Add file” > “Create new file.”
   - Name the first file `swedish_nationals_social_work_views.py` and paste the first script.
   - Name the second file `swedish_immigrants_social_work_views.py` and paste the second script.
   - Commit each file to the repository.

---

### Why This Update Works
- **Language Consistency:** The entire README is now in English, making it accessible to a broader audience while aligning with your LinkedIn post.
- **Tech Integration:** The new section adds a tech element with Python scripts, showcasing your coding skills and enhancing the case study with visual data.
- **Clear Instructions:** The instructions for saving and running the scripts are detailed, ensuring anyone can replicate the graphs.
- **Seamless Fit:** The new section integrates naturally into the existing structure, complementing the case study’s focus on public perception.

---

### Next Steps
- **Share with Your Girlfriend:** Let her know you’ve updated the repository with the graphs, e.g., “Hey älskling, I added some cool Python graphs to the case study showing public views on social work! Check it out: [link] 💕”
- **Enhance the Graphs:** If you find real survey data, you can update the scripts with actual values.
- **Use in Volvo Application:** Highlight your Python skills and understanding of Swedish social work in your application to Volvo.

Would you like to draft a message to share this update with your girlfriend, or perhaps prepare a section for your Volvo application using these additions? 😊 Let me know!
