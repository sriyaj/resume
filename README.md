# Sriya Jayakumar — Resume & Cover Letter

HTML-based resume and cover letter system. Edit content in Markdown, sync to HTML, export to PDF.

---

## Files

| File | Purpose |
|---|---|
| `sriya_jayakumar_resume_general.html` | Styled resume template |
| `sriya_jayakumar_resume_ibm.html` | IBM-tailored resume |
| `sriya_jayakumar_resume_ibm.md` | Editable content source (edit this) |
| `sriya_jayakumar_coverletter_ibm.html` | IBM cover letter |
| `sriya_jayakumar_resume_general.pdf` | Latest exported PDF |

---

## Requirements

| Software | Purpose | Download |
|---|---|---|
| **Google Chrome** | PDF generation | [chrome.com](https://www.google.com/chrome) |
| **VS Code** | Edit files | [code.visualstudio.com](https://code.visualstudio.com) |
| **GitHub Copilot** (optional) | Sync MD → HTML automatically | VS Code extension |

No other dependencies. Fonts load from Google Fonts — internet connection required for preview and PDF export.

---

## Workflow

### 1. Edit content
Open `sriya_jayakumar_resume_ibm.md` in any text editor and make your changes.

### 2. Sync to HTML
Open the file in VS Code with GitHub Copilot and prompt:

> *"I have updated the .md file. Update the HTML to match exactly as it is now."*

Copilot will apply all changes from the `.md` into the `.html`.

### 3. Export to PDF

**macOS** — run in Terminal:
```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless=new \
  --no-sandbox \
  --print-to-pdf="/path/to/sriya_jayakumar_resume_general.pdf" \
  --print-to-pdf-no-header \
  --no-pdf-header-footer \
  "file:///path/to/sriya_jayakumar_resume_general.html"
```

**Windows** — run in Command Prompt:
```bat
"C:\Program Files\Google\Chrome\Application\chrome.exe" ^
  --headless=new --no-sandbox ^
  --print-to-pdf="resume.pdf" ^
  --print-to-pdf-no-header --no-pdf-header-footer ^
  "file:///C:/path/to/sriya_jayakumar_resume_general.html"
```

### 4. Preview without exporting
Open the `.html` file directly in Chrome. What you see is what the PDF will look like.

---

## Creating a tailored version for a new job

1. Add the job description as a `.txt` file in this folder
2. Open it in VS Code with GitHub Copilot and prompt:

> *"Tailor my resume and create a cover letter based on this job description and my resume."*

Copilot will generate:
- `sriya_jayakumar_resume_<company>.html`
- `sriya_jayakumar_resume_<company>.md`
- `sriya_jayakumar_coverletter_<company>.html`

---

## Design

- Font: [Tenor Sans](https://fonts.google.com/specimen/Tenor+Sans) via Google Fonts
- Accent colour: `#B85C72`
- Page size: A4
