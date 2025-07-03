# SmartCRM Prototype — Simulated Lead Flow with AI-Driven Logic

A Python-based simulation of a smart Customer Relationship Management (CRM) system that thinks, tags, and acts like a real revenue operations (RevOps) engine.

##  Project Summary

This project simulates how a modern CRM might intelligently process leads using:

* CSV pipelines
* Python rule-based scripts
* GenAI prompt design
* Automated funnel visualizations

Rather than just storing contacts, this CRM prototype aims to **simulate decisions**:

* Classifying lead stages based on behavior
* Assigning nurturing strategies
* Flagging engagement signals
* Documenting logic changes

---

##  Pipeline Overview

```
leads_cleaned_1000.csv
    ⬇️
funnel_stages.py                  ➔   leads_with_stages.csv
    ⬇️
feedback_loops.py                 ➔   leads_with_feedback_flags.csv
    ⬇️
nurturing_playbooks.py            ➔   leads_with_nurture_tracks.csv
    ⬇️
plot_conversion_funnel.py         ➔   conversion_funnel.html

log_logic_override.py             ➔   logic_overrides.csv
crm_schema.csv, crm_fields_notion.md  ➔   Field definitions and logic documentation
```

---

##  Core Files & Their Roles

| File                        | Purpose                                                |
| --------------------------- | ------------------------------------------------------ |
| `leads_cleaned_1000.csv`    | Initial synthetic dataset (1000 fake leads)            |
| `funnel_stages.py`          | Reclassifies leads into Lead/MQL/SQL/Customer          |
| `feedback_loops.py`         | Tags leads as Active, Stale, or Dormant                |
| `nurturing_playbooks.py`    | Assigns follow-up tracks like Education, Reactivation  |
| `plot_conversion_funnel.py` | Generates an HTML funnel visualization                 |
| `log_logic_override.py`     | Logs manual overrides with timestamps                  |
| `logic_overrides.csv`       | Auto-generated logic change tracker                    |
| `crm_schema.csv`            | CRM field schema for data types, automation            |
| `crm_fields_notion.md`      | Notion-style version of CRM schema (human readable)    |
| `genai_prompts.md`          | GenAI templates to summarize pain points & send emails |
| `conversion_funnel.html`    | Interactive funnel chart to visualize stage breakdown  |
| `requirements.txt`          | Python dependencies                                    |

---

##  CRM Field Summary (See `crm_fields_notion.md`)

###  Core Fields

| Field               | Type    | Description              |
| ------------------- | ------- | ------------------------ |
| lead\_id            | ID      | Unique lead record       |
| created\_at         | Date    | Entry point timestamp    |
| funnel\_stage       | Enum    | Lead, MQL, SQL, Customer |
| intent\_score       | Integer | Signal strength (0–100)  |
| last\_engaged       | Date    | Last touchpoint          |
| company\_size       | Enum    | "S: 1-10", etc.          |
| source              | Enum    | Facebook, LinkedIn, etc. |
| engagement\_channel | Enum    | Email, WhatsApp, etc.    |
| sales\_owner        | Text    | Assigned rep             |

###  Automation Fields

| Field              | Purpose                             |
| ------------------ | ----------------------------------- |
| simulated\_stage   | Funnel stage based on logic engine  |
| stage\_reason      | Why that stage was picked           |
| engagement\_health | Dormant, Stale, or Active           |
| nurture\_track     | Reactivation, Education, Conversion |

Ownership transitions:

* Lead → Marketing
* MQL → Marketing Ops
* SQL → SDRs / AEs
* Customer → CSM / Account Managers

---

##  Prompt Engineering (See `genai_prompts.md`)

### Example Prompts

* **Pain Summary:** Convert messy call notes to CRM-ready one-liner
* **Email Generator:** Craft personalized reactivation emails

### Output Sample

```
pain_point_summary: "Perceived product complexity and uncertain fit for current team size."
```

---

##  Sample Output CSVs

| File                            | What It Contains                       |
| ------------------------------- | -------------------------------------- |
| `leads_with_stages.csv`         | Reclassified funnel stages             |
| `leads_with_feedback_flags.csv` | Added engagement health flags          |
| `leads_with_nurture_tracks.csv` | Assigned Education / Conversion tracks |

You can include **screenshot snapshots** of these files in relevant sections of a presentation or notebook.

---

##  What You Can Learn from This

* How to simulate CRM behavior using CSVs + scripts
* How to log changes like a real RevOps team
* How to prompt GenAI for non-salesy outreach
* How logic can be transparent, tweakable, and explainable

---

##  Visualization Output

Open `conversion_funnel.html` in a browser to see:

* Drop-off by stage
* Stage-wise funnel conversion
* Strategy opportunities

---

##  Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

---

##  Folder Structure Recommendation (Optional)

```bash
SmartCRM_Project/
├── data/
│   ├── leads_cleaned_1000.csv
│   ├── leads_with_stages.csv
│   ├── leads_with_feedback_flags.csv
│   ├── leads_with_nurture_tracks.csv
│   ├── logic_overrides.csv
├── scripts/
│   ├── funnel_stages.py
│   ├── feedback_loops.py
│   ├── nurturing_playbooks.py
│   ├── log_logic_override.py
│   ├── plot_conversion_funnel.py
├── docs/
│   ├── crm_fields_notion.md
│   ├── crm_schema.csv
│   ├── genai_prompts.md
│   └── SmartCRM_Presentation.pdf
├── outputs/
│   ├── conversion_funnel.html
├── requirements.txt
├── README.md
```

---

##  Credits

Created by a CRM automation enthusiast to simulate:

> "How would a RevOps assistant powered by GenAI behave?"

This project blends **data clarity**, **human logic**, and **automated insight**. All logic decisions are explainable and tweakable.
