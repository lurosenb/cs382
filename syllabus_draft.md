# Responsible Machine Learning
**Course Syllabus**

---

## Course Overview

Responsible Machine Learning is the science and practice of designing algorithms and deploying AI systems in ways that are socially sustainable. This course introduces students to core technical and socio-technical objectives in responsible AI, with an emphasis on algorithmic fairness, transparency and interpretability, differential privacy, and bias and risk factors for large language models.

This course is sociotechnically grounded. Students will examine how and why machine learning systems can produce harmful or inequitable outcomes, and how different stakeholders (impacted communities, developers, institutions, and regulators) define "responsible" in ways that are sometimes in conflict. Students will learn to evaluate these trade-offs, while thinking carefully about mitigation techniques. There will be a focuse on communicating technical results clearly.

The course integrates both conceptual frameworks (ethics, governance, legal and policy constraints) and technical solutions (models with fairness and privacy constraints, explainability toolkits, and more). Students will work in Python to analyze datasets and write models, apply bias mitigation methods, generate explanations for model decisions, and explore privacy-preserving data releases. Students will also work on some problems requiring mathematical proofs and prerequisite knowledge of probability and statistics. Students will be assessed on their ability to present their work coherently and demonstrate mastery of the material.

---

## Learning Goals

By the end of this course, students will:

1. **Understand the motivations and stakes of responsible machine learning**, including the historical and ongoing harms caused by poorly designed systems, and why sociotechnical perspectives are essential to addressing them.
2. **Develop fluency with the major tools and frameworks** the RML community has produced over the past two decades, including fairness metrics and constraints, interpretability and explainability methods, differential privacy, and LLM risk evaluation.
3. **Gain hands-on experience applying this toolkit** to hard, open-ended problems through structured lab work and an original research project.

---

## Lab Sections

Lab sections alternate between two types of weeks: **(A) Problem weeks** and **(B) Presentation weeks**. Students will be organized into permanent groups of three at the start of the semester (six groups total). Each group is assigned a home problem set (Set 1, 2, or 3), with two groups sharing each set.

### (A) Problem Weeks
Groups work through their assigned problem set during lab. Problem sets consist of 1–2 challenging problems. **No laptops, phones, or electronic devices are permitted.** A printed reference sheet of useful formulas and prior results will be provided. Any student found using technology during an (A) week will receive a zero for that lab.

Students will submit notes for completion credit: one group member is responsible for photographing the group's work (from the blackboard or paper) and uploading it to the shared drive.

### (B) Presentation Weeks
Groups pair with a group that worked a *different* problem set and present their solutions. The emphasis is not only on the correctness of the solution, but on the process: What did students notice? What was the intuition? Each presentation should last approximately 10–20 minutes and should genuinely educate the audience: both on how the solution works and on the intuition behind the problem itself.

Grading for (B) weeks is completion-based, assessed on the quality and coherence of the presented solution. Students are expected to have put genuine thought into how they will structure their presentation. **Every student must speak**: at minimum, one student may serve as the designated question-answerer at the end. After (B) week, full solutions will be released for all three problem sets.

---

## Quizzes

Short quizzes (10 minutes), consisting of multiple-choice and true/false questions, will be held on Mondays and will cover lecture content from the preceding week. Students will vote at the start of the semester on their preferred timing within the lecture period: beginning, middle, or end. Each quiz will be worth 1 point. Students will have ~12 quizzes, though only need 10 points to acheive full credit on the quiz category towards their final grade. Thus, students could (in principle) miss up to 2 quizzes entirely and still receive full credit. For this reason, make-up quizzes will only be given under extreme circumstances.

---

## Midterm and Final Exam

The midterm and final exams share a consistent format: a section of multiple-choice and true/false questions (similar in style to the weekly quizzes) and a section of lab-style problems (similar in style to the lab problem sets, but somewhat more accessible). Students may also be asked to write some free-responses. The best preparation is a thorough understanding of all quiz questions and lab problems encountered throughout the semester.

---

## Research Project

Students will work in **groups of two** on a semester-long research project that mimics the research process applied to an open RML question. Students will be required to schedule time to meet with the instructor during instructor office hour blocks at designated project milestones.

### Deliverable 1: GitHub Repository

Students will create and maintain a GitHub repository with the following structure:

```
README.md              # Research question and proposed approach
data/                  # Data and data-loading code
src/                   # Python package
  utils/               # Helper code
  <project_name>/      # Core project module
  metrics/             # Metrics and plotting code
exp_runner.py          # Main experiment runner
exp_***.py             # Additional experiment scripts
env.yaml               # Conda environment specification
```

Code must be clean, well-commented, and reproducible after correct Conda environment setup.

A github template is available for students to use as a starting point, with templated files and already functional example imports, etc.

### Deliverable 2: Workshop Paper

Students will produce a 4-page article formatted as a workshop paper for an ML conference, written in Overleaf. This paper is the primary artifact used to evaluate the project. References will not count against this page limit. An additional 6 pages of appendix are available for supplementary figures and details. Reports over 10 pages (excluding references) will receive a minor deduction.

### Deliverable 3: Class Presentation

Students will give a **10-minute presentation** to the full class. Both project partners must speak. The prescribed format is:

- **Title slide**
- **Problem statement** (3–5 slides): Ensure the class has a clear understanding of the problem and why it matters. Most important part of the presentation!
- **Data, experimental setup, and metrics** (1-3 slides): Explain how success will be evaluated.
- **Key result** (1 slide): Walk through a single plot or table in detail and explain what it means for the broader research question.
- **Summary and takeaways** (1 slide): State the conclusions clearly.

Presentations are evaluated on clarity and insight. Slides that favor intuitive visuals over dense text will receive higher marks.

> **Note:** Students who produce strong projects should consider submitting their work to an actual RML workshop. The instructor will support any interested students through this process.

---

## Homework

Homeworks will include a variety of problems and exploration of relevant Python packages, designed to build intuition and prepare students for exams and the research project. **Grading emphasizes completion over correctness**, in order to incentivize authentic engagement over shortcuts (e.g., using an LLM to complete the whole thing quickly). Students who invest genuinely in the homework will be better prepared for quizzes/exams, and will also produce more interesting projects; students who do not are likely to find the course more difficult as a whole.

---

## Course Policies

### Language Models

This course is designed to be largely agnostic to LLM usage. Students who rely on language models for assignments may find themselves at a disadvantage when assessments arrive, as exams and quizzes weeks are designed to test understanding. Students are **softly encouraged** to use LLMs for the coding portions of the research project, as this part of the class requires extensive efforts. However, the written portions of the project should reflect the joint work of both project partners, and students are discouraged from using LLMs for the article, beyond grammatical checks and cleaning up language.

### Engagement

While lecture engagement is not formally graded, it is greatly appreciated. Lab sections serve as the primary participation check.

---

## Grade Breakdown

| Component | Weight |
|-----------|--------|
| Quizzes | 10% |
| Midterm | 15% |
| Final Exam | 20% |
| Labs | 20% |
| Research Project | 20% |
| Homework | 15% |
| **Total** | **100%** |
