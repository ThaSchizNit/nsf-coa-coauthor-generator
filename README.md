# NSF COA Co-Author Generator (PubMed)

Automatically extracts your co-authors from PubMed publications (last 48 months) and formats them perfectly for **Table 4** of the NSF Collaborators and Other Affiliations (COA) template.

### Features
- Pulls co-authors and full affiliations directly from PubMed XML
- Removes initials (NSF does not require them in the name field)
- Preserves **all commas** in affiliations (no chopping!)
- Outputs a clean tab-separated (.tsv) file ready for Excel copy-paste
- Runs 100% in Google Colab — no software installation needed
- Uses pipe (`|`) delimiter to safely handle commas in affiliation text
- Licensed under **MIT** — free to use, modify, and share

### How to Use (takes ~2–5 minutes)
1. Click the button to open the notebook in Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]([https://colab.research.google.com/github/ThaSchizNit/nsf-coa-coauthor-generator/blob/main/NSF_COA_PubMed_CoAuthors.ipynb](https://colab.research.google.com/drive/1IYdDzzJQCYBIzHBk6S984x3OkVKOTfBq?usp=sharing)

2. **Make a copy** so you can edit:  
   File → Save a copy in Drive

3. In **Cell 3** (labeled `# EDIT THESE:`), update:
   ```python
   author_name = "YourLastName Initials"     # e.g., "Schisler JC" or "Smith AB"
   your_email = "your.email@institution.edu" # REQUIRED by NCBI/PubMed
- If few/no results, try variations like "LastName J" or full "LastName, First M".

4. Run the cells top-to-bottom:
- Cell 1: installs Biopython (only once)
- Cell 2: defines the function (no edit needed)
- Cell 3: runs your search (wait 1–5 min)
- Cell 4: generates preview + downloads coa_coauthors.tsv

5. Open the downloaded coa_coauthors.tsv in Excel:
- Select columns A:C (Marker, Name, Organizational Affiliation)
- Copy → paste directly into your NSF COA Excel template (Table 4 section, usually starting around row 52)

### Example Output Preview
This is what the TSV looks like when opened in Excel (or previewed in the notebook):

| Marker | Name                | Organizational Affiliation                                                                 |
| :----- | :------------------ | :----------------------------------------------------------------------------------------- |
| A:     | Adkins, Joshua N    | Biological Science Division, Pacific Northwest National Laboratory, Richland, WA 99354.   |
| A:     | Afolayan, Adeleye J | Department of Pediatrics, Children's Research Institute and Cardiovascular Research Center, Medical College of Wisconsin, Milwaukee, WI 53226, USA. |
| A:     | Albrecht, Lars A    | University of North Carolina McAllister Heart Institute, Chapel Hill, NC.                  |
| A:     | Allen, Noah         | Department of Biomedical Engineering, Rensselaer Polytechnic Institute, Troy, NY, USA.     |
| A:     | Beheshti, Afshin    | COVID-19 International Research Team.                                                      |

(Note: Full affiliations are preserved with all commas; "Unknown" appears only if PubMed lacks affiliation data.)

License
MIT License — see LICENSE for full text.
You are free to use, modify, distribute, and incorporate this tool in your own work.

Feedback / Issues
Found a bug? Missing co-authors? Want a version for Google Scholar backup?
→ Open an issue here or reply on X: @NitDawg

Happy NSF proposing! 🚀
— Jonathan C. Schisler (Chapel Hill, NC)

Last updated: January 2026
