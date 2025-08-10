(The project is still on going, gonna update later soon. I promise.)

# Analysis of Academic Performance and Major Preferences & Distribution in 1CS Students at ESI SBA

## Overview

This mini-research project grew out of my curiosity about the trends that shape my college community. Using the limited dataset I had access to, I wanted to explore how **academic performance** relates to the majors students aspire to pursue in 2CS (4th year) and beyond.

The analysis focuses on three consecutive promotions (2022-2025) of 1CS students at ESI SBA, with an emphasis on how performance patterns and preferences interact under different student allocation policies.

The analysis also considers the effect of a recent policy change, where the administration shifted from an equal seat distribution between majors to an uneven allocation model, implemented alongside a first-come-first-serve registration system.

## Objectives

I had a few questions in mind:

- **Performance trends:** How does academic performance vary from one promotion to another?
- **Performance–preference correlation:** Is there a relationship between a student’s performance and their eventual preferred major?
- **Policy impact:** How has the shift from an *equal distribution of seats across majors* to an *uneven distribution model* affected major selection trends?


## Data In Hand

### Data Description

The dataset contains student information from three promotions of 1CS at ESI SBA, including their academic performance, assigned major, and (for two promotions) their ranked preferences of majors for 2CS. The features are:

| Feature         | Type  | Description                                                   |
| --------------- | ----- | ------------------------------------------------------------- |
| `N`           | int   | Sequential student index within the dataset.                  |
| `NINSC`       | str   | Student registration number.                                  |
| `Nom`         | str   | Student’s last name.                                         |
| `Prenom`      | str   | Student’s first name.                                        |
| `MG-C`        | float | Student’s annual average score (out of 20) in 1CS.           |
| `Choix 1–4`  | str   | Ordered list of preferred majors, from most to least desired. |
| `Affectation` | str   | Final major assigned to the student.                          |

The data was collected by extracting and consolidating information from old administrative emails. The format varied between promotions, so it was normalized into a unified structure for analysis.

A key limitation is that **major preference data (`Choix 1–4`) is missing for the 2023–2024 promotion** (Promo 21/22 in this dataset). As a result, preference analysis only includes Promo 20/21 and Promo 22/23, while Promo 21/22 is only considered in the context of final allocations and academic performance.

### Majors in the Dataset

At ESI SBA, students in 2CS (4th year) can specialize in one of several majors. In this dataset, the following majors are present:

* **SIW** ( *Systèmes d’Information et Web* ) — Oriented towards web development, information systems, and software engineering.
* **ISI** ( *Ingénierie des Systèmes Informatiques* ) — Specializing in systems engineering, networking, and distributed computing.
* **IASD** ( *Intelligence Artificielle et Science des Données* ) — A newer AI and data science-focused track (introduced later in the dataset).
* **CyS** ( *Cyber Security* ) — Concentrated on network security, cryptography, and system protection. **This major was introduced in the most recent promotion (Promo 22/23)** and was not available in previous years.
