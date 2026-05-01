# RFE Skills Navigator

An interactive HTML reference for RFE staff covering the skills, concepts, and products used across the team.

## How this works

Content is managed in a spreadsheet and rendered in the HTML. Claude (AI) handles the translation between the two.

- **Content edits** → made in the xlsx on Box (`mel_topics_popup_data_apr_22_2026.xlsx`)
- **HTML output** → `rfe_products_updated.html` in this repo
- **Claude** → reads the xlsx, compares against the HTML, and updates the popupData section

## How to update the HTML

1. Edit the xlsx in Box
2. Clone this repo (one-time): `git clone https://github.com/RFEtraining/RFE-skills-navigator.git`
3. Open Claude Code in the cloned folder
4. Paste in the updated xlsx and say: *"compare the xlsx against the HTML and update it"*
5. Claude reports all differences for your review before making changes
6. After approving, copy the updated HTML from your working folder into the repo folder
7. Push to GitHub:
   ```bash
   git add rfe_products_updated.html
   git commit -m "brief description of what changed"
   git push
   ```

## Version control

Every push is logged in GitHub with a timestamp and commit message. View full history at:
`https://github.com/RFEtraining/RFE-skills-navigator/commits`

## One-time setup (per person)

- Install [Git](https://git-scm.com)
- Install [Claude Code](https://claude.ai/code)
- Get access to the `RFEtraining` GitHub org
- Generate a GitHub Personal Access Token (Settings → Developer settings → Tokens) with `repo` scope — use this as your password on first push
