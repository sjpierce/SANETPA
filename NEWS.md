# SANETPA News 

## 0.17.0
* `README.qmd` and `README.md`
    * Added example terminal command for getting date-stamped production run 
      output. 
    * Updated software version info & citations.
* `SANETPA.Rproj`
    * Switched from XeLaTex to LuaLaTeX due to Quarto verion upgrade.
* `graphics/Combomark-Horiz_Pantone-567.pdf`
    * Added PDF version of logo to avoid epstopdf conversion issue.
* `scripts/.gitignore`
    * Omit python Jupyter notebook files.
* `scripts/_quarto.yml`
    * Updated rendering key to include RQ4 script.
* `scripts/Descriptive_Analyses.qmd`
    * Switched to using PDF version of logo file.
* `scripts/Import_Data.qmd`
    * Switched to using PDF version of logo file.
* `scripts/RQ1_Analyses.qmd`
    * Switched to using PDF version of logo file.
* `scripts/RQ2_RQ3_SR_Models.qmd`
    * Switched to using PDF version of logo file.
    * Updated package loading, replace emmeans w/ marginaleffects. Fix line 
      breaks.
    * Switched to marginaleffects instead of emmeans to get EMMs. Add risk 
      differences.
* `scripts/RQ4_Analyses.qmd`
    * Added file.
* `scripts/Production_Run.qmd`
    * Updated workflow diagram. 
    * Added chunk to run RQ1 script.  
    * Updated chunk to run RQ2 and RQ3 script.
    * Updated Software Information section to omit name of the output file. 
    * Use quarto_render(..., quarto_args = c('--output', OutFile)) to control 
      output file names. 
    * Added chunk to run RQ4 script. 
* `scripts/references.bib`
    * Added new methods reference. 
    * Updated software version info & citations.

## 0.16.0
* `.Rbuildignore`
    * Ignore the `graphics/` folder when installing package. 
* `DESCRIPTION`
    * Update the Suggests field to include effectsize package. 
    * Moved piercer from Depends to Suggests field to solve a note from 
      devtools::check(), updated piercer version number.
* `README.qmd` and `README.md`
    * Update software version & citation info.
    * Add research questions. 
* `scripts/_quarto.yml`
    * Update Render key to refer to `scripts/RQ1_Analyses.qmd`
    * Update Render key to refer to `scripts/RQ2_RQ3_SR_Models.qmd`
* `scripts/Descriptive_Analyses.qmd`
    * Update to reflect revised imported data file. 
    * Improve narrative text.
    * Removed eligibility rate (which is now in RQ1 analyses script).
    * Updated to reflect change from analyzing eligible applicants to analyzing 
      enrolled applicants (consistent with SR models for RQ2 and RQ3). 
* `scripts/Import_Data.qmd`
    * Update Stage_Reached coding.
    * Improve narrative text. 
    * Revise Eligible Applicants section.
    * Add Enrolled Applicants section.
    * Add value labels to Enrolled variable.
    * Update stage diagram.
    * Update creation of Thresholds data. 
    * Update table on size of datasets.
    * Update data saved out. 
    * Updated value labels for variables about starting/finishing DT modules. 
    * Add code to create and save `StartedDT_Applicants` dataset.
* `scripts/references.bib`
    * Updated software version and citation data. 
    * Add methods references. 
* `scripts/RQ1_Analyses.qmd`
    * Added draft of file. 
    * Load more R packages. 
    * Convert categorical variables to factors.
    * Create a temporary dataset called Overall.
    * Improved the Methods section.
    * Update the Results section.
* `scripts/SR_Model.qmd`
    * Updated Purpose section to reflect revised research questions.
    * Updated Research Questions section.
* Renamed `scripts/SR_Model.qmd` to `scripts/RQ2_RQ3_SR_Models.qmd`.
*  `scripts/RQ2_RQ3_SR_Models.qmd`
    * Updated YAML header, including title, left header, default parameter 
      values, and default output-file value.
    * Add objects to store sample sizes. 
    * Update table of dataset sizes.
    * Update stage diagram.
    * Improved the Methods section.
    * Changed order of predictors in Models 2 and 3 to better match RQ3 wording. 
    * Added callout about Model 2 vs Model 4.
    * Added module start and finish rates. 
    * Updated Conclusions section.
    * Moved creation of `StartedDT_Applicants` to import script. 
    * Improve narrative text.
    * Add methods text about DT module start and finish variables.
    * Improve figure formatting and captions.
    * Improve Conclusions section, add Recommendations section.
    
## 0.15.0
* `DESCRIPTION`
    * Updated Depends field to require piercer 0.21.0.
* `README.qmd` and `README.md`
    * Update software version & citation info.
* `scripts/Descriptive_Analyses.qmd`
    * Use new piercer::file_details() function.
    * Replaced Barrier_TD with Barrier_WR and Barrier_FO variables. 
    * Improve code readability.
    * Update explanatory text about measuring barriers construct.
    * Fix a table formatting issue. 
    * Improve narrative text.
* `scripts/Import_Data.qmd`
    * Use new piercer::file_details() function.
    * Improve narrative text. 
    * Revised recoding of Stage_Raw to Stage_Reached. 
    * Updated stage diagram to match revised Stage_Reached variable.
    * Updated creation of Thresholds dataset to match revised Stage_Reached 
      variable. 
    * Replaced Barrier_TD with Barrier_WR and Barrier_FO variables. 
    * Update missingness assessments to reflect new variables. 
    * Update Eligible_Applicants_CD and Thresholds datasets with new variables.
    * Resize fig-Stages and refine its labeling.
    * Fix value labels for thresholds.
* `scripts/SR_Model.qmd`
    * Use new piercer::file_details() function.
    * Switch to using new piercer::display_num() function instead of defining it 
      in this script. 
    * Resize fig-Stages and refine its labeling.
    * Improve narrative text. 
    * Removed research questions we will no longer pursue. 
    * Updated to reflect revised set of focal predictors.
    * Improved table and figure labeling. 
    * Improve table and figure captions. 
    * Switch to black & white theme for figures. 
    * Improve table footnotes.
    * Add random number seed parameters for DHARMa model diagnostics 
      simulations.
    * Load more R packages.
    * Add methods details about software and model diagnostics. 
    * Add model diagnostics output. 
* `scripts/references.bib`
    * Updated software version and citation data. 
    * Added several more methods references. 

## 0.14.0
* `DESCRIPTION`
    * Updated Suggests field to list packages used in various scripts. 
* `README.qmd` and `README.md`
    * Update software version & citation info.
* `scripts/_quarto.yml`
    * Update render key to use new file name for modeling script.
* `scripts/Descriptive_Analyses.qmd`
    * Reduce size of text in code chunks.
* `scripts/Import_Data.qmd`
    * Reduce size of text in code chunks.
* `scripts/Production_Run.qmd`
    * Updated workflow diagram. 
    * Updated chunk for running modeling script.
* `scripts/SR_Model.qmd`
    * Fixed a table format. 
    * Improve research question wording.
    * Improve callout and narrative text.
    * Add emmeans plot for Model 1.
    * Remove model fitting code that is now located elsewhere in script.
    * Add FloatBarriers to control layout. 
    * Add emmeans for Model 2 and Model 4. 
    * Fix spelling.
    * Add callout about Model 3.
    * Fix headings, table captions, and table footnotes.
    * Fixed a table format. 
    * Fix figure caption and size. 
    * Add Model 5 output.
    * Add conclusions section.
    * Reduce size of text in code chunks.
* `scripts/references.bib`
    * Updated software version and citation data. 
    
## 0.13.0
* `README.qmd` and `README.md`
    * Update software version & citation info.
* Renamed `scripts/CR_Model.qmd` to `scripts/SR_Model.qmd`. 
* `scripts/Descriptive_Analyses.qmd`
    * Expanded section on reliability of Barrier_TD.
    * Updated axis for histogram of Barrier_TD.
    * Improve narrative text. 
    * Add a table of stage distribution after listwise deletion.
    * Add a callout about only doing reliability analysis with data before 
      listwise deletion.
    * Add a table for continuous predictor descriptives after listwise deletion.
    * Update figures to use data after listwise deletion.
    * Update correlation table to use data after listwise deletion.
    * Update categorical predictor distributions to use data after listwise 
      deletion.
    * Update Threshold contingency table title. 
    * Add callout showing Thresholds data already reflect listwise deletion. 
* `scripts/Import_Data.qmd`
    * Updated Barrier_TD scale score.
    * Update comments about loaded packages. 
    * Filtered Eligible_Applicants dataset to creates Eligible_Applicants_CD by 
      using listwise deletion of cases with missing data on variables required 
      for modeling. 
    * Updated T1 to T4 and Thresholds dataset to hold only variables required 
      for modeling.
    * Updated Dataset Sizes table. 
    * Now saves out Eligible_Applicants_CD dataset too.
    * Add centered variables to Thresholds dataset. 
    * Convert categorical predictors to factors. 
    * Improve narrative text. 
* `scripts/references.bib`
    * Updated software version and citation data. 
    * Added references for methods papers. 
* `scripts/SR_Model.qmd`
    * Updated title left header, filename parameters, and default output 
      filename.
    * Improve narrative text. 
    * Improve research questions. 
    * Update headings. 
    * Load more R packages. 
    * Define a display_num() function.
    * Update table of dataset sizes. 
    * Remove Prepare Data section (workl is now done in import script).
    * Update Model 1 analysis. 
    * Update Model 2 analysis. 
    * Update Model 3 analysis. 
    * Add Model 4 analysis. 
    
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
