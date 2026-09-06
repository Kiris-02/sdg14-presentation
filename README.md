# SDG 14: Life Below Water — 15-Minute 6-Speaker Presentation
### In-Depth Analysis of Targets 14.1, 14.2, and 14.3 using Slidev

This repository contains a presentation slide deck built with [Slidev](https://sli.dev/) and a companion 6-speaker word-for-word script document, designed for an exact 15-minute group presentation.

---

## 🎯 Topic & Analytical Framework

Each target is analyzed through a **4-Question Analytical Grid**:
1. **Targets**: What does each target aim to achieve? (Aims, scope, milestones)
2. **Indicators**: What official UN indicators benchmark progress?
3. **Measurement Methods**: How are these indicators measured? (Satellite remote sensing, autonomous sensors, ocean chemistry)
4. **Institutions & Governance**: What custodian agencies, treaties, and governance mechanisms regulate and monitor compliance?

---

## ⏱️ 6-Speaker Presentation Roster & Time Budget

Total Presentation Duration: **15:00 Minutes** (2:30 per speaker):

| Speaker | Time Window | Section Title | Analytical Focus |
|---|---|---|---|
| **Speaker 1** | `0:00 - 2:30` | **Introduction & Planetary Context** | Ocean life support (oxygen, heat, livelihoods), 4-question methodology roadmap |
| **Speaker 2** | `2:30 - 5:00` | **Target 14.1: Marine Pollution** | Q1 (Aim: nutrients & plastics), Q2 (14.1.1a/b), Q3 (Satellite Chl-a, manta trawls), Q4 (UNEP, MARPOL, Global Plastics Treaty) |
| **Speaker 3** | `5:00 - 7:30` | **Target 14.2: Marine Ecosystems** | Q1 (Aim: resilience & restoration), Q2 (14.2.1: MSP & ICZM), Q3 (Satellite biome mapping, MSP scorecards), Q4 (UNEP, IOC-UNESCO, CBD 30x30) |
| **Speaker 4** | `7:30 - 10:00` | **Target 14.3: Ocean Acidification** | Q1 (Aim: carbon chemistry), Q2 (14.3.1: pH & carbonate pair), Q3 (Spectrophotometry, BGC-Argo floats), Q4 (IOC-UNESCO, GOA-ON, IAEA OA-ICC) |
| **Speaker 5** | `10:00 - 12:30` | **Systemic Synthesis & Governance Gaps** | Cross-target ecological feedback loops, UNCLOS high-seas fragmentation, sensor inequality, chronic SDG 14 financing gap |
| **Speaker 6** | `12:30 - 15:00` | **Strategic Levers & Group Conclusion** | Binding treaties (Plastics Treaty & BBNJ), Blue finance, 4-Question Master Synthesis Matrix, Group closing & Q&A |

> 📜 **Complete Script File:** See [`speaker_scripts.md`](./speaker_scripts.md) for full word-for-word spoken texts, timing cues, slide transition triggers, and speaking notes.

---

## 🚀 How to Share Online via GitHub Pages (Zero-Setup Deployment)

This repository includes a pre-configured GitHub Actions workflow at [`.github/workflows/deploy.yml`](./.github/workflows/deploy.yml). Pushing this project to GitHub automatically builds and hosts your interactive presentation on the web!

### Step 1: Initialize Git and Push to Your GitHub Repository
Run these commands in PowerShell or Git Bash from this directory:

```bash
git init
git add .
git commit -m "feat: complete 15-minute 6-speaker SDG 14 presentation and scripts"
git branch -M main

# Replace <YOUR_USERNAME> and <YOUR_REPO_NAME> with your GitHub details:
git remote add origin https://github.com/<YOUR_USERNAME>/<YOUR_REPO_NAME>.git
git push -u origin main
```

### Step 2: Enable GitHub Pages in Repository Settings
1. Open your repository on GitHub in a web browser.
2. Navigate to **Settings** > **Pages** (on the left sidebar).
3. Under **Build and deployment** > **Source**, select **GitHub Actions**.
4. The workflow will automatically run and publish your slides at:
   ```
   https://<YOUR_USERNAME>.github.io/<YOUR_REPO_NAME>/
   ```

Anyone can open this link to view your slides interactively, navigate with arrow keys, and access presenter mode!

---

## 💻 Running Locally (Optional)

If you have or want to install Node.js locally:

1. **Install Node.js** (if not already installed):
   ```powershell
   winget install OpenJS.NodeJS.LTS
   ```
   *(Restart your terminal after installation)*

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Start the local presentation server**:
   ```bash
   npm run dev
   ```
   Open `http://localhost:3030` in your browser.

4. **Presenter View**:
   - Access `http://localhost:3030/presenter` for a synchronized presenter dashboard displaying notes, speaker timers, and upcoming slide previews.

---

## 📂 Repository File Structure

```
sdg14-presentation/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Pages CI/CD workflow
├── components/
│   ├── SpeakerBadge.vue        # Visual indicator for active speaker & time slot
│   └── TargetCard.vue          # Modular card for the 4-question breakdown
├── styles/
│   └── index.css               # Ocean-inspired styling and glassmorphism cards
├── slides.md                   # Complete Slidev presentation deck with speaker notes
├── speaker_scripts.md          # Word-for-word 6-speaker presentation scripts
├── package.json                # Slidev scripts and dependencies
├── .gitignore                  # Git exclusions
└── README.md                   # Documentation and deployment instructions
```
