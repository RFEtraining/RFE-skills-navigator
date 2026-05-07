# RFE Skills Navigator

An interactive HTML reference for RFE staff covering the skills, concepts, and products used across the team.

**Live site:** https://rfetraining.github.io/RFE-skills-navigator/wrapper.html

---

## How this works

Content is managed in a spreadsheet and rendered in the HTML. Claude Code (AI) handles the translation between the two.

- **Content edits** → made in the xlsx on Box (`mel_topics_popup_data_apr_22_2026.xlsx`)
- **HTML output** → `rfe_products_updated.html` in this repo
- **Claude Code** → reads the xlsx, compares against the HTML, updates the HTML, and pushes to GitHub

---

## One-time setup (per person)

Do this once before your first update.

### Step 1: Install Git
Go to [git-scm.com/download/win](https://git-scm.com/download/win), download and install. Accept all defaults.

### Step 2: Get GitHub access
Ask a team member to add you to the `RFEtraining` GitHub org. You'll need a free GitHub account at [github.com](https://github.com) if you don't have one.

### Step 3: Create a Personal Access Token
1. Go to github.com → click your profile photo (top right) → **Settings**
2. Scroll to the bottom → **Developer settings**
3. **Personal access tokens** → **Tokens (classic)** → **Generate new token (classic)**
4. Give it a name (e.g. "RFE Navigator"), check the **repo** box, click **Generate token**
5. Copy the token — you only see it once. Save it somewhere safe (e.g. a Notes file)

### Step 4: Clone the repo
Open a terminal (search "Command Prompt" in Start menu) and run:
```
git clone https://github.com/RFEtraining/RFE-skills-navigator.git
```
When prompted for a password, paste your Personal Access Token from Step 3.

This creates a folder called `RFE-skills-navigator` on your computer. You never need to edit files in this folder directly — Claude handles it.

---

## How to update the HTML

Do this any time you've made changes to the xlsx in Box.

1. Edit the xlsx in Box and save
2. Open Claude Code, navigate to your local `RFE-skills-navigator` folder
3. Paste this message (update the Box path to match your username):

> *"Compare the xlsx at `C:\Users\[yourname]\Box\Right-Fit Evidence Unit\5_Planning\Annual planning\2025\1. Strong Team\1.1 Improved Technical Skills\Skill Architecture HTML docs\mel_topics_popup_data_apr_22_2026.xlsx` against the HTML at the same folder's `rfe_products_updated.html`, show me all differences, then update the HTML and push to GitHub."*

4. Claude reports all differences for your review before making any changes
5. Approve the changes and Claude handles the rest — updating the HTML, copying it to the repo folder, committing, and pushing

---

## Version control

Every push is logged in GitHub with a timestamp and commit message. View full history at:
`https://github.com/RFEtraining/RFE-skills-navigator/commits`
