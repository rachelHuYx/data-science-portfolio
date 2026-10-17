# HU JIAYI — Data Science Portfolio

A personal learning portfolio for **CISC7204**, by **HU JIAYI**. It presents one completed exploratory analysis and the methods, findings, limitations, and next questions behind it.

- Portfolio repository: [rachelHuYx/data-science-portfolio](https://github.com/rachelHuYx/data-science-portfolio)
- Live GitHub Pages website: [rachelHuYx.github.io/data-science-portfolio](https://rachelHuYx.github.io/data-science-portfolio/)
- Analysis repository: [rachelHuYx/data-science-project](https://github.com/rachelHuYx/data-science-project)

Published with GitHub Pages from **`main` / `/ (root)`**. The public home page, both figures, project links, and mobile/desktop layouts were verified in Google Chrome on 17 October 2026. Public chart images match the analysis outputs. Classmate review and any resulting improvement are separate next steps.

## Website entry point

**`index.md` at the repository root is the website entry point.** Its YAML front matter selects `_layouts/default.html`; GitHub Pages uses Jekyll to render it as the home page. All local asset paths use Liquid's `relative_url` filter so that they work under `/data-science-portfolio`.

```text
index.md                        Website home page and project narrative
_config.yml                     Jekyll settings and GitHub Pages base URL
_layouts/default.html           Accessible page shell and navigation
assets/css/style.css            Responsive styling
assets/images/annual_reports.png
assets/images/date_consistency.png
```

## Publish from `main` / root

1. Push this source and both chart images to the **`main`** branch of `rachelHuYx/data-science-portfolio`.
2. Open the repository's **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch** as the source.
4. Select branch **`main`** and folder **`/ (root)`**, then save.
5. Wait for the GitHub Pages build/deployment to succeed. Open the website address reported in Pages settings and check the home page, both figures, navigation, and project link.

Keep `index.md` at the root. Do not add `.nojekyll`, because this site needs Jekyll to process the layout and Liquid asset paths. If the repository name changes, update `baseurl` in `_config.yml` to match.

## Featured analysis

**Poaching Reports: Dates Before Conclusions** asks:

> How do recorded poaching reports vary over time, and how consistent is their date metadata?

The course-provided CSV contains **268 records** with report dates in **2005–2015**. Of these, **167 (62.3%)** have `created_date` earlier than `date_report`; 19 have the same calendar date and 82 have a later creation date. Date-field definitions need investigation before interpreting that order as an error.

Annual totals describe recorded reports, **not actual poaching incidence or rates**. The latest observed report date in 2015 is 7 September; full-year coverage is unverified. Patrol effort and a population denominator are unavailable. No causal explanation is claimed.

## Data handling

Redistribution permission for the original course CSV has not been confirmed. The public portfolio includes aggregate chart images and summary counts only. Do not add the source CSV, individual records, or raw coordinates to this repository. The linked analysis repository documents the workflow and how to supply the course data locally.

## Accessibility and design

The site uses semantic landmarks, a keyboard skip link, visible focus states, meaningful figure descriptions, and expandable tables containing the chart values. It adapts to small screens and does not require JavaScript, external fonts, or a theme dependency.
