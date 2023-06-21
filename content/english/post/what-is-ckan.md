---
author: "Geo V L"
date: 2018-07-05
linktitle: What is CKAN
nomenu:
  main:
    parent: tutorials
next: /tutorials/what-is-ckan
prev: /tutorials/what-is-ckan
title: What is CKAN
tags : [
    "ckan",
    "data",
]
categories : ["ckan"]
weight: 10
image: img/tags.jpg
authorAvatar: hugo-logo.png
---

CKAN stands for Comprehensive Knowledge Archive Network. CKAN is a self-described data portal platform that allows an organization to manage, publish, and share data and for others to find and use that data. It is a tool for making open data websites.It helps you manage and publish collections of data. It is used by national and local governments, research institutions, and other organizations who collect a lot of data.

Once your data is published, users can use its faceted search features to browse and find the data they need, and preview it using maps, graphs and tables - whether they are developers, journalists, researchers, NGOs, citizens, or even your own staff.
In general, data portal platforms provide a structured solution of software, policies, and guidelines that let an organization (often a government entity) share data. The services embedded in these platforms may include data management, content management, data publishing, data discovery, visualization, and workflow. Other examples of such products include

* [Socrata](https://socrata.com/)
* [Junar](http://www.junar.com/)
* [DKAN](http://drupal.org/project/dkan)
* [Open Government Platform](http://www.opengovplatform.org/).

CKAN installation guidelines are detailed on the site at [Here](http://docs.ckan.org/en/latest/maintaining/installing/index.html)

We can run it standalone (as noted above) or in a hosted instance. CKAN provides a hosted service, which lets you essentially run the software in an instance on their servers 

### DataSets and Resources ###

For CKAN purposes, data is published in units called “datasets”. A dataset is a parcel of data - for example, it could be the crime statistics for a region, the spending figures for a government department, or temperature readings from various weather stations. When users search for data, the search results they see will be individual datasets.

A dataset contains two things:

* Information or “metadata” about the data. For example, the title and publisher, date, what formats it is available in, what license it is released under, etc.
* A number of “resources”, which hold the data itself. CKAN does not mind what format the data is in. A resource can be a CSV or Excel spreadsheet, XML file, PDF document, image file, linked data in RDF format, etc. CKAN can store the resource internally, or store it simply as a link, the resource itself being elsewhere on the web. A dataset can contain any number of resources. For example, different resources might contain the data for different years, or they might contain the same data in different formats.