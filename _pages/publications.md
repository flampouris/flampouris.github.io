---
title: "Publications"
layout: gridlay
sitemap: false
permalink: /publications/
years: [2006, 2007, 2008, 2009, 2010, 2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019, 2020, 2021, 2022, 2023, 2024, 2025]
---

<style>
.jumbotron{
    padding:3%;
    padding-bottom:10px;
    padding-top:10px;
    margin-top:10px;
    margin-bottom:30px;
}
</style>


### Books

<div class="jumbotron">
{% bibliography --query @Book %}
</div>


### Book Chapter

<div class="jumbotron">
{% bibliography --query @InBook %}
</div>

### Journal Articles

<div class="jumbotron">
{% bibliography --query @article %}
</div>

### Conference Proceedings

<div class="jumbotron">
{% bibliography --query @inproceedings %}
</div>

### In Collections

<div class="jumbotron">
{% bibliography --query @incollection %}
</div>

### Technical Reports

<div class="jumbotron">
{% bibliography --query @TechReport %}
</div>
