---
layout: default
title: HU JIAYI — Data Science Portfolio
description: A CISC7204 student portfolio exploring poaching report patterns and the consistency of their date metadata.
---

<section class="hero" id="about" aria-labelledby="intro-title">
  <div class="hero-copy">
    <p class="eyebrow"><span class="small-line" aria-hidden="true"></span> CISC7204 · Student portfolio</p>
    <h1 id="intro-title">Careful questions.<br>
<em>Clearer evidence.</em></h1>
    <p class="hero-intro">I'm <strong>HU JIAYI</strong>, a CISC7204 student learning to turn data into understandable, reproducible analysis.</p>
    <p class="hero-description">This portfolio documents what I explored, what the data can support, and which questions remain open.</p>
    <a class="text-link hero-link" href="#project">Explore the project <span aria-hidden="true">↓</span></a>
  </div>
  <aside class="field-note" aria-label="Portfolio focus">
    <span class="note-index">FIELD NOTES / 01</span>
    <div class="note-rule" aria-hidden="true"></div>
    <p class="note-title">A date is a data point.<br>
Its meaning needs checking.</p>
    <p class="note-body">The first project starts with recorded poaching reports—and a closer look at the dates behind them.</p>
    <div class="note-meta"><span class="status-dot" aria-hidden="true"></span> One completed exploratory analysis</div>
  </aside>
</section>

<section class="skills-strip" aria-labelledby="skills-title">
  <h2 id="skills-title">Tools I'm practising</h2>
  <ul>
    <li>Python</li>
    <li>Pandas</li>
    <li>Matplotlib</li>
    <li>Git &amp; GitHub</li>
    <li>Jupyter</li>
  </ul>
  <p>Cleaning tables, handling dates, making figures, and documenting a repeatable workflow.</p>
</section>

<article class="project" id="project" aria-labelledby="project-title">
  <header class="project-header">
    <div class="section-label"><span class="section-number">01</span><span>Selected project</span></div>
    <div class="project-heading">
      <p class="project-status"><span class="status-dot" aria-hidden="true"></span> Completed exploratory analysis</p>
      <h2 id="project-title">Poaching Reports:<br>
<em>Dates Before Conclusions</em></h2>
      <p class="project-deck">A small exploratory study of reporting patterns and date consistency, with an emphasis on what the records actually describe.</p>
      <div class="project-tags" aria-label="Project methods"><span>Exploratory data analysis</span><span>Date quality</span><span>Python</span></div>
    </div>
  </header>

  <section class="question-block" aria-labelledby="question-title">
    <p class="eyebrow" id="question-title">The research question</p>
    <p class="research-question">How do recorded poaching reports vary over time, and how consistent is their date metadata?</p>
    <dl class="dataset-facts">
      <div><dt>Records</dt><dd>268</dd></div>
      <div><dt>Report years</dt><dd>2005–2015</dd></div>
      <div><dt>Source</dt><dd class="fact-text">Course-provided CSV</dd></div>
    </dl>
  </section>

  <section class="project-section" aria-labelledby="method-title">
    <div class="section-label"><span class="section-number">A</span><h3 id="method-title">Approach</h3></div>
    <div class="section-content">
      <p>I summarised records by the year of <code>date_report</code>, then compared the calendar dates in <code>created_date</code> and <code>date_report</code>. The analysis uses all 268 rows and reports counts rather than estimates of poaching incidence.</p>
      <ol class="method-steps">
        <li><span>01</span><div><strong>Inspect</strong><p>Review the columns, parse the date fields, and check the recorded date range.</p></div></li>
        <li><span>02</span><div><strong>Summarise</strong><p>Count reports by year and classify creation dates as earlier than, the same as, or later than report dates.</p></div></li>
        <li><span>03</span><div><strong>Interpret carefully</strong><p>Separate patterns in the records from claims about events or the data collection process.</p></div></li>
      </ol>
    </div>
  </section>

  <section class="project-section findings-section" aria-labelledby="findings-title">
    <div class="section-label"><span class="section-number">B</span><h3 id="findings-title">What the data shows</h3></div>
    <div class="section-content">
      <figure class="chart-figure">
        <div class="figure-heading"><span>FIG. 01</span><h4>Report counts vary by year</h4></div>
        <a class="chart-image-link" href="{{ '/assets/images/annual_reports.png' | relative_url }}" aria-label="Open the annual report counts figure at full size">
          <img class="chart-image" src="{{ '/assets/images/annual_reports.png' | relative_url }}" width="2466" height="1326" alt="Bar chart of 268 recorded reports by report year, 2005–2015. Counts range from 2 in 2014 to 46 in both 2012 and 2015. Full-year coverage for 2015 is unverified." loading="lazy">
        </a>
        <figcaption>The largest recorded counts are 46 in both 2012 and 2015; the lowest is 2 in 2014. The latest observed report date in 2015 is 7 September; full-year coverage is unverified.</figcaption>
        <details class="chart-data">
          <summary>View the annual counts</summary>
          <div class="table-scroll" role="region" aria-label="Annual report counts" tabindex="0">
            <table>
              <caption>Number of records, grouped by report year</caption>
              <thead><tr><th scope="col">Year</th><th scope="col">Reports</th></tr></thead>
              <tbody><tr><th scope="row">2005</th><td>31</td></tr><tr><th scope="row">2006</th><td>7</td></tr><tr><th scope="row">2007</th><td>7</td></tr><tr><th scope="row">2008</th><td>20</td></tr><tr><th scope="row">2009</th><td>31</td></tr><tr><th scope="row">2010</th><td>25</td></tr><tr><th scope="row">2011</th><td>19</td></tr><tr><th scope="row">2012</th><td>46</td></tr><tr><th scope="row">2013</th><td>34</td></tr><tr><th scope="row">2014</th><td>2</td></tr><tr><th scope="row">2015 (coverage unverified)</th><td>46</td></tr></tbody>
            </table>
          </div>
        </details>
      </figure>

      <figure class="chart-figure">
        <div class="figure-heading"><span>FIG. 02</span><h4>Date definitions need investigation</h4></div>
        <a class="chart-image-link" href="{{ '/assets/images/date_consistency.png' | relative_url }}" aria-label="Open the date consistency figure at full size">
          <img class="chart-image" src="{{ '/assets/images/date_consistency.png' | relative_url }}" width="2321" height="1312" alt="Date comparison for 268 records: created_date is earlier than date_report for 167 records, 62.3 percent; the same for 19, 7.1 percent; and later for 82, 30.6 percent." loading="lazy">
        </a>
        <figcaption><strong>167 of 268 records (62.3%)</strong> have a creation date earlier than their report date. This is a flag for further checking; it does not establish that those records are incorrect.</figcaption>
        <details class="chart-data">
          <summary>View the date comparison counts</summary>
          <div class="table-scroll" role="region" aria-label="Date comparison counts" tabindex="0">
            <table>
              <caption>Calendar date of creation compared with calendar date of report</caption>
              <thead><tr><th scope="col">Creation date</th><th scope="col">Records</th><th scope="col">Share</th></tr></thead>
              <tbody><tr><th scope="row">Earlier than report date</th><td>167</td><td>62.3%</td></tr><tr><th scope="row">Same as report date</th><td>19</td><td>7.1%</td></tr><tr><th scope="row">Later than report date</th><td>82</td><td>30.6%</td></tr></tbody>
            </table>
          </div>
        </details>
      </figure>
    </div>
  </section>

  <section class="project-section" aria-labelledby="interpretation-title">
    <div class="section-label"><span class="section-number">C</span><h3 id="interpretation-title">Findings &amp; limits</h3></div>
    <div class="section-content interpretation">
      <div class="interpretation-item"><span class="annotation">01 / OBSERVATION</span><h4>The records are uneven over time.</h4><p>Yearly totals differ, but this dataset alone cannot explain why. Changes in reporting, coverage, or collection could affect the counts.</p></div>
      <div class="interpretation-item"><span class="annotation">02 / OPEN QUESTION</span><h4>Metadata needs context.</h4><p>The date comparison makes the next question explicit: what do the two date fields mean, and how were they entered? Their definitions and entry workflow need confirmation before labelling the order as an error.</p></div>
      <aside class="limits-note" aria-labelledby="limits-title"><h4 id="limits-title">What this analysis cannot establish</h4><p>These are counts of recorded reports, not actual poaching rates. There is no patrol-effort measure or population denominator, full-year coverage for 2015 is unverified, and no causal explanation is tested.</p><p>The course CSV has no confirmed redistribution permission. This public portfolio shares aggregate figures only; raw records and coordinates are excluded.</p></aside>
    </div>
  </section>

  <div class="project-close">
    <p>Follow the analysis, methods, and reproducibility notes.</p>
    <a class="button-link" href="https://github.com/mobbbs/data-science-project">View project on GitHub <span aria-hidden="true">↗</span></a>
  </div>
</article>

<section class="next-section" id="next" aria-labelledby="next-title">
  <div class="section-label"><span class="section-number">02</span><span>Learning forward</span></div>
  <div class="next-content">
    <h2 id="next-title">Better context.<br>
<em>More useful questions.</em></h2>
    <p>Next, I plan to verify the date-field definitions, review the records flagged by the comparison, and obtain collection or patrol-effort context if it is available.</p>
    <p>Alongside that work, I want to improve my Python workflow and add future projects with clear questions, reproducible steps, and limitations stated alongside the findings.</p>
    <a class="text-link" href="https://github.com/mobbbs">Follow my learning on GitHub <span aria-hidden="true">↗</span></a>
  </div>
</section>
