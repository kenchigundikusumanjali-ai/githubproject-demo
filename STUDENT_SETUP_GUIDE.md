# MindforgeAI Internship 2026 - Workspace Setup Guide

## Student Instructions: Complete Folder Structure Setup

This guide documents the complete process for setting up your MindforgeAI Internship workspace with proper folder organization, resources, and Git repository structure.

---

## Part 1: Initial Folder Structure Setup

### Overview
The internship program uses 8 main module folders plus additional resource and work folders.

### Main Module Folders (01-08)

1. **01_Daily_Diary** - Daily progress logs and reflections
2. **02_Daily_Tasks** - Task tracking and daily assignments
3. **03_Assignments_Colab** - Colab notebooks and collaborative work
4. **04_Module_Assessments_Answer_Sheets** - Assessment answers and evaluations
5. **05_Project_Abstract_Midterm_Final** - Project documentation and reports
6. **06_Research_Papers** - Research paper submissions
7. **07_Certificates_Profile_Resume** - Credentials and professional documents
8. **08_Final_Report_Blackbook** - Final comprehensive report

### Additional Resource & Work Folders

- **Notes/** - Personal notes and study materials
- **Resources/** - PDFs, guides, and learning materials
- **09_Projects_Work/** - Active project files and deliverables
- **10_Git_Repository/** - All Git-related work
- **11_Code_Practice/** - Code practice exercises
- **12_Learning_Resources/** - Additional learning materials

### Creating the Folder Structure

#### Automated Setup (Google Apps Script)
If using Google Drive, use this Google Apps Script:

```javascript
function createMindforgeAIFolders() {
  const studentId = "2026IT009";
  const studentName = "Kusumanjali Kenchigundi";
  const root = DriveApp.createFolder("MindforgeAI Internship 2026 - " + studentId + " - " + studentName);
  [
    "01_Daily_Diary",
    "02_Daily_Tasks",
    "03_Assignments_Colab",
    "04_Module_Assessments_Answer_Sheets",
    "05_Project_Abstract_Midterm_Final",
    "06_Research_Papers",
    "07_Certificates_Profile_Resume",
    "08_Final_Report_Blackbook"
  ].forEach(name => root.createFolder(name));
  Logger.log(root.getUrl());
}
```

#### Manual Setup (Windows PowerShell)
```powershell
# Navigate to your drive
cd e:\

# Create main folder
$rootPath = "e:\MindforgeAI Internship 2026 - [2026IT009] - [Kusumanjali Kenchigundi]"
New-Item -ItemType Directory -Path $rootPath -Force

# Create main module folders
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
    New-Item -ItemType Directory -Path "$rootPath\$_" -Force
}
```

---

## Part 2: Organizing Resources

### Moving Resources to Proper Folders

#### PDF Files
All learning PDFs should be placed in `Resources/`:

```powershell
# Example: Moving a PDF
Move-Item -Path "E:\Algorithmic Thinking Orientation Experience - Google Gemini.pdf" `
          -Destination "E:\MindforgeAI Internship 2026 - 2026IT009- Kusumanjali Kenchigundi\Resources\"
```

#### Current Resources
The following resources are included:
1. **Algorithmic Thinking Orientation Experience - Google Gemini.pdf** - Foundational concepts
2. **Git & GitHub Master Guide - MindForgeAI.pdf** - Version control and Git workflow

### File Organization Best Practices

- **Keep Resources separate from module work** - Resources are reference materials
- **Don't mix Notes with module deliverables** - Notes go in `Notes/` folder
- **Module folders are only for submissions** - Don't store personal notes there
- **Research papers go in 06_Research_Papers** - Only finalized papers

---

## Part 3: Git Repository Structure

### Folder Organization

```
10_Git_Repository/
├── 01_Main_Projects/
│   ├── source/          (Clone main projects here)
│   └── docs/            (Project documentation)
├── 02_Practice_Repos/
│   ├── exercises/       (Git exercises)
│   └── tutorials/       (Tutorial repos)
├── 03_Forked_Repos/     (Forked repositories)
└── 04_Cloned_Resources/ (Reference repositories)
```

### Cloning Repositories

#### Step 1: Navigate to Target Folder
```powershell
cd "E:\MindforgeAI Internship 2026 - 2026IT009 - Kusumanjali Kenchigundi\10_Git_Repository\01_Main_Projects\source"
```

#### Step 2: Clone Repository
```bash
git clone https://github.com/username/repository-name.git
cd repository-name
```

#### Step 3: Set Up Local Configuration
```bash
# Configure Git (if not already done)
git config --global user.name "Kusumanjali Kenchigundi"
git config --global user.email "kenchigundikusumanjali@gamil.com"

# Verify configuration
git config --list
```

### Standard Git Workflow

#### Daily Workflow
```bash
# 1. Pull latest changes
git pull origin main

# 2. Create a feature branch
git checkout -b feature/your-feature-name

# 3. Make changes and commit
git add .
git commit -m "Clear description of changes"

# 4. Push to remote
git push origin feature/your-feature-name

# 5. Create Pull Request on GitHub
```

#### Commit Message Best Practices
```
Format: [TYPE] Brief description

Types:
- feat: New feature
- fix: Bug fix
- docs: Documentation
- style: Code style
- refactor: Code refactoring
- test: Testing
- chore: Maintenance

Example:
feat: Add user authentication module
fix: Resolve login validation bug
docs: Update API documentation
```

---

## Part 4: Daily Workflow Integration

### Daily Routine

1. **Morning Check-in** (01_Daily_Diary)
   - Log learning objectives
   - Plan daily tasks
   
2. **Task Management** (02_Daily_Tasks)
   - Create task checklist
   - Mark completed items
   
3. **Work on Assignments** (03_Assignments_Colab / 09_Projects_Work)
   - Code in practice folder
   - Collaborate in Colab
   
4. **Version Control** (10_Git_Repository)
   - Commit changes regularly
   - Push to remote repository
   
5. **End-of-Day Reflection** (Notes)
   - Document learnings
   - Note challenges and solutions

### Weekly Routine

- Review 02_Daily_Tasks and mark completed work
- Organize and clean up working files
- Prepare assignments for 04_Module_Assessments_Answer_Sheets
- Update documentation in 06_Research_Papers

### Monthly Routine

- Prepare project updates for 05_Project_Abstract_Midterm_Final
- Review and organize certificates in 07_Certificates_Profile_Resume
- Create consolidated progress report

---

## Part 5: Important Guidelines

### ✓ DO
- ✓ Commit changes frequently (daily minimum)
- ✓ Write descriptive commit messages
- ✓ Keep Notes separate from submission folders
- ✓ Back up important work to cloud storage
- ✓ Review Git history before pushing
- ✓ Document your work thoroughly

### ✗ DON'T
- ✗ Mix personal notes with deliverables
- ✗ Push directly to main branch without PR review
- ✗ Commit large binary files to Git
- ✗ Store sensitive credentials in repositories
- ✗ Skip documentation
- ✗ Ignore merge conflicts

---

## Part 6: Troubleshooting

### Git Issues

**Issue: Cannot clone repository**
```powershell
# Solution: Verify you have Git installed
git --version

# If not installed, download from https://git-scm.com/
```

**Issue: Authentication failed**
```powershell
# Solution: Set up Git credentials
git config --global user.name "Kusumanjali Kenchigundi"
git config --global user.email "kenchigundikusumanjali@gamil.com"

# For HTTPS cloning with GitHub, use personal access token
```

**Issue: Merge conflict**
```bash
# 1. Check status
git status

# 2. Edit conflicted files manually
# 3. Stage resolved files
git add .

# 4. Complete merge
git commit -m "Resolve merge conflict"
```

### Folder Access Issues

**Issue: Permission denied**
```powershell
# Run PowerShell as Administrator
# Right-click PowerShell → Run as administrator
```

**Issue: Path too long (Windows)**
```powershell
# Solution: Enable long paths in Windows
# Group Policy Editor (gpedit.msc)
# Computer Configuration > Administrative Templates > System > Filesystem
# Enable "Enable Win32 long paths"
```

---

## Part 7: Resources & References

### Important Documents
- **Git & GitHub Master Guide** - Located in Resources/
- **Algorithmic Thinking Orientation Experience** - Located in Resources/
- This guide - Located in 10_Git_Repository/

### External Resources
- [Git Official Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Pro Git Book](https://git-scm.com/book/en/v2)

### Support
- Refer to PDF guides in Resources/
- Check 11_Learning_Resources/ for additional tutorials
- Consult with program mentors for complex issues

---

## Part 8: Template Files

### Daily Diary Template
Create a new file: `01_Daily_Diary/2026-06-24_Daily_Log.md`
```markdown
# Daily Log - June 24, 2026

## Objectives
- [ ] Objective 1
- [ ] Objective 2

## Tasks Completed
- [x] Task 1
- [x] Task 2

## Challenges Faced
...

## Key Learnings
...

## Tomorrow's Plan
...
```

### Task Template
Create in `02_Daily_Tasks/`:
```markdown
# Task: [Task Name]
**Date:** 2026-06-24
**Status:** In Progress

## Description
...

## Requirements
- [ ] Requirement 1
- [ ] Requirement 2

## Progress
...

## Completion Date: [When completed]
```

---

## Quick Reference

### Folder Purposes
| Folder | Purpose |
|--------|---------|
| 01_Daily_Diary | Personal daily logs |
| 02_Daily_Tasks | Task tracking |
| 03_Assignments_Colab | Colab notebooks |
| 04_Module_Assessments | Assessments |
| 05_Project_Abstract | Project docs |
| 06_Research_Papers | Research papers |
| 07_Certificates | Credentials |
| 08_Final_Report | Final report |
| 09_Projects_Work | Active projects |
| 10_Git_Repository | Version control |
| 11_Code_Practice | Practice code |
| 12_Learning_Resources | Learning materials |
| Notes | Personal notes |
| Resources | PDFs & guides |

---

## Conclusion

This setup provides a professional, organized workspace for your MindforgeAI Internship program. Regular maintenance and adherence to these guidelines will ensure smooth workflow throughout your internship.

**Next Steps:**
1. Create the folder structure following Part 1
2. Move resources to appropriate folders (Part 2)
3. Set up Git repositories (Part 3)
4. Begin daily workflow (Part 4)

---

**Created:** 2026-06-24  
**For:** MindforgeAI Internship Program 5th Semester  
**Applicable to:** All Students
