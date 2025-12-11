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
- `resume_template.html`: Jinja2 template for HTML/PDF rendering.
- `resume.html`: Generated HTML resume.
- `assets/`: Images and logos used in the resume.

## Customization & Templating

Edit `sample_resume.json` to update your resume details. The schema supports:
- Headline, LinkedIn, profile picture
- Experience (single and grouped roles)
- Employment type, company website, company image
- Location, skills, highlights, description
- Certifications (with links)
- Volunteer work

### Template Features
- **Jinja2 macros** for:
  - Formatting experience duration (years/months, hides years if zero)
  - Formatting dates (e.g., `2022-03` → `Mar 2022`)
- **PDF page numbers**: Shown at the bottom center of each page (`Page X of Y`)
- **Extra bottom margin** for clean PDF layout
- **Modern fonts** (Montserrat, Roboto)
- **Responsive layout** for HTML viewing

You can modify `resume_template.html` to change the layout, add/remove fields, or adjust styling. The template uses Jinja2 syntax and supports all fields present in your JSON.

The script will generate both `resume.html` and `resume.pdf` using the template and your data.

To use a different template, update the script or replace `resume_template.html` with your own.
