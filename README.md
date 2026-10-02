# IEAP-Series02-RStudio

Team assignment for the **IEAP 2025 – Series 02 RStudio** course
(*Data mining and statistical tests*, Denis Mottet).

Repository: <https://github.com/sdurand875-spec/IEAP-Series02-RStudio>

## Authors

| Member | Part of the report | Branch |
|---|---|---|
| Damien Clanet | 2.1 – What is a statistical test, and when to use it? | (see Git history) |
| Sarah Durand | 2.2 – Effect of treatment over time (`PrePost.csv`) | `Sarah-2.2` |
| Albatoul Ahmad | 2.3 – Testing some stereotypes (`snore.txt`) | `albatoul-2.3` |

The common parts (Git workflow, challenges, data sources, references and
checklist) were written together.

## Repository structure

```
IEAP-Series02-RStudio/
├── IEAP-Series02-Rstudio.qmd   # main Quarto document (header + includes)
├── IEAP-Series02-Rstudio.pdf   # rendered report (also uploaded on Moodle)
├── Sections/                   # one sub-document per part / per member
│   ├── Damien_2.1-definitions.qmd
│   ├── Sarah_2.2-prepost.qmd
│   ├── Albatoul_2.3-snore.qmd
│   ├── Team_git-workflow.qmd
│   ├── Team_sources-references.qmd
│   └── Team_checklist.qmd
├── data/                       # PrePost.csv, snore.txt
├── IEAP-Series02-RStudio.Rproj # RStudio project
├── README.md
└── LICENSE                     # MIT license (also LICENSE.md)
```

The main document only contains the YAML header and `{{< include >}}`
statements. Each team member works in their own file in `Sections/`, which
avoids merge conflicts.

## How to render the report

1. Open `IEAP-Series02-RStudio.Rproj` in RStudio.
2. Install the required packages once:
   `install.packages(c("tidyverse", "here"))`
3. If needed, install a LaTeX distribution for the PDF output:
   `quarto install tinytex` (in the RStudio Terminal).
4. Open `IEAP-Series02-Rstudio.qmd` and click **Render**.

Data files are read with the `here` package (e.g.
`here("data", "PrePost.csv")`), so paths work both when running a chunk
interactively and when rendering the main document.

## Git workflow (summary)

- `main` contains the validated version and is the graded branch.
- Each member works on their own branch, with at least one commit per
  question, then opens a Pull Request into `main`.
- Problems are reported with GitHub Issues and fixed through a dedicated
  branch and Pull Request (e.g. issue #3 closed by PR #4).

See the section *Team workflow strategy with Git* in the report for details.

## License

This project is released under the MIT License (see `LICENSE`).
