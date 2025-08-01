# Motorq Data Science Assignment 2025 - CE

## Overview
This repository contains the Motorq Data Science Assignment for 2025, focusing on data science and machine learning challenges in the automotive/vehicle telemetry domain.

## Repository Structure
This repository includes:

- **Problem Statement**: `problem_statement_ce.pdf` - Detailed assignment requirements and specifications
- **Assignment Materials**: `Motorq Data Science Assignment - 2025.zip` - Complete dataset and supporting files (managed via Git LFS)
- **Documentation**: This README file
- **Git LFS Configuration**: `.gitattributes` - Ensures large files are handled efficiently

## Technical Setup

### Git LFS (Large File Storage)
This repository uses Git LFS to efficiently manage large files:
- **Tracked file types**: `*.zip`
- **Large files**: Assignment dataset (60MB) stored via LFS
- **Benefits**: Faster clones, reduced repository size, efficient handling of binary files

### Getting Started
1. **Clone the repository**:
   ```bash
   git clone https://github.com/theharshavinash/ds_assement_2026_summer_intern_CE.git
   cd ds_assement_2026_summer_intern_CE
   ```

2. **Ensure Git LFS is installed**:
   ```bash
   git lfs version
   ```
   If not installed, install via: `brew install git-lfs` (macOS) or visit [git-lfs.github.io](https://git-lfs.github.io/)

3. **Pull LFS files** (if needed):
   ```bash
   git lfs pull
   ```

4. **Extract assignment materials**:
   ```bash
   unzip "Motorq Data Science Assignment - 2025.zip"
   ```

5. **Review the problem statement**:
   - Open `problem_statement_ce.pdf` for detailed requirements
   - Follow the specifications and deliverables outlined

## File Descriptions

### Core Files
- **`problem_statement_ce.pdf`** (1.2MB): Complete assignment specification with requirements, evaluation criteria, and submission guidelines
- **`Motorq Data Science Assignment - 2025.zip`** (60MB): Comprehensive dataset package containing:
  - Training and test datasets
  - Data dictionaries and schemas
  - Sample code or notebooks (if applicable)
  - Additional resources and documentation

### Configuration Files
- **`.gitignore`**: Standard Git ignore patterns for data science projects
- **`.gitattributes`**: Git LFS configuration for large file management

## Assignment Workflow
1. **Understand Requirements**: Review the problem statement thoroughly
2. **Data Exploration**: Extract and analyze the provided datasets
3. **Solution Development**: Implement the required analysis/models
4. **Documentation**: Create comprehensive documentation of your approach
5. **Submission**: Follow the submission guidelines in the problem statement

## Best Practices
- Keep your code modular and well-documented
- Use version control effectively for your solution
- Include clear explanations of your methodology
- Validate your results and include performance metrics
- Follow data science best practices for reproducibility

## Support
For questions or clarifications regarding the assignment, refer to the contact information provided in the problem statement document.

---
*This repository demonstrates proper setup of Git LFS for data science projects with large datasets.*
