# NYU GSAS PhD thesis template

A PhD dissertation/thesis template satisfying the [requirements]
https://gsas.nyu.edu/academics/submitting-your-dissertation.html of NYU's Graduate School of Arts and Sciences (as of 2007,2019,2021,2023/2025).

The official guidelines provided here:
https://gsas.nyu.edu/content/dam/nyu-as/gsas/documents/dissertationsubmissionrelated/A%20Formatting%20Guide%20(UPDATING%2010-09-15).pdf


This is based on a template by José Koiller (2007-2008).
Modified by Siddharth Krishna, 2019.
Revised by Quynh M Nguyen, 2021.
Further Modified by Weiwei He, 2023/2025
% Updates by Weiwei He:
% - 2023/2025: introduced improved section layouts and citation formatting.
% - 2023/2025: added support for Angstrom symbol, chemical formulas, list of appendix, and advanced table formatting (three-part tables, split cells, and diagonal lines).
% **The key update in this 2025 version is the added support for a "List of Appendices" page before the main thesis body, a feature required by NYU but not available in the 2021 version.**

How to use:
- The `thesis.tex` file is the main file for the thesis.
  `abstractpage.tex` is to create a stand-alone abstract page (required for the preliminary submission).
- In both, modify the macros under "Thesis Metadata" with your name, thesis title, etc.
- Add your own macros and additional latex packages to `defs.tex`.
- Replace the content under "Body of Thesis" with your thesis.
  I'd recommend using a file per chapter and using `\input` commands to include them in `thesis.tex`.

We hope this can help Feedback (via issues) and updates (via pull requests) welcome.
