## Deposit Policy

To submit a data proposal to VaxStats, follow these steps:
1. Prepare your data for deposit. 
- If needed, convert your data to an appropriate file format. For help converting data in PDFs to tabular formats, see the Tabula tutorial below, as well as some guidance on R and Python tools to try.
2. Ensure that your data is complete, correct, and well-documented. The most useful datasets also have:
- Data descriptions
- Data dictionaries
- Data collection summaries and instrumentation information (if applicable)
- Any associated publications 
- Any other information that could help contextualize the data for reuse
3. Submit your data and all accompanying documentation, along with the following:
- Data creator contact information
- All required metadata fields (read more in our metadata profile)
- Approval for the data to be licensed CC-0 or CC-BY, or some other license as discussed with the VaxStats team
- Certification of de-identification 

### File-Formatting Tips
The recommended naming convention for VaxStats submissions is: 
- `Year_State_Description_LevelofDivision.csv` (ex: `2015_Oregon_RatesAdol_county.csv`)

Other best practices for file naming:
- Use consistent, brief, and descriptive naming convention for all files.
- Avoid spaces and special characters (ex: * # % \ / :  ? “ < > | [ ] & $ , . )
- Use three-letter file extensions to ensure backwards compatibility (ex: .csv, .txt, etc)
- Do not rely on letter case for identifying different files (ex: datasetA.txt, dataseta.txt)
- Adapted from the University of Washington Libraries [Data Management Guide](http://guides.lib.uw.edu/research/dmg/orgformat)

### Clean Data Tips
- Avoid special characters such as commas in numerical values (ex: 1000✓ vs 1,000 ✗ or 99.9✓ vs 99.9% ✗).
- Each variable should form a column and each observation should form a row, per tidy data principles.
- Make sure to store only one value per unit.
- Create separate files for different types of observations (ex: separate files for data separated by county and data separated by school district).
- Use descriptive and interpretable headers in only the first line of the table.
- Only include data values and header in data files and provide extra information (ex: source, footnotes, background) in a separate README file (.txt or .md).
Ex: 

| County | Reported_enrollment | Percent_immunized |
| --- | --- | --- |
| Adams | 1200 | 80.0 |
| Clark | 99 | 55.6 |

## Converting Documents to Machine-Readable Formats
If you need to convert data housed in PDF to CSV (or some other machine-readable format), [Tabula](https://github.com/tabulapdf/tabula), which is open-source, may be useful. To assist our VaxStats users, we’ve created the following tutorial on Tabula. 

### Tabula Tutorial
1. Install from https://tabula.technology/
2. Open the application; the application will open in your browser.
3. Under ‘Import one or more PDFs,’ click ‘Browse’ to choose a PDF from your computer to import.
4. Once you’ve selected a PDF, click ‘Import.’
5. Select the part of the PDF you want to convert to a table. Click and drag until the entire table is selected; it should show up shaded red. You can also use the ‘Autodetect Tables’ which will detect all the tables in the PDF.
6. Click ‘Preview & Export Extracted Data.’
7. Preview the extracted data. If it’s not accurate, click ‘<-- Revise Selections.’
- Note 1: Tabula will only recognize horizontal text. If your PDF has vertical text, select as much of the table that does not have vertical text and export it to a .csv file. Then open the file, in either a text editor or spreadsheet software, and add in the vertical headings by hand.
- Note 2: Headings or Data that is broken into two lines within one box may not be detected correctly and could be broken into multiple rows with blank boxes. Tabula has a “Choose Alternate Extraction Method” option on the left hand menu that allows you to choose between “Stream” or “Lattice.” Changing this option may help get rid of blank boxes and extra rows. If not, choose the best of the two options and adjust your table selection to get the most data possible. Then open the file, in either a text editor or spreadsheet software, and add in the missing data by hand. 
8. Once satisfied with the preview, choose desired export format, and click ‘Export.’

**Tabula Tips:**
- Crop the table as closely as possible on each edge without losing any data. The closer the crop, the more accurate the data export, usually.
- If you have a PDF with multiple tables in it, it may be easier to crop each table individually, and download each as a separate CSV.

### Alternative Methods for Converting PDF-locked Tables into Other File Formats
If Tabula isn’t proving sufficient, we’ve also provided links to data document conversion methods using R and Python.

**R: pdftools**
- R Documentation: https://ropensci.org/technotes/2018/12/14/pdftools-20/
- Sample code: https://gist.github.com/nniiicc/28488e7193277c7f0bc8feb07091a089

**Python: tabula-py**
Tabula-py may work for tables, but it does require Java to work.
- Documentation: https://github.com/chezou/tabula-py
