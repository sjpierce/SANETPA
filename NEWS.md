# SANETPA News 

## 0.12.0
* `README.qmd` and `README.md`
    * Update software version & citation info.
* `scripts/Descriptive_Analyses.qmd`
    * Update list of R packages loaded.
    * Improve narrative text and headings. 
    * Add more crosstab output.
    * Assess reliability of Barrier_TD scale. 
    * Examine predictor distributions.
* `scripts/Import_Data.qmd`
    * Compute a Barrier_TD scale score.
    * Compute centered scale scores for potential predictors. 
* `scripts/references.bib`
    * Updated software version and citation data. 
    * Add a reference for ProQOL manual.


## 0.11.0
* `README.qmd` and `README.md`
    * Update software version & citation info.
* `scripts/Import_Data.qmd`
    * Recode practicset_dem_num into Setting & combine Rural and Tribal 
      categories along the way.
* `scripts/Descriptive_Analyses.qmd`
    * Update to show original vs recoded setting frequency distributions. 
* `scripts/references.bib`
    * Updated software version and citation data. 

## 0.10.0, 2025-06-13
* `scripts/CR_Model.qmd`
    * Load more R packages. 
    * Enable load-data chunk, add tables about the data file and datasets it 
      contains.
    * Improve narrative text. 
    * Add Prepare Data section.
    * Add Results section, with initial draft of Model 1. 
    * Add subsections for Models 2 and 3 as placeholders. 
* `scripts/Descriptive_Analyses.qmd`
    * Add a frequency table for setting. 
    * Improve narrative text. 
* `scripts/Import_Data.qmd`
    * Update comments about R packages loaded.
    * Improve headings. 
* `scripts/Production_Run.qmd`
    * Improved narrative text. 
    * Enabled chunks for import & modeling scripts. 
    * Add chunk for descriptive analyses script.
    * Updated data flow diagram. 
    * Add a callout about pending tasks. 
* `scripts/references.bib`
    * Updated software version and citation data. 

## 0.9.0, 2025-06-11
* `scripts/_quarto.yml`
    *  Updated render key list of scripts.
* `scripts/CR_Model.qmd`
    * Improve narrative text and add stage diagram.
* `scripts/Descriptive_Analyses.qmd`
    * Added table footnote.
* `scripts/Import_Data.qmd`
    * Improve narrative text. 
* `scripts/references.bib`
    * Added references. 

## 0.8.0, 2025-06-06
* `scripts/Descriptive_Analyses.qmd`
    * Added file. 
    * Improved table content, formatting, & footnote.
    * Added more tables. 
    * Improved narrative text.
    * Added stage/threshold figure.
* `scripts/Import_Data.qmd`
    * Improve table formatting.
    * Improve narrative text. 
    * Stopped saving out `Aplpicants_Raw` dataset. 
    * Add some value labels.
    * Updated source data file. 
    * Add value labels to `Thresholds` dataset. 

## 0.7.0, 2025-05-28
* `scripts/Import_Data.qmd`
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
* `scripts/Import_Data.qmd`
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
