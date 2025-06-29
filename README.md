# README
Steven J. Pierce

<!-- README.md is generated from README.Rmd. Please edit that file -->

# SANETPA Package Documentation

<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![Project Status: WIP – Initial development is in progress, but there
has not yet been a stable, usable release suitable for the
public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip)
[![CRAN
status](https://www.r-pkg.org/badges/version/SANETPA.png)](https://CRAN.R-project.org/package=SANETPA)
<!-- badges: end -->

This package (Pierce, 2025) is a research compendium (Marwick et al.,
2018) for a study examining attrition from a sexual assault nurse
examiner (SANE) training program. The research team is led by
Dr. Katherine Dontje (PI) and Dr. Rebecca Campbell (Co-I) at Michigan
State University and was supported by a grant (Dontje & Campbell,
07/01/2021–06/30/2025).

## Assumptions

We eventually expect two different types of users of this package:
collaborators and readers. Collaborators include members of the research
team working on the project prior to publication who may contribute to
the code. Readers include members of the public who simply want to
reproduce the computations and analyses after reading the paper. These
instructions include some steps that are more relevant to collaborators
than to readers.

To collaborate on the code for this package, you must have a GitHub
account. You can request such access by emailing the package maintainer
your GitHub username and ask to be added as a collaborator on this
repository. You will need to use [Git](https:/git-scm.com) (Torvalds et
al., 2025) for version control on files associated with this package and
to synchronize changes between your local copy of the repository and
[GitHub](https://github.com), with
[RStudio](https://posit.co/products/open-source/rstudio/) (RStudio Team,
2025) as the primary editor. There is a lot of useful information about
using these tools at the [Happy Git and GitHub for the
userR](https://happygitwithr.com) website (Bryan et al., n.d.). Other
useful resources on using Git and GitHub include Bryan (2018) and
Perez-Riverol et al. (2016). Meanwhile, Wickham & Bryan (2021) provides
extensive guidance on creating R packages. Chacon & Straub (2014) is a
full book on using Git for version control.

Changes made to files in a local copy of the repository should be
committed and pushed to the main branch of the remote *SANETPA*
repository on GitHub. See Bryan (2018) for a short introduction to why
this is good practice.

We assume you are using the most recent stable release versions of the
software packages discussed below and also frequently updating your
installed R packages.

## Installation

This package is only available from a *private* repository available on
the [GitHub server](https://github.com) at
https://github.com/sjpierce/SANETPA. Private repositories are only
visible to GitHub users who are logged in and have been registered by
the repository owner as a collaborator on the project.

This package’s repository will remain private until the associated
manuscript has been accepted for publication. Once that happens, the
repository may be made public to enable readers to reproduce the
analyses.

The package can be installed with the information shown below. The
overall goal here is to set you up for using a suite of software tools
and practices that works well for reproducible research. That will
facilitate using this package.

### Create a GitHub Account (Optional for Readers)

You should create a GitHub user account before proceeding further. After
you have the GitHub account, send the *SANETPA* package maintainer your
GitHub username and ask to be added as a collaborator on the repository.
This is necessary because the main branch of the package repository is
stored on GitHub. You will need to be able to use Git and GitHub to
synchronize changes between your local copy of the repository and
GitHub.

### Install R 4.5.1 or later.

You can get the most recent version of R (R Development Core Team, 2025)
from the [Comprehensive R Archive Network
(CRAN)](https://cran.r-project.org/).

### Install tools for compiling packages

Install any tools required for compiling packages (they will be specific
to your operating system). These will be necessary for the *devtools*
package to work.

- On Windows, see https://cran.r-project.org/bin/windows/Rtools/.
- On Mac OS X, see https://cran.r-project.org/bin/macosx/tools and
  https://mac.R-project.org/tools/.

### Install RStudio Desktop

Install [RStudio
Desktop](https://posit.co/products/open-source/rstudio/) version
2025.05.1+513 (or later). We recommend using RStudio to interact with
the files for this package. RStudio is both a good interface to R and
has built-in support for using some of the other software discussed
below.

### Install Quarto

We rely on [Quarto](https://quarto.org) (Allaire et al., 2025) scripts
to enhance reproducibility because they provide excellent support for
generating dynamic reports (Mair, 2016). Install Quarto version 1.7.32
or later. Although RStudio bundles a version of Quarto, we want the most
recent stable release instead. Quarto also includes a copy of
[Pandoc](https://pandoc.org/).

- To download Quarto, visit https://quarto.org/docs/get-started/

### Install Git (Optional for Readers)

This step is required for collaborators, but optional for readers.
Readers can just skip to the “Install *devtools* package section”.

Install [Git](https://git-scm.com/). We use this for version control on
the package code. Get the most recent version available for your
operating system. See instructions at
https://happygitwithr.com/install-git.html.

- On Windows, download from https://git-scm.com/download/win
- On MacOS, download from https://git-scm.com/download/mac

### Configure Git (Optional for Readers)

This step is required for collaborators, but optional for readers.
Readers can just skip to the “Install *devtools* package” section.

Configure Git using the instructions at
https://happygitwithr.com/hello-git.html. RStudio can be your main
interface to the Git client most of the time, but occasionally using a
Git Bash command window instead is more useful. You can open that by
clicking **Start \> All Programs \> Git \> Git Bash** on your own
computer.

### Connect Git, GitHub, and RStudio (Optional for Readers)

You will need to configure RStudio to use Git and GitHub. Use the
instructions at https://happygitwithr.com/connect-intro.html. The reason
for that is that because RStudio is both a good interface to R and has
built-in support for Git.

#### Obtain a GitHub personal access token (PAT)

Read Section 9 of the Happy Git with R website
(https://happygitwithr.com/https-pat.html) to learn more about what a
PAT is, how to get one, and why it is useful. The following subsections
may be particularly useful.

- https://happygitwithr.com/https-pat.html#valid-pat-gets-stored-but-later-told-the-pat-is-invalid
- https://happygitwithr.com/https-pat.html#pat-doesnt-persist-on-macos-or-windows
- https://happygitwithr.com/https-pat.html#pat-doesnt-persist-on-linux

You may also want to read GitHub documentation about managing PATs
(https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

Visit https://github.com/settings/tokens to create a PAT that has the
`gist`, `repo`, `user`, and `workflow` scopes. Once you have it, you’ll
need to store it so your computer can find your PAT automatically.

#### Store your GitHub PAT in the Git Credential Manager

We want to store your PAT in the Git Credential Manager because that
allows RStudio and Git to easily connect to GitHub for pushing and
pulling commits.

We can use the
[*credentials*](https://cran.r-project.org/package=credentials) package
for R to facilitate this task.

``` r
# If you don't already have it installed.
install.packages("credentials")
```

Then, run the following function call.

``` r
credentials::git_credential_ask("https://github.com")
```

If this prompts you for username and password, use the PAT as the
password. If that just displays a result but the password does not match
your PAT, run the code below then enter your GitHub username and use
your PAT as the password.

``` r
credentials::git_credential_update("https://github.com")
```

### Install *devtools* Package

Install the [*devtools*](https://devtools.r-lib.org/) package for R. The
most recent [CRAN release](https://cran.r-project.org/package=devtools)
will likely be more stable but sometimes you may instead need the
[development version at GitHub](https://github.com/r-lib/devtools). This
package provides developer tools/functions that simplify creating,
quality-checking, and installing custom R packages. You can use the
following command at the R console.

``` r
install.packages("devtools")
```

### Install *piercer* Package

Install the [*piercer*](https://github.com/sjpierce/piercer) package for
R. Instructions for doing that are at the link. Please read and follow
them before trying to install or use this package.

### Install TinyTex

[TinyTex](https://yihui.org/tinytex/) is a specific distribution of
LaTeX, which is document preparation software that allows high-quality
typesetting. It takes plain text LaTeX files (`*.tex` files) that
describe the structure of a document and compiles them into
fully-formatted PDF files with nice fonts and layout. We can actually
use the R package called
[tinytex](https://cran.r-project.org/package=tinytex) to install TinyTeX
via the following commands inside R.

``` r
# If you don't already have it installed.
install.packages("tinytex")
```

``` r
tinytex::install_tinytex()
```

You can use alternative LaTeX distributions and tools (e.g.,
[MiKTeX](https://miktex.org/)) instead, but TinyTeX is very convenient
because of how well it integrates with the other tools we’re using.

Major versions of TinyTex are released at least annually. If it has been
a long time since you last installed TinyTeX, you may want to update it
using the code below. This should refresh both the base TinyTex and the
LaTeX packages you have previously installed by using it.

``` r
tinytex::reinstall_tinytex()
```

### Update Your R packages

It is a good idea to update all your R packages. You may be prompted
with a dialog box asking “Do you want to install from sources the
packages which need compilation?” It usually works fine if I choose
“no”. Occasionally, it appears necessary to choose “yes”, but I am more
likely to run into problems when doing that.

``` r
update.packages(ask='graphics', checkBuilt=TRUE)
```

If you previously were using an older version of R (any version before
4.5.0), you should plan to reinstall all your R packages from scratch.
The best way to do that is to use a script such as
`scripts/Reinstall_Packages.R` under the older version to save a data
file containing the names of installed packages, then remove the older
version of R and replace it with the newest version of R, and use the
remainder of that script to read in that list of packages and install
them. That will take several minutes if you have a lot of packages.

### Clone the *SANETPA* Repository from GitHub to your Local Computer

#### Instructions for readers not using Git & GitHub

Once the repository is made public, readers should be able to download a
ZIP file containing the latest released version of the repository
contents from https://github.com/sjpierce/SANETPA/releases/latest. Just
unzip that to create a folder on your local computer such as
`C:\Users\username\Documents\SANETPA`; that will be your local copy of
the repository.

#### Instructions for collaborators and readers using Git & GitHub

If you want to work with the package on your laptop, use RStudio to
clone the *SANETPA* package from GitHub (the repository source is
https://github.com/sjpierce/SANETPA.git) to a local folder on your
computer such as `C:\Users\username\Documents\SANETPA`. This is the
folder where you would edit scripts and files and that you would
synchronize with the GitHub main branch via Git’s *pull* and *push*
operations.

Ideally, only one person should be using a given local repository at a
time. The beauty of Git is that it allows us all synchronize with the
main repository on GitHub regardless of where our local copies are
stored.

### Install *SANETPA* to your personal package library

You have to install the package to your personal R package library
before some of the scripts will work because they may depend on
functions defined in the package. This personal R package library would
usually be in a location such as
`C:\Users\username\AppData\Local\R\win-library\4.5\SANETPA` on your
laptop, desktop, or on the server. Note that this is distinct from the
local repository folder!

Scripts that do not have a `library(SANETPA)` call in them may work
without the package being installed, but those containing that call
depend on custom functions found only in the *SANETPA* package. When you
use that call, R loads the copy of the package found in your personal R
package library, not from the local Git repository.

Now you should be ready to actually install the package. There are two
main ways to do that: from GitHub and from the local repository. Both
are explained below.

#### Install from GitHub (recommended for collaborators and readers using Git & GitHub)

You should be ready to actually install the package from the main branch
on GitHub. This is the recommended default method for installing
*SANETPA*.

``` r
devtools::install_github(repo = "sjpierce/SANETPA", dependencies = TRUE)
```

If you can use Git pull and push successfully but the installation
command above does not work, the problem may be that you need to store
your Git credentials in the Git credential manager or to update them
there.

#### Install from the local respository (recommended for readers not using Git & GitHub)

You may sometimes want to build and install the package from the local
repository directly to your personal R package library instead of
pulling the copy from GitHub. This can be useful when testing new code
before you commit it to the main branch or if you do not use Git and
GitHub.

Double-click the `SANETPA.Rproj` file from Windows Explorer. That should
open the project in RStudio. Then run the following code in a fresh R
session.

``` r
library(devtools)
document()
check()
install()
```

## Repository Structure and Contents

The structure for the package is shown in the outline below, where
folder names and file names are `highlighted like this` and comments are
in normal text. The folder structure is largely determined by the
conventions governing the structure of R packages. It deviates a bit
from the example research compendium folder structures discussed by
Marwick et al. (2018). The repository is also set up as an [RStudio
project](https://support.rstudio.com/hc/en-us/articles/200526207-Using-RStudio-Projects).

- `SANETPA/`: This is the root folder for the repository.
  - `.git/`: This hidden folder is used by Git. Leave it alone!
  - `.Rproj.user/`: This hidden folder is used by Rstudio. Leave it
    alone!
  - `data/`: This folder is where the data file produced by our scripts
    will be stored. This is a standard folder for R package structures.
    - `Placeholder.text` This text file is just present to ensure that
      the `data` subfolder will be created when you clone the repository
      or extract files from ZIP file copy of the repository obtained
      from GitHub.
  - `man/`: This folder contains R documentation help files (`*.Rd`) for
    the package and its custom functions. It is required by R package
    building conventions. You should not edit these files manually and
    you really only access them through R’s normal help system.
  - `R/`: This folder contains the source code for the package’s custom
    functions in a set of `*.R` script files. It is required by R
    package building conventions.
    - `SANETPA-package.R`: This script file is used to automate creating
      package level help files. Do not edit it manually.
  - `scripts/` The folder is configured as a Quarto project. It holds
    meta-data files, `.qmd` scripts, and files used by the scripts.
    - `extdata/`: This subfolder is where you will need to put any raw
      data files mentioned in the Obtaining Data Files section below.
    - `output/`: This subfolder holds rendered output files.
      - `CR_Model_Draft.pdf`: This is temporary draft output obtained by
        rendering the `scripts/CR_Model.qmd` script directly.
      - `CR_Model_yyyy-mm-dd.pdf`: Production output obtained by using
        `scripts/Production_Run.qmd` to render the
        `scripts/CR_Model.qmd` script will have names following this
        date-stamped naming convention. An actual rendering date will
        replace the `yyyy-mm-dd` notation.
      - `Import_Data_Draft.pdf`: This is temporary draft output obtained
        by rendering the `scripts/Import_Data.qmd` script directly.
      - `Import_Data_yyyy-mm-dd.pdf`: Production output obtained by
        using `scripts/Production_Run.qmd` to render the
        `scripts/Import_Data.qmd` script will have names following this
        date-stamped naming convention. An actual rendering date will
        replace the `yyyy-mm-dd` notation.
      - `Production_Run.html`: This is the log resulting from rendering
        `scripts/Production_Run.qmd`. This documents when the production
        process was last run and the result of each step.
    - `.gitignore`: This was auto-created by Quarto. Don’t edit or
      delete it.
    - `.quarto/`: This hidden folder may be created by Quarto to hold
      temporary files. Do not edit or delete any of these files unless
      you know what you are doing! This folder is not tracked by Git.
    - `_brand.yml`: This file specifies color, font, and logo settings
      for using an MSU/CSTAT branding scheme for HTML output.
    - `_quarto.yml`: This is a Quarto metadata file containing
      project-level YAML code that will be inherited by Quarto scripts
      in this folder or its subfolders.  
    - `apa.csl`: This is a citation style language file for the
      Publication Manual of the American Psychological Association, 7th
      ed. It is used by Quarto to format reference sections.
    - `compact-title.tex`: This LaTeX file can be called from an .qmd
      file’s YAML header via the in_header option. It just formats the
      title of the rendered PDF file so it uses less vertical white
      space. It is used by multiple other scripts.
    - `CR_Model.qmd`: This script runs the continuation-ratio model(s)
      that comprises the main analysis for the study. Methodology notes,
      references, and results interpretation will be built into this
      script and its output. Rendering this directly generates draft
      output named `output/CR_Model_Draft.pdf`; you can get date-stamped
      production output (e.g., `output/CR_Model_yyyy-mm-dd.html`) by
      using `scripts/Production_Run.qmd` to render this script.
    - `Delete_nul_file.bat`: This is a Windows batch file that automates
      removing a nuisance file sometimes left over when rendering a
      Quarto or R Markdown script doesn’t work right.
    - `Development_Tools.R`: This contains some examples of R commands I
      use interactively when working on the package.
    - `Example_Render_to_HTML.qmd`: This is just an example script that
      you can copy to start a new script that will produce an HTML
      output file.
    - `Example_Render_to_PDF.qmd`: This is just an example script that
      you can copy to start a new script that will produce a PDF output
      file.
    - `Import_Data.qmd`: This script imports the raw data from SPSS and
      saves it in an .RData file for use by other scripts here.
      Rendering this directly generates draft output named
      `output/Import_Data_Draft.pdf`; you can get date-stamped
      production output (e.g., `output/Import_Data_yyyy-mm-dd.pdf`) by
      using `scripts/Production_Run.qmd` to render this script.
    - `Production_Run.qmd`: This script is used to automate rendering
      other scripts in the proper order to generate date-stamped
      production outputs (e.g., `output/Import_Data_yyyy-mm-dd.pdf`). It
      also produces `scripts/output/Production_Run.html`.
    - `references.bib`: This is a BibTeX file containing the citation
      data for references mentioned in various scripts. Quarto uses it
      to get the data needed to insert reference lists.
    - `Reinstall_Packages.R`: This script contains R code that stores a
      data file containing a list of all your installed packages, plus
      code for reading that file and re-installing all of those packages
      from scratch. It automates an otherwise tedious process. You would
      use this before and after upgrading to a new version of R (e.g.,
      when going from version 4.3.x to 4.4.x).
    - `Setup_as_Package.qmd`: This is a script I used to remind myself
      of how to rapidly do various parts of turning a new repository
      into an R package. It’s only really used once.
    - `title.tex`: This LaTeX file enables better handling of author
      affiliations in PDF outputs. It is used by multiple other scripts.
  - `.gitignore`: This file tells Git what files to ignore and omit from
    synchronizing with the main repository on GitHub.
  - `.Rbuildignore`: This file tells R what files to ignore when
    building the package from the source code.
  - `DESCRIPTION`: This file is a brief, structured description of the
    package that is required by R package building conventions. It holds
    essential meta-data.
  - `LICENSE`: This file contains the terms of the license that applies
    to all source code in this repository.
  - `NAMESPACE`: This file is created automatically by R when building
    the package. You should not edit it manually. It is required by R
    package building conventions.
  - `NEWS.md`: This file contains an list of comments about the changes
    made with each version of this package. It is required by R package
    building conventions
  - `README.md`: This file is obtained by rendering the `README.qmd`
    file and is used by GitHub to display information about the package.
    Do not edit it manually: just render `README.qmd` to update it. In R
    Studio, you can read the formatted version by opening the file and
    clicking the Preview button.
  - `README.qmd`: This file gives an introduction to the package.
    Rendering it produces the `README.md` file and opens the preview
    automatically.
  - `SANETPA.Rproj`: This is an RStudio project file. It contains some
    settings for working with the project in that software.

## Software Dependencies

Scripts in this R package may depend on having a number of other R
packages installed. Those packages are listed in the `DESCRIPTION`
file’s Depends, Suggests, and Imports fields. They are mostly available
from CRAN and should be installed automatically when you install the
*SANETPA* package itself if you use `dependencies = TRUE` option.

## Software Maintenance

Many software packages are updated periodically, so it is a good idea to
update to the newest stable version of them occasionally. Most of us
accumulate a large number of installed R packages. There is a good
chance that at least one of them will have been updated every week, so
updating R packages regularly is a good idea. User-contributed packages
collectively change more often than base R.

Staying reasonably current on software versions for the whole suite of
tools we are using here will keep things working smoothly most of the
time. It also helps if we are using the same versions wherever possible
because version differences can introduce discrepancies in the results
we each obtain.

## Obtaining Data Files

The data required to use this package are not available in the GitHub
repository and should not be checked into Git version control. This
reduces the number of servers where the data files may be stored and
thereby increases data security.

To obtain the data files, you can contact the package author Steven J.
Pierce at pierces1@msu.edu. If you are a CSTAT employee assigned to the
project team, you can find the data files on CSTAT’s secure network
drive at `P:\Consulting\Cases_1600-1799\C1788\Data`. When you get the
files, you will need to put them all in the `scripts/extdata/` subfolder
of your local repository.

Members of our research team should not distribute the data files to
other parties outside the research team without Dr. Dontje’s approval.
They should not put them on servers not controlled or approved for use
by MSU without her approval either.

The PI will decide later whether to add the data to the repository or
archive them separately for reproducibility purposes.

Once you have completed this step and all the others listed above, you
should be ready to use this package to reproduce our results.

## Loading the *SANETPA* Package in R

After it has been installed to your package library as described above,
you can load *SANETPA* via the following R console command. That
provides access to the custom R functions we have included in the
package.

``` r
library(SANETPA)
```

Loading the package will also mean that we can use functions like
`devtools::session_info()` to show the package version number in our
output. That facilitates reproducibility by making it easier to see the
software environment required to obtain a particular result.

## Get Help on *SANETPA* Custom Functions

You can see information about the package by using the following command
in the R console. The resulting help page has an Index link at the
bottom that will show you a list of all the custom functions in the
package.

``` r
?SANETPA
```

## Reproducing Our Results

One of the main uses of the package is to run scripts that import,
manage, and analyze data for the manuscript it supports. If you want to
reproduce the results, you can double-click the `SANETPA.Rproj` file
from Windows Explorer to open the project in RStudio. Rendering a Quarto
script:

- May read external data files from the `scripts/extdata/` folder.
- May write R data files to the `data/` folder.
- Will generate output files in the `scripts/output/` folder.

Scripts in this package can generate either draft or production output.
I wrote a [blog
post](https://sjpierce.github.io/posts/output/draft_vs_production.html)
describing a rationale for, and approach to, separating draft and
production output. That approach has been implemented in this
compendium.

### Draft Output

You can get draft output by rendering a script with its default
parameters. Just use RStudio to open the relevant Quarto script (e.g.,
`scripts/Import_Data.qmd`) and then click the “Render” button in
RStudio. This is most useful to collaborators on our research team while
we’re developing the compendium before publication of the associated
paper. This allows us to focus on one script at a time. We tend to edit
and render draft output frequently as we do so, overwriting the draft
output each time to avoid creating too much file clutter.

### Production Output

Our final results for publication will be generated as production
output. The production process requires rendering each of the main
scripts in a specific order. We automated that process via the
`scripts/Production_Run.qmd` script. Use RStudio to open that file and
then click the “Render” button. If you have everything set up correctly,
that will create date-stamped output files in the `scripts/output/`
folder, plus the file `scripts/output/Production_Run.html`. The latter
file contains a data flow diagram showing all the inputs and outputs of
the production process, how long it took to render each script called by
the production script, and information about the software environment
used.

## References

<div id="refs" class="references csl-bib-body hanging-indent"
entry-spacing="0" line-spacing="2">

<div id="ref-Allaire-RN8427" class="csl-entry">

Allaire, J. J., Dervieux, C., Scheidegger, C., Teague, C., & Xie, Y.
(2025). *Quarto* (Version 1.7.32) \[Computer Program\]. Posit Software,
PBC. <https://quarto.org>

</div>

<div id="ref-Bryan-RN3900" class="csl-entry">

Bryan, J. (2018). Excuse me, do you have a moment to talk about version
control? *The American Statistician*, *72*(1), 20–27.
<https://doi.org/10.1080/00031305.2017.1399928>

</div>

<div id="ref-Bryan-RN3908" class="csl-entry">

Bryan, J., TAs, T. S. 545., & Hester, J. (n.d.). *Happy Git and GitHub
for the useR* \[Web Page\]. <https://happygitwithr.com>

</div>

<div id="ref-Chacon-RN3480" class="csl-entry">

Chacon, S., & Straub, B. (2014). *Pro Git*. Apress Media.
<https://git-scm.com/book/en/v2>

</div>

<div id="ref-Dontje-RN8757" class="csl-entry">

Dontje, K., & Campbell, R. (07/01/2021–06/30/2025). *Increasing access,
recruitment, and retention of sexual assault nurse examiners in rural
michigan* (Grant No. T96HP42059). Health Resources and Services
Administration.

</div>

<div id="ref-Mair-RN3387" class="csl-entry">

Mair, P. (2016). Thou shalt be reproducible! A technology perspective.
*Frontiers in Psychology*, *7*(1079), 1–17.
<https://doi.org/10.3389/fpsyg.2016.01079>

</div>

<div id="ref-Marwick-RN3899" class="csl-entry">

Marwick, B., Boettiger, C., & Mullen, L. (2018). Packaging data
analytical work reproducibly using R (and friends). *The American
Statistician*, *72*(1), 80–88.
<https://doi.org/10.1080/00031305.2017.1375986>

</div>

<div id="ref-Perez-Riverol-RN3924" class="csl-entry">

Perez-Riverol, Y., Gatto, L., Wang, R., Sachsenberg, T., Uszkoreit, J.,
Leprevost, F. da V., Fufezan, C., Ternent, T., Eglen, S. J., Katz, D.
S., Pollard, T. J., Konovalov, A., Flight, R. M., Blin, K., & Vizcaíno,
J. A. (2016). Ten simple rules for taking advantage of Git and GitHub.
*PLOS Computational Biology*, *12*(7), e1004947.
<https://doi.org/10.1371/journal.pcbi.1004947>

</div>

<div id="ref-Pierce-RN8756" class="csl-entry">

Pierce, S. J. (2025). *SANETPA: Research compendium for a study of
sexual assault nurse examiner training program attrition* (Version
0.14.0) \[Reproducible Research Materials and Computer Program, R
package, Private Repository Until Release\]. GitHub.
<https://github.com/sjpierce/SANETPA>

</div>

<div id="ref-R-Devel-Core-RN8182" class="csl-entry">

R Development Core Team. (2025). *R: A language and environment for
statistical computing* (Version 4.5.1) \[Computer Program\]. R
Foundation for Statistical Computing. <http://www.R-project.org>

</div>

<div id="ref-RStudio-Team-RN8351" class="csl-entry">

RStudio Team. (2025). *RStudio Desktop: Integrated development
environment for R* (Version 2025.05.1+513) \[Computer Program\]. Posit
Software, PBC. <https://posit.co>

</div>

<div id="ref-Torvalds-RN3929" class="csl-entry">

Torvalds, L., Hamano, J. C., & other contributors to the Git Project.
(2025). *Git for Windows* (Version 2.50.0(1)) \[Computer Program\].
Software Freedom Conservancy. <https://git-scm.com>

</div>

<div id="ref-Wickham-RN3898" class="csl-entry">

Wickham, H., & Bryan, J. (2021). *R packages: Organize, test, document,
and share your code*. O’Reilly Media. <https://r-pkgs.org>

</div>

</div>

## Citing This Package

Please cite the package itself (Pierce, 2025), plus any associated data
files.

## Disclaimer

The opinions or points of view expressed in this document (or any other
document included in this R package and repository) are solely those of
the authors and do not reflect the official positions of any
organization.
