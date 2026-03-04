# 2400033034_FSAD_Skill_exp-1

## Skill 1: Git Version Control - FSAD Lab Experiment

### Overview
This project demonstrates fundamental Git Version Control concepts including repository initialization, branching, merging, and collaboration workflows.

### Learning Objectives
- Initialize and configure Git repositories
- Create and manage branches
- Perform merge operations
- Use .gitignore for version control best practices
- Understand commit history and logging
- Collaborate using pull requests

### Key Git Commands Demonstrated

#### Repository Setup
```bash
# Initialize a new repository
git init

# Clone an existing repository
git clone <repository-url>

# Configure user information
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

#### Basic Operations
```bash
# Check repository status
git status

# Stage changes
git add <file>
git add .                 # Stage all changes

# Commit changes
git commit -m "Commit message"
git commit -am "Stage and commit tracked files"

# View commit history
git log
git log --oneline         # Condensed log view
git log --graph --all     # Visual branch graph
```

#### Branching and Merging
```bash
# Create a new branch
git branch <branch-name>
git checkout -b <branch-name>    # Create and switch

# List branches
git branch
git branch -a              # List all branches (local and remote)

# Switch branches
git checkout <branch-name>
git switch <branch-name>   # Newer syntax

# Merge branches
git merge <branch-name>

# Delete branch
git branch -d <branch-name>
```

#### Remote Operations
```bash
# View remote repositories
git remote -v

# Add remote
git remote add origin <repository-url>

# Push changes
git push origin <branch-name>
git push -u origin <branch-name>    # Set upstream

# Pull changes
git pull origin <branch-name>

# Fetch updates
git fetch origin
```

#### Undoing Changes
```bash
# Unstage changes
git reset <file>
git reset --hard HEAD     # Discard all changes

# Revert a commit
git revert <commit-hash>

# Amend last commit
git commit --amend
```

### .gitignore Configuration
Example `.gitignore` file for Java projects:
```
# Compiled class files
*.class

# Maven build files
target/
pom.xml.tag
pom.xml.releaseBackup

# IDE files
.idea/
.vscode/
*.swp
*.swo

# OS files
.DS_Store
Thumbs.db

# Logs
*.log

# Dependencies
.classpath
.project
.settings/
```

### Workflow Example

1. **Initialize Repository**
   ```bash
   git init
   git config user.name "Student Name"
   git config user.email "student@example.com"
   ```

2. **Create Initial Commit**
   ```bash
   echo "# Project" > README.md
   git add README.md
   git commit -m "Initial commit"
   ```

3. **Create Feature Branch**
   ```bash
   git checkout -b feature/login
   # Make changes
   git add .
   git commit -m "Add login feature"
   ```

4. **Switch and Merge**
   ```bash
   git checkout main
   git merge feature/login
   ```

5. **Push to Remote**
   ```bash
   git push -u origin main
   git push origin feature/login
   ```

### Common Merge Conflicts

When conflicts occur:
```bash
# View conflict status
git status

# Edit conflicted files manually
# Markers: <<<<<<< HEAD, ======, >>>>>>

# Resolve conflicts
git add <resolved-file>
git commit -m "Resolve merge conflict"
```

### Best Practices

1. **Meaningful Commit Messages**
   - Use imperative mood ("Add feature" not "Added feature")
   - Keep messages concise but descriptive
   - Reference issue numbers when applicable

2. **Frequent Commits**
   - Commit logical units of work
   - Avoid mixing unrelated changes

3. **Branch Naming Conventions**
   - `feature/<feature-name>`
   - `bugfix/<bug-description>`
   - `hotfix/<issue-description>`

4. **Pull Before Push**
   - Always pull latest changes before pushing
   - Resolve conflicts locally

5. **Code Review**
   - Use pull requests for code review
   - Require at least one approval before merging

### Project Structure
```
2400033034_FSAD_Skill_exp-1/
├── README.md                 # This file
├── .gitignore               # Git ignore rules
├── src/
│   ├── HelloGit.java
│   └── GitDemo.java
└── docs/
    └── git-commands.md
```

### Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/Yogeshcheedalla/2400033034_FSAD_Skill_exp-1.git
   cd 2400033034_FSAD_Skill_exp-1
   ```

2. View the project structure:
   ```bash
   ls -la
   ```

3. Explore Git history:
   ```bash
   git log --oneline --graph --all
   ```

4. Create a new branch and make changes:
   ```bash
   git checkout -b my-feature
   # Make changes
   git add .
   git commit -m "Add my feature"
   ```

### Assessment Criteria

- [ ] Repository properly initialized with Git
- [ ] README documentation complete
- [ ] .gitignore properly configured
- [ ] Multiple commits with meaningful messages
- [ ] At least one feature branch created and merged
- [ ] Remote repository linked and code pushed
- [ ] Proper directory structure maintained

### References

- [Git Official Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Git Cheat Sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet/)

### Author
**Student ID:** 2400033034
**Course:** Full Stack Application Development (FSAD)
**Experiment:** 1 - Git Version Control

### Last Updated
March 2026
