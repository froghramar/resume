# JSON Resume Generator

This project generates a formatted resume from a JSON file, with schema validation.

## Setup Instructions

1. **Clone or download the repository.**

2. **Create and activate a virtual environment:**

   On Windows (bash):
   ```bash
   python -m venv venv
   source venv/Scripts/activate
   ```

3. **Install required packages:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the generator script:**
   ```bash
   python generate_resume.py
   ```

## Files
- `sample_resume.json`: Example resume data.
- `resume_schema.json`: JSON schema for validation.
- `generate_resume.py`: Script to validate and generate resume.

## Customization & Templating

- Edit `sample_resume.json` to update your resume details. The schema supports advanced fields such as headline, LinkedIn, experience location, experience skills, certifications, and volunteer work.
- The resume is rendered using a customizable Jinja2 HTML template (`resume_template.html`).
- You can modify `resume_template.html` to change the layout, add/remove fields, or adjust styling. The template uses Jinja2 syntax and supports all fields present in your JSON.
- The script will generate both `resume.html` and `resume.pdf` using the template and your data.
- To use a different template, update the script or replace `resume_template.html` with your own.
