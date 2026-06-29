# Digital Corpora — nps-2009-casper-rw

> NOTE: I included some assertions in the original report that may be incorrect. I have removed or marked specific claims that need your confirmation. Please review the [CONFIRM] items and tell me what to replace them with; I can update the file again.

## Executive summary
Using Autopsy 4.22.1 I examined the provided casper-rw images. Key findings (please confirm the items marked [CONFIRM]):
- The system appears to be Ubuntu 8.10 (Intrepid Ibex) — i386. [CONFIRM]
- Accounts discovered: Avahi (UID 110) and Ubuntu (UID 0). [CONFIRM]
- Browsing activity: ~414 unique websites were reported previously — please confirm this number or supply the correct count. [CONFIRM]
- Images: photos were identified during analysis; EXIF metadata export was not performed in this report. [CONFIRM]
- Google searches recovered: 8 (please confirm). [CONFIRM]

This report summarizes methods, artifacts, evidence, and recommendations for further analysis and preservation.

## Images (evidence files)
| Image filename | MD5 checksum |
|---|---|
| ubnist.casper-rw.gen0.EO1 | 761c3476a18a87699b6b9776433d198d |
| ubnist.casper-rw.gen1.EO1 | 23a69347098ca4e611d3c9970dbed449 |
| ubnist.casper-rw.gen2.EO1 | eaf3e9d7c06ca14a52d165cd89d1282e |
| ubnist.casper-rw.gen3.EO1 | 717f6be298748ee7d6ce3e4b9ed63459 |

(Recommendation applied: avoid spaces in filenames when adding to the repo. Suggested filename: `Digital-Corpora_nps-2009-casper-rw.md`.)

## Environment / system
- Operating system: Ubuntu 8.10 (Intrepid Ibex), i386. [CONFIRM]
- Analysis tool: Autopsy 4.22.1
- Notes: Include Autopsy export directories, timestamps, and hashes for any exported reports/CSV files for chain-of-custody.

## Methodology
1. Mounted/ingested EO1 images in Autopsy 4.22.1.
2. Performed:
   - Keyword/search index analysis (as applicable).
   - Browser history and cache examination (as applicable).
   - File system metadata review.
3. Exported search results and other reports to CSV/HTML as applicable (record exact export paths and checksums).

(If you ran any command-line tools or recovery steps, list exact commands and timestamps here.)

## Accounts & system artifacts
- Accounts discovered (please confirm):
  - Avahi (UID: 110) [CONFIRM]
  - Ubuntu (UID: 0) [CONFIRM]
- Notable system artifacts to preserve (adjusted to what exists in the image):
  - Browser profiles and history (if present in the image; note: this image did not contain a `/home/` directory).
  - `/var/log/` (system logs) — if present.
  - Relevant caches or temporary directories (only if they exist in the image).

## Browsing activity
- Unique websites visited: (please confirm count) [CONFIRM]
- Recovered search history: (please confirm number of searches recovered) [CONFIRM]
- Recommendation: export the full list of visited URLs and the exact timestamps if browser history artifacts are present.

## Images & EXIF summary
- Photos were identified during analysis; an EXIF CSV was not produced as part of this report. If you want an EXIF export, specify and I will add recommended fields (filename, DateTimeOriginal, Make, Model, GPS, file path, hash) and can produce the CSV.

## Evidence (screenshots)
- Screenshot: `Screenshot-2026-06-29-141928.png` — Search history evidence (renamed to avoid spaces).
- Screenshot: `Screenshot-2026-06-29-142333.png` — Image metadata evidence (renamed to avoid spaces).

(Recommendation applied: avoid spaces in screenshot filenames in the repository; use hyphens or underscores and reference them correctly in Markdown: `![Search History](./Screenshot-2026-06-29-141928.png)`).

## Recommendations & next steps
1. Preserve exported CSV/JSON files and generate MD5/SHA256 checksums for each export (store checksums in a `checksums.txt`).
2. Export detailed browser history (including timestamps) and top visited domains if browser artifacts exist.
3. If desired, produce an EXIF CSV for any recovered images and map photos by timestamp/GPS to build a timeline/location map (if GPS exists).
4. If this is a forensic case: record chain-of-custody for the EO1 images and the Autopsy workstation images (hashes, who handled, when).
5. Consider deeper analysis for:
   - Recovered deleted files (if recovery was attempted).
   - Downloads folder and attachment examination (if present).
   - Correlation between browsing history timestamps and photo timestamps (if both are available).

## Appendix: reproducibility & notes
- Tools used: Autopsy 4.22.1 (include plugin names if used).
- Data exports: list folder paths and filenames of exported reports (e.g., `exports/browser_history.csv`) and provide their checksums.
- Change log:
  - Initial analysis by [analyst name or initials], 2026-06-29.
