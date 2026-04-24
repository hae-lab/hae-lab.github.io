---
layout: default
title: Home
---

<div class="hero">
  <h2 class="largestest">HKUST HAE Lab</h2>
  <span id='lab-desc'>
    We design interactive data systems that make complex data accessible, interpretable, and actionable for everyone.
    HAE Lab is an interdisciplinary research lab located at the <a href="https://cse.hkust.edu.hk/">Department of Computer Science and Engineering</a> at the <a href="http://hkust.edu.hk/">Hong Kong University of Science and Technology (HKUST)</a>, led by <a href="https://sehilyi.com">Sehi L'Yi</a>.
  </span>
</div>

## Our Research
<div class="areas">
    {% assign areas = site.areas | sort: 'order' %}
    {% for area in areas %}
    {% include area.html %}
    {% endfor %}
</div>

## Selected Projects
<div class="themes">
    {% assign themes = site.projects | sort: 'order' %}
    {% for theme in themes %}
    {% include theme.html %}
    {% endfor %}
</div>

<div class="news-section">
  <div class="news-section-body">
    <div class="news-section-header">
      <h2>News &amp; Events</h2>
      <!--<a href="/news" class="view-all-link">View all news →</a>-->
    </div>
    <div class="news-cards">
      {% assign latest_news = site.news | sort: 'date' | reverse | slice: 0,3 %}
      {% for news in latest_news %}
      {% include news-card.html %}
      {% endfor %}
    </div>
  </div>
  <div class="join-lab-box">
    <h3>Join Our Lab</h3>
    <p>We are always looking for highly-motivated students and postdocs.</p>
    <a href="/join" class="join-lab-btn">View Openings →</a>
  </div>
</div>

## Selected Publications <small><a href="/publications/">[see more]</a></small>

<table class="publications">
    {% assign featured_publications = site.publications | where: 'featured', true | sort: 'year' | reverse | slice: 0,10 %}
    {% for publication in featured_publications %}
    {% include publication.html %}
    {% endfor %}
</table>

## Media Coverage
<table class='media'>
    <tr>
        <td>
            <div class='media-source'>
                <img class='media-nature-icon' src='assets/nature.png' alt=""/>
                <strong>Nature</strong> (TECHNOLOGY FEATURE)
            </div>
            <div class='media-title'>
                <a href="https://www.nature.com/articles/d41586-022-02191-z">
                    A graphics toolkit for visualizing genome data
                </a>
            </div>
            <div class='media-subtitle'>
                Powerful 'grammar' allows geneticists to display their data in interactive and scalable illustrations.
            </div>
            <!--
            <div class='media-desc'>
                "Sehi L’Yi, who led Gosling’s development, says that what differentiates Gosling from other visualization tools is its expressiveness. With most tools, he says, the graphics that can be made and what they will look like are predefined. ‘It is really not easy to customize visualizations as a user.’ But with Gosling, users can, for instance, specify the colour, dimensions and placement of the symbol used to represent a centromere or genomic interval, then overlay that on an ideogram of a chromosome to highlight a region of interest."
            </div>
            -->
        </td>
        <!--
        <td>
            <img class='media-thumbnail' src='https://media.nature.com/w1219/magazine-assets/d41586-022-02191-z/d41586-022-02191-z_23359970.jpg?as=webp' alt="Image with two heatmap visualizations that look like an eyebrow and an eye."/>
        </td>
        -->
    </tr>
</table>

