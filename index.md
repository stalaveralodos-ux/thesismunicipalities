---
layout: default
title: EU Policy Watch
permalink: /
wide_layout: true
---
<div class="home-hero">
  <h1>EU Policy Watch</h1>
  <p>A running, source-checked read on the EU legislative files that matter right now: where each one stands, who is pushing what, and what changes for the people and companies affected. Not a news feed, a tracker built to be revisited.</p>
</div>

<div class="home-live-strip">
  {% assign latest_digest = site.briefs | sort: 'month' | reverse | first %}
  {% if latest_digest %}
  <a class="home-live-card" href="{{ latest_digest.url | relative_url }}">
    <div class="home-live-label">Latest monthly digest — {{ latest_digest.title }}</div>
    <p>{{ latest_digest.headline }}</p>
  </a>
  {% endif %}

  {% assign latest_alert = site.pages | where_exp: "p", "p.url contains '/alerts/'" | where_exp: "p", "p.title != nil" | where_exp: "p", "p.url != '/eu-policy-watch/alerts/'" | sort: 'date' | reverse | first %}
  {% if latest_alert %}
  <a class="home-live-card" href="{{ latest_alert.url | relative_url }}">
    <div class="home-live-label">Latest alert — {{ latest_alert.date | date: "%d %b %Y" }}</div>
    <p>{{ latest_alert.title }}</p>
  </a>
  {% endif %}
</div>

## Where to start

<div class="section-explainer-grid">

  <a class="section-explainer-card section-directives" href="{{ '/directives/' | relative_url }}">
    <span class="section-explainer-icon">✳</span>
    <span class="section-explainer-name">Directives</span>
    <span class="section-explainer-text">A dedicated dashboard for each legislative file: legal and political status, a horizontal timeline, who holds the pen in each institution, and what happens next. This is the core of the site.</span>
    <span class="section-explainer-cta">Browse directives →</span>
  </a>

  <a class="section-explainer-card section-actors" href="{{ '/actors/' | relative_url }}">
    <span class="section-explainer-icon">◐</span>
    <span class="section-explainer-name">Actors</span>
    <span class="section-explainer-text">The people and institutions steering each dossier: who leads it inside the Commission, who holds the pen in Parliament, which Council presidency landed or blocked what, and where outside pressure comes from.</span>
    <span class="section-explainer-cta">Meet the actors →</span>
  </a>

  <a class="section-explainer-card section-alerts" href="{{ '/alerts/' | relative_url }}">
    <span class="section-explainer-icon">!</span>
    <span class="section-explainer-name">Alerts</span>
    <span class="section-explainer-text">Short, dated notes the moment something concrete happens on a file, a vote, a mandate, a missed deadline, with a link back to the full directive for context.</span>
    <span class="section-explainer-cta">See latest alerts →</span>
  </a>

  <a class="section-explainer-card section-sector" href="{{ '/sector-impact/' | relative_url }}">
    <span class="section-explainer-icon">▤</span>
    <span class="section-explainer-name">Sector impact</span>
    <span class="section-explainer-text">Who actually feels each file, by sector, finance, manufacturing, retail, agriculture, rather than by institution. Still early and being filled in as sourced data comes in.</span>
    <span class="section-explainer-cta">View sector impact →</span>
  </a>

  <a class="section-explainer-card section-briefs" href="{{ '/briefs/' | relative_url }}">
    <span class="section-explainer-icon">▦</span>
    <span class="section-explainer-name">Briefs</span>
    <span class="section-explainer-text">A monthly archive of what actually moved across every file tracked here, one entry per month, starting August 2026. The fastest way to catch up after time away.</span>
    <span class="section-explainer-cta">Read the archive →</span>
  </a>

</div>
