---
layout: splash
title: "pandapipes"
permalink: /
header:
  overlay_image: /images/home/background.png
  cta_label: "<i class='fas fa-download'></i> Install Now"
  cta_label2: "<i class='fas fa-envelope'></i> Get Updates"
  cta_url: "/start/#install"
  cta_url2: "/contact/#list"
  subtitle: <a href='https://pypi.python.org/pypi/pandapower'> <img src='{{"/images/home/shield_python_versions.svg" | relative_url}}'></a>
  
shields:
  - icon: 'https://badge.fury.io/py/pandapipes.svg'
    url: https://pypi.python.org/pypi/pandapipes
  - icon: 'https://img.shields.io/pypi/pyversions/pandapipes.svg'
    url: https://pypi.python.org/pypi/pandapipes
  - icon: https://readthedocs.org/projects/pandapower/badge/
    url: http://pandapipes.readthedocs.io/
  - icon: 'https://codecov.io/github/e2nIEE/pandapipes/coverage.svg?branch=develop'
    url: https://codecov.io/github/e2nIEE/pandapipes?branch=master
  - icon: 'https://api.codacy.com/project/badge/Grade/86c876ab23fc40d98e85f7d59bdef928'
    url: https://app.codacy.com/gh/e2nIEE/pandapipes/dashboard
  - icon: 'https://img.shields.io/badge/License-BSD%203--Clause-blue.svg'
    url: https://github.com/e2nIEE/pandapipes/blob/master/LICENSE
  - icon: 'https://mybinder.org/badge_logo.svg'
    url: https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=tutorials
    
excerpt: An easy to use open source tool for fluid system modeling, analysis and optimization with a high degree of automation.
feature_row:
  - image_path: /images/home/fluid_modeling.PNG
    title: "Fluid Modeling"
    excerpt: "Includes thoroughly validated models for pipes, pumps, valves and more."
    url: "about/#modeling"
    btn_class: "btn--primary"
    btn_label: "Learn More"
  - image_path: /images/home/power_flow.png
    title: "Fluid System Analysis"
    excerpt: "Supports stationary and quasi-stationary analysis of gas and district heating networks."
    url: "about/#analysis"
    btn_class: "btn--primary"
    btn_label: "Learn More"
  - image_path: /images/home/osi_symbol.png
    title: "Free and Open"
    excerpt: "Published under a BSD License and therefore free to use, modify and share however you want."
    url: "https://github.com/e2nIEE/pandapipes"
    btn_class: "btn--primary"
    btn_label: "Explore on github"
---

To get started with pandapipes, just

1. Install pandapipes through pip:

        pip install pandapipes

2. Create a simple network

        import pandapipes as pp
        net = pp.create_empty_network(fluid="lgas") 
        j1 = pp.create_junction(net, pn_bar=1.05, tfluid_k=293.15, name="Junction 1")
        j2 = pp.create_junction(net, pn_bar=1.05, tfluid_k=293.15, name="Junction 2")    
        j3 = pp.create_junction(net, pn_bar=1.05, tfluid_k=293.15, name="Junction 3") 
        ext_grid = pp.create_ext_grid(net, junction=j1, p_bar=1.1, t_k=293.15, name="Grid Connection")
        sink = pp.create_sink(net, junction=j3, mdot_kg_per_s=0.045, name="Sink")
        pipe = pp.create_pipe_from_parameters(net, from_junction=j1, to_junction=j2, length_km=0.1, diameter_m=0.05, name="Pipe 1")
        valve = pp.create_valve(net, from_junction=j2, to_junction=j3, diameter_m=0.05, opened=True, name="Valve 1")
        
3. Run a pipe flow:

        pp.pipeflow(net)
        
4. And check the results:

        print(net.res_junction)
        print(net.res_pipe)

But of course pandapipes can do much more than that - find out what on this page!

{% include feature_row id="intro" type="center" %}
    
{% include feature_row %}
