# SmartCRM


# Simulated CRM System with AI-Driven Funnel Logic

This project simulates a smart CRM engine that can analyze lead behavior, apply dynamic funnel logic, and assign AI-powered follow-up strategies — all using Python, CSV data, and structured prompts.

---

## Project Goals

- Build a realistic CRM simulation from scratch using synthetic lead data
- Reclassify leads using engagement and intent signals — not static labels
- Assign follow-up tracks using automation and rule-based logic
- Track logic overrides for transparency and adaptability
- Generate clear documentation and AI-powered prompts for future use

---

## Key Files and What They Do

| File | Purpose |
|------|---------|
| `leads_cleaned_1000.csv` | Initial raw dataset of leads |
| `funnel_stages.py` | Applies funnel logic → outputs updated stage labels |
| `leads_with_stages.csv` | Output after stage logic applied |
| `feedback_loops.py` | Tags lead freshness → Active, Dormant, Stale |
| `leads_with_feedback_flags.csv` | Output with engagement health |
| `nurturing_playbooks.py` | Assigns nurture strategies (Convert, Educate, Reactivate) |
| `leads_with_nurture_tracks.csv` | Final enriched CRM output |
| `plot_conversion_funnel.py` | Builds funnel chart (`conversion_funnel.html`) |
| `crm_schema.csv` | Field-by-field CRM structure |
| `crm_fields_notion.md` | Clean Markdown version of the CRM dictionary |
| `genai_prompts.md` | GenAI prompt templates to simulate assistant support |
| `log_logic_override.py` | Tracks changes made to CRM decision logic |
| `logic_overrides.csv` | Auto-generated changelog of override decisions |
| `SmartCRM_Presentation.pdf` | Project Workflow Presentation |


---

## Example Output

You’ll see a final enriched file with columns like:

```plaintext
lead_id | simulated_stage | stage_reason | engagement_health | nurture_track

And an override log like:
2025-07-06 | Ally | Lowered SQL threshold from 80 to 70 | Too many high-intent leads stuck in MQL 
