# Workspace Organization Guide

## For All Students - Quick Reference

### What is This?
A complete guide to organizing your MindforgeAI Internship workspace for productivity, collaboration, and success.

---

## Quick Start (5 Minutes)

### Step 1: Run Setup Script (Recommended)
**PowerShell Command:**
```powershell
# Create folders automatically
$studentId = "Kusumanjali Kenchigundi"
$studentName = "YOUR_NAME_HERE"
$root = "e:\MindforgeAI Internship 2026 - $studentId - $studentName"
New-Item -ItemType Directory -Path $root -Force | Out-Null

$folders = @(
    "01_Daily_Diary",
    "02_Daily_Tasks",
    "03_Assignments_Colab",
    "04_Module_Assessments_Answer_Sheets",
    "05_Project_Abstract_Midterm_Final",
    "06_Research_Papers",
    "07_Certificates_Profile_Resume",
    "08_Final_Report_Blackbook",
    "09_Projects_Work",
    "10_Git_Repository",
    "11_Code_Practice",
    "12_Learning_Resources",
    "Notes",
    "Resources"
)

$folders | ForEach-Object {
    New-Item -ItemType Directory -Path "$root\$_" -Force | Out-Null
}

Write-Host "✓ Setup complete! Location: $root"
```

### Step 2: Verify Structure
Open File Explorer and navigate to your folder. You should see 14 folders.

### Step 3: Refer to Documentation
- **STUDENT_SETUP_GUIDE.md** - Detailed guide
- **GIT_BEST_PRACTICES.md** - Git reference
- **README.md** in 10_Git_Repository - Git quick start

---

## Folder Purposes at a Glance

### Module Folders (Official Deliverables)

| Folder | Purpose | File Type | Due |
|--------|---------|-----------|-----|
| 01_Daily_Diary | Daily reflections & logs | .md, .txt | Daily |
| 02_Daily_Tasks | Task tracking & checklist | .md, .txt | Daily |
| 03_Assignments_Colab | Colab notebooks & code | .ipynb | Weekly |
| 04_Module_Assessments_Answer_Sheets | Quiz answers & assessments | .pdf, .doc | Monthly |
| 05_Project_Abstract_Midterm_Final | Project reports | .pdf, .doc | Midterm + Final |
| 06_Research_Papers | Research submissions | .pdf | As assigned |
| 07_Certificates_Profile_Resume | Credentials | .pdf | As earned |
| 08_Final_Report_Blackbook | Final comprehensive report | .pdf | End of semester |

### Work Folders (Personal Organization)

| Folder | Purpose | What Goes Here |
|--------|---------|----------------|
| 09_Projects_Work | Active project files | Code, designs, prototypes |
| 10_Git_Repository | Version control | Git repositories |
| 11_Code_Practice | Coding exercises | Practice code, algorithms |
| 12_Learning_Resources | Learning materials | Tutorials, notes, guides |
| Notes | Personal notes | Study notes, reflections |
| Resources | Reference materials | PDFs, guides, documentation |

---

## Daily Workflow

### Morning (Start of Day)
```
1. Open 01_Daily_Diary
2. Log date and objectives
3. Check 02_Daily_Tasks
4. Plan your work
```

### During Work
```
1. Complete assignments in appropriate folder
2. Make Git commits in 10_Git_Repository
3. Update 02_Daily_Tasks progress
4. Save code in 11_Code_Practice
```

### Evening (End of Day)
```
1. Update 01_Daily_Diary with learnings
2. Commit remaining work to Git
3. Review tomorrow's tasks in 02_Daily_Tasks
4. Organize files if needed
```

---

## File Organization Tips

### ✓ DO

- ✓ Create dated subfolders: `01_Daily_Diary/2026-06-24_Monday`
- ✓ Use clear naming: `Assignment_03_Solution.py`
- ✓ Keep Resources for PDFs only
- ✓ Use Notes for study materials
- ✓ Commit to Git daily
- ✓ Archive old work monthly

### ✗ DON'T

- ✗ Leave files on Desktop
- ✗ Save random files in module folders
- ✗ Mix notes with deliverables
- ✗ Forget to commit changes
- ✗ Skip organizing files

---

## Git Quick Reference

### First Time Setup
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Daily Git Commands
```bash
# Navigate to project
cd e:\MindforgeAI Internship 2026 - YOUR_ID - YOUR_NAME\10_Git_Repository\01_Main_Projects\source\your-project

# Pull latest
git pull origin main

# Create branch for your work
git checkout -b feature/your-feature

# Make changes, then commit
git add .
git commit -m "Clear description of changes"

# Push to remote
git push origin feature/your-feature

# Create Pull Request on GitHub
```

### Important Git Branches
- `main` - Production-ready code
- `develop` - Development branch
- `feature/*` - Your feature branches

---

## Troubleshooting

### Folder Already Exists?
```powershell
# Rename existing folder
Rename-Item "e:\MindforgeAI Internship 2026 - 2026CS020 - Trupti Waychal" `
            "e:\MindforgeAI Internship 2026 - 2026CS020 - Trupti Waychal_OLD"

# Then run setup script with new ID or name
```

### Permission Denied?
```powershell
# Run PowerShell as Administrator
# Right-click → Run as Administrator
```

### Git Not Working?
```bash
# Check if installed
git --version

# If not installed, download from https://git-scm.com/

# Configure if needed
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

### Path Too Long Error?
1. Enable long paths: Settings → System → About → Advanced system settings
2. Or move files to shorter path

---

## Important Files to Keep

### Essential Documents
- [ ] STUDENT_SETUP_GUIDE.md - Complete setup guide
- [ ] GIT_BEST_PRACTICES.md - Git reference
- [ ] CHAT_LOG.md - Setup documentation
- [ ] README.md (in 10_Git_Repository) - Git quick start

### Where They Are
```
Your-Internship-Folder\
├── STUDENT_SETUP_GUIDE.md
├── CHAT_LOG.md
└── 10_Git_Repository\
    ├── README.md
    └── GIT_BEST_PRACTICES.md
```

---

## Progress Tracking

### Weekly Review
- [ ] Check completed tasks in 02_Daily_Tasks
- [ ] Archive completed assignments
- [ ] Review learnings in Notes
- [ ] Plan next week

### Monthly Review
- [ ] Consolidate monthly progress
- [ ] Update 05_Project_Abstract_Midterm_Final
- [ ] Clean up and organize files
- [ ] Backup important work

### Semester End
- [ ] Review all work in module folders
- [ ] Prepare 08_Final_Report_Blackbook
- [ ] Collect certificates in 07_Certificates_Profile_Resume
- [ ] Archive everything

---

## Resources

### Files Included
- Algorithmic Thinking Orientation Experience - Google Gemini.pdf
- Git & GitHub Master Guide - MindForgeAI.pdf

**Location:** Resources/ folder

### External Resources
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Markdown Guide](https://www.markdownguide.org/)

---

## Success Tips

1. **Start organized** - Set up immediately
2. **Be consistent** - Daily logging is key
3. **Commit regularly** - Small, frequent commits
4. **Keep notes** - Document everything
5. **Review often** - Weekly progress review
6. **Ask for help** - Use troubleshooting guides
7. **Stay backed up** - Use cloud storage too
8. **Follow guidelines** - Use folder structure as designed

---

## Common Questions

**Q: Should I use Google Drive or local storage?**  
A: Use local storage for version control (Git). Optionally back up to cloud.

**Q: What if I finish a project early?**  
A: Move it to archive subfolder, start next project in same location.

**Q: How often should I commit?**  
A: At least once daily, preferably after each feature or fix.

**Q: Can I use a different folder structure?**  
A: Not recommended - coordination with team relies on consistency.

**Q: What if I make a mistake?**  
A: Refer to troubleshooting guides or contact program mentors.

---

## Final Checklist

Before starting internship:
- [ ] Folder structure created
- [ ] PDFs moved to Resources/
- [ ] Git configured with your name/email
- [ ] SSH key generated (optional but recommended)
- [ ] First daily log created
- [ ] First commit made to Git

You're ready to start!

---

**Version:** 1.0  
**Last Updated:** June 24, 2026  
**For:** MindforgeAI Internship Program
