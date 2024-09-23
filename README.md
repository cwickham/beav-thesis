# `beav` Quarto format for Oregon State University Theses

Organize your thesis like a Quarto book, e.g in `_quarto.yml`:

```{.yaml}
book:
  title: "Thesis Title"
  author: "Jane Doe"
  date: "January 1, 2013"
  chapters:
    - index.qmd
    - conclusion.qmd
    - references.qmd
  appendices: 
    - appendix.qmd
```

Set `thesis` metadata in `_quarto.yml`:

```{.yaml}
thesis:    
  doctype: Dissertation
  major: Statistics
  advisor: Jane R. Professor
  coadvisor: John S. Professor
  depttype: Department
  department: Statistics
  depthead: Head
  commencementyear: 2013
  degree: Master of Science
  acknowledgements: I would like to acknowledge...
  abstract: > 
    This is a LaTex template derived from the beavtex template found 
    on the Oregon State University Math Department website. 
```

This example sets co-major advisors for a single major. Set `twomajor`, `twodepartment`, `twodepttype`, and `twodepthead` with values corresponding to your second major if you have one.

You may optionally also set: `contributions`, `dedication` and `preface`.

When drafting you may find it useful to preview individual chapters using the `html` format:

```{.bash}
quarto preview index.qmd --to html
```

(Or use the usual "Render"/"Preview" buttons).

When you are ready for the final version, render the project to `beav-pdf`:

```{.bash}
quarto render --to beav-pdf
```

## Acknowlegements

Build on the [`beavtex.cls`](_extensions/beav/beavtex.cls) style authored by: Rick Treinen, Neville Mehta, Deling Ren and John Metta.

