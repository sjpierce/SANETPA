# SANETPA News 

## 0.7.0, 2025-05-28
* `scripts/Import_data.qmd`
   * Renamed more variables. 
   * Add a table with variables names & labels for updated applicants data. 
   * Improve narrative text. 
   * Add comments about similar variables and crosstab showing how they handle 
     missing data differently. 
   * Rename variables.
   * Add variable and value labels.
   * Created Eligible_Applicants and Thresholds datasets. 
   * Added summary of dataset sizes.
   * Save out additional datasets.
   
## 0.6.0, 2025-05-18
* `DESCRIPTION` 
    * Updated Depends field to require R 4.5.
* `README.qmd` and `README.md`
    * Update software version & citation info.
* `scripts/Import_data.qmd`
    * Decreased default font size for code chunks.
    * Load more R packages. 
    * Improve headings and narrative text.
    * Add callout about raw data file.
    * Add table with meta-data about raw data file.
    * Add raw data file name and enable import chunk.
    * Update list of objects saved out and enable chunk for saving data.
    * Fix line breaks.
    * Rename variables. 
    * Add table with meta-data about imported data file.
    * Update Save Data section.
* `scripts/CR_Model.qmd`
    * Add narrative text. 
* `scripts/references.bib`
    * Updated software version & citation info. 
    * Added citations for papers on continuation ratio modeling.
    
## 0.5.0, 2025-04-26
* `.gitignore`
    * Omit Windows thumbnail files and MacOS .DS_Store files from Git tracking.
* `README.qmd` and `README.md`
    * Update software version & citation info.
    * Update Repository Structure section.
* `graphics/Combomark-Horiz_Green.png`
    * Added MSU Helmet/wordmark combination logo for use in HTML output. 
* `graphics/Combomark-Horiz_Pantone-567.eps`
    * Added MSU Helmet/wordmark combination logo for use in PDF output. 
* `scripts/CR_Model.qmd`
    * Updated subtitle (which will not display in PDF output).
    * Update author affiliation data. 
    * Changed output format to PDF per client preference. 
    * Add \FloatBarrier commands to keep tables/figures in their own sections. 
* `scripts/Import_Data.qmd`
    * Updated subtitle (which will not display in PDF output).
    * Update author affiliation data. 
    * Changed output format to PDF per client preference. 
    * Add \FloatBarrier commands to keep tables/figures in their own sections. 
* `scripts/Production_Run.qmd` 
    * Updated data flow diagram.
    * Updated to write PDF output for import and modeling scripts. 
* `scripts/references.bib`
    * Updated software version & citation info. 
* `scripts/title.tex`
    * Show each numbered author affiliation only once, with name, department, 
      and url.

## 0.4.0, 2025-04-23
* `README.qmd` and `README.md`
    * Update Reproducing Our Results section.
* `scripts/Production_Run.qmd`
    * Disable import script for now. 
    * Added Workflow section.
* `scripts/references.bib`
    * Updated software version & citation info. 
    * Improve narrative text. 

## 0.3.0, 2025-04-09
* `README.qmd` and `README.md`
    * Updated Quarto software version. 
    * Updated Repository Structure and Contents section. 
* `scripts/_quarto.yml` 
    * List additional scripts in the render key so that their output will 
      automatically be directed into `scripts/output` instead of remaining in 
      the folder where those script files are stored. 
* `scripts/CR_model.qmd`
    * Added initial draft skeleton for the file. 
* `scripts/Import_Data.qmd` 
    * Fixed default value for SourceFile parameter. 
    * Added default output file name. 
    * Improve narrative text. 
* `scripts/Production_Run.qmd`
    * Added initial draft skeleton for the file. 
* `scripts/references.bib`
    * Updated Quarto software version. 

## 0.2.0, 2025-04-02
* `README.qmd` and `README.md`
    * Improved introduction, cited sources, and updated repository contents 
      section. 
* `scripts/.gitignore` 
    * Added as part of configuring Quarto project. 
* `scripts/CSTAT_style.css`
    * Fixed path to logo file.
* `scripts/Import_Data.qmd`
    * Added first draft of import script. 
* `scripts/references.bib`
    * Added data for more references. 

## 0.1.0, 2025-04-01
* Configured repository as an R package.  
    * `data/Placeholder.txt`
    * `graphics/CSTAT_5x5_Transparent.png`
    * `logo_MSU_CSTAT.png`
    * `R/SANETPA-package.R`
    * `scripts/_brand.yml`
    * `scripts/_quarto.yml`
    * `scripts/CSTAT_style.css`
    * `scripts/CSTAT_theme.scss`
    * `scripts/references.bib`
    * `scripts/extdata/Placeholder.txt`
    * `scripts/output/Placeholder.txt`
    * `.gitignore`
    * `.Rbuildignore`
    * `DESCRIPTION`
    * `LICENSE`
    * `NAMESPACE`
    * `NEWS.md`
    * `README.qmd` and `README.md`
    * `SANETPA.Rproj`

## 0.0.0.9000, 2025-04-01
* Initial commit. 
