
# Cover Letter Engine

A minimal, high-signal system to generate tailored cover letters using an LLM (Copilot / ChatGPT) with full control over tone, structure, and relevance.

This repository avoids over-engineered agent frameworks and instead uses a **deterministic prompt-driven workflow** to produce consistent, human-quality cover letters.

---

##  Concept

Instead of generating cover letters from scratch each time, this system:

- Starts from a **polished base template**
- Uses your **resume as the source of truth**
- Adapts to a **specific job description (JD)**
- Applies **strict rewriting rules** to avoid AI-generated tone

---

## 📁 Repository Structure

```

/cover-letter-engine
├── base_letter.md   # Style + structure reference (3-paragraph template)
├── resume.md        # Full resume + prioritized skills snapshot
├── jd.md            # Job description (replace for each application)
├── prompt.md        # Core logic (rules + adaptation strategy)
├── output_cover_letter.md        # Final generated cover letter
└── README.md        # Documentation

`````

---

## ⚙️ How It Works

The LLM is instructed to:

1. Read all input files
2. Understand the job requirements from `jd.md`
3. Extract relevant experience from `resume.md`
4. Rewrite `base_letter.md` accordingly
5. Apply strict constraints from `prompt.md`
6. Output a **concise, 3-paragraph cover letter**

---

##  How to Use (IDE + Copilot/Claude, Codex,etc)

### Step 1 — Update JD
Paste the job description into:

````md
jd.md
`````

---

### Step 2 — Run the Prompt

Copy and paste this into Copilot / Claude / any LLM:

```
Read prompt.md, base_cover_letter.md, resume.md, and jd.md. 
Generate the cover letter and write it to output_cover_letter.md. 
If something is not relevant, remove it instead of adapting it.
```

---

### Step 3 — Get Output

Check:

```
output_cover_letter.md
```


---

##  Tips for Best Results

* Keep `jd.md` clean (remove noise if needed)
* Do NOT modify `prompt.md` frequently
* Improve `base_cover_letter.md` over time based on outputs
* Ensure `resume.md` is well-structured and updated
