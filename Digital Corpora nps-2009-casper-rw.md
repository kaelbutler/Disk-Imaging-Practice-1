# Digital Corpora — nps-2009-casper-rw

## Executive summary
Using Autopsy 4.22.1 I examined the provided casper-rw images. Key findings:
- The system appears to be Ubuntu 8.10 (Intrepid Ibex) — i386.
- Two accounts were present: Avahi (UID 110) and Ubuntu (UID 0).
- The user browsed ~414 unique websites including government domains (example: whitehouse.gov, sanjuan.fbi.gov).
- There are >60 images with EXIF metadata indicating Nikon and Canon devices.
- Eight Google searches were recovered.

This report summarizes methods, artifacts, evidence, and recommendations for further analysis and preservation.

## Images (evidence files)
| Image filename | MD5 checksum |
|---|---|
| ubnist.casper-rw.gen0.EO1 | 761c3476a18a87699b6b9776433d198d |
| ubnist.casper-rw.gen1.EO1 | 23a69347098ca4e611d3c9970dbed449 |
| ubnist.casper-rw.gen2.EO1 | eaf3e9d7c06ca14a52d165cd89d1282e |
| ubnist.casper-rw.gen3.EO1 | 717f6be298748ee7d6ce3e4b9ed63459 |

(Consider renaming files to avoid spaces in filenames when adding to the repo: e.g., `Digital-Corpora_nps-2009-casper-rw.md`.)

## Environment / system
- Operating system: Ubuntu 8.10 (Intrepid Ibex), i386
- Analysis tool: Autopsy 4.22.1
- Notes: Include Autopsy export directories, timestamps, and hashes for any exported reports/CSV files for chain-of-custody.

## Methodology
1. Mounted/ingested EO1 images in Autopsy 4.22.1.
2. Performed:
   - Keyword/search index analysis
   - Browser history and cache extraction
   - File system metadata and EXIF extraction for images
3. Exported search results, timeline snapshots, and EXIF tables to CSV (record exact export paths and checksums).

(If you ran any sleuthkit/command-line tools or recovery steps, list exact commands and timestamps here.)

## Accounts & system artifacts
- Accounts discovered:
  - Avahi (UID: 110)
  - Ubuntu (UID: 0)
- Notable system artifacts to preserve:
  - /home/* browser profiles (history, bookmarks)
  - /var/log/ (system logs)
  - ~/.cache and /tmp if relevant for browser cache or downloaded items

## Browsing activity
- Unique websites visited: 414 (includes government domains: whitehouse.gov, sanjuan.fbi.gov)
- Recovered search history: 8 Google searches (see Evidence: Search History)
- Recommendation: export the full list of visited URLs and the exact timestamps (Autopsy timeline view or browser history CSV).

## Images & EXIF summary
- Over 60 photos recovered.
- Camera makes found: Nikon, Canon.
- Recommended exports:
  - EXIF table including: filename, DateTimeOriginal, Make, Model, GPS (if present), file path, hash.
  - Group by camera model and date to form a timeline of photographic activity.

## Evidence (screenshots)
- Screenshot: `Screenshot 2026-06-29 141928.png` — Search history evidence (replace spaces in filename or URL-encode).
- Screenshot: `Screenshot 2026-06-29 142333.png` — Image metadata evidence.

(Recommendation: avoid spaces in screenshot filenames in the repository; use hyphens or underscores and reference them correctly in Markdown: `![Search History](./Screenshot-2026-06-29-141928.png)`).

## Recommendations & next steps
1. Preserve exported CSV/JSON files and generate MD5/SHA256 checksums for each export (store checksums in a checksums.txt).
2. Export detailed browser history (including timestamps) and top visited domains.
3. Produce an EXIF CSV for all images and map photos by timestamp/GPS to build a timeline/location map (if GPS exists).
4. If forensic case: record chain-of-custody for the EO1 images and the Autopsy workstation images (hashes, who handled, when).
5. Consider deeper analysis for:
   - Recovered deleted files
   - Downloads folder and attachment examination
   - Correlation between browsing history timestamps and photo timestamps

## Appendix: reproducibility & notes
- Tools used: Autopsy 4.22.1 (include plugin names if used).
- Data exports: list folder paths and filenames of exported reports (e.g., `exports/browser_history.csv`, `exports/exif_report.csv`) and provide their checksums.
- Change log:
  - Initial analysis by [analyst name or initials], 2026-06-29.
