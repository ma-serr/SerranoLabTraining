# Serrano Lab Training Matrix

The **Serrano Lab Training Matrix** is a self-contained, interactive web tool designed to facilitate structured skill development for trainees in the Serrano Lab. It enables easy tracking of progress, documentation of evidence, and simplified reporting.

## Table of Contents

* [I. Guidelines for Mentees](#i-guidelines-for-mentees)

  * [1. Getting Started](#1-getting-started)

    * [Access the Matrix](#access-the-matrix)
    * [Select Your Trainee Level](#select-your-trainee-level)
  * [2. Tracking Your Progress](#2-tracking-your-progress)

    * [Enter Your Name](#enter-your-name)
    * [Record Skill Status](#record-skill-status)
    * [Monitor Your Progress](#monitor-your-progress)
  * [3. Saving & Submitting](#3-saving--submitting)
* [II. Guidance for Adopters](#ii-guidance-for-adopters)

  * [1. Setup & Installation](#1-setup--installation)

    * [Prerequisites](#prerequisites)
    * [Installation](#installation)
  * [2. Customization](#2-customization)
  * [3. Deployment](#3-deployment)

    * [GitHub Pages](#github-pages)
    * [Local Hosting](#local-hosting)
  * [4. Contribution](#4-contribution)
  * [5. License & Attribution](#5-license--attribution)


## I. Guidelines for Mentees

### 1. Getting Started

#### Access the Matrix

* Open `index.html` in your web browser (Chrome, Firefox, Safari, Edge).
* Ensure you have an active internet connection (for Chart.js and Formspree integration).

#### Select Your Trainee Level

* Choose **Undergraduate**, **PhD**, **Post‑doc**, or **Staff/Technician**.
* The matrix will display only the skills relevant to your selection (plus core requirements).

### 2. Tracking Your Progress

#### Enter Your Name

* Type your full name into the “Mentee Name” field at the top.

#### Record Skill Status

* Click any category header to expand or collapse sections.
* For each skill row:

  * Select a **Status**: Not Started, In Progress, Blocked, Needs Refresh, or Complete.
  * Paste any **Evidence URL(s)**.
  * Add **Notes** in the textarea provided.
  * Check off **yearly milestone** boxes (this year and future years).
  * Optionally, click “Completed 2022–2024” to auto‑check all past years.

#### Monitor Your Progress

* The **overall progress bar** at the top updates in real time.
* Each row has a **mini progress bar** showing that skill’s completion percentage.
* The **category chart** (Chart.js) breaks down completion by skill group.

### 3. Saving & Submitting

* **Download CSV**: Export your matrix data (includes version tag and timestamp).
* **Download PDF**: Opens the print dialog (you can save as PDF).
* **Send Progress**: Prompts for your email and submits the matrix via Formspree.



## II. Guidance for Adopters

This tool is open‑source and can be adapted for your lab or training environment. Please cite:

> “Training Matrix by Serrano Lab, Center for Regenerative Medicine (CReM), Boston University.”

### 1. Setup & Installation

#### Prerequisites

* A modern browser (Chrome, Firefox, Safari, Edge).
* Internet access for external libraries (Chart.js CDN, Formspree).

#### Installation

```bash
 git clone https://github.com/SerranoLab/training-matrix.git
 cd training-matrix
```

To launch locally:

* Double‑click **index.html**, or
* Serve via local server:

  ```bash
  npx serve .
  ```

### 2. Customization

* **Logo & Branding**: Replace `logo.png` and update `<img>` path in `index.html`.
* **Color Scheme**: Edit CSS variables in the `<style>` block (`--brand-blue`, `--brand-orange`, etc.).
* **Skill Content**: Modify the `mentoringAreas` array at the bottom of `index.html`:

  ```js
  const mentoringAreas = [ /* your groups, topics, and skills */ ];
  ```
* **Form Submission**: Change the Formspree `action` URL in the `<form>` element or integrate your own backend.

### 3. Deployment

* **GitHub Pages**:

  1. Push repo to GitHub.
  2. In Settings → Pages, set source to `main` (root).

* **Local Hosting**:

  ```bash
  python3 -m http.server 8000
  ```

### 4. Contribution

Contributions are welcome:

1. Fork the repository.
2. Create a branch: `git checkout -b feature/YourFeature`.
3. Commit: `git commit -m "Describe your changes"`.
4. Push: `git push origin feature/YourFeature`.
5. Open a pull request.

### 5. License & Attribution

This project is licensed under the [MIT License](LICENSE).

© Serrano Lab, Center for Regenerative Medicine (CReM), Boston University. Please attribute as above when using or adapting this tool.


