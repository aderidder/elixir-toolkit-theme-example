---
title: The FAIR Metroline
---

The FAIR principles aim to make data Findable, Accessible, Interoperable and Reusable, to maximize the reuse of (research) data. See the Health-RI website for more information on FAIR. 

But, where do you start to make data FAIR? What steps are involved? What do these steps mean and, importantly, how do you implement these steps? 

The FAIR Metroline provides practical guidance to help you reach your FAIR goals and make your data more FAIR. Each Metroline step includes a short description, aimed at a general audience, as well as a section describing the expertise that may be necessary for the how-to section. This expertise can vary greatly per step and may include, for example, domain experts, software engineers or legal professionals. Given the time commitment and specialised knowledge needed, most steps will require the expertise of at least a data steward.

![FAIR Metroline.jpg](assets/img/main/FAIR%20Metroline.jpg)

A variety of models and publications which are used in practice were studied to identify common FAIRification steps, which resulted in the FAIR Metroline (see image above). Depending on your project and goals only a select number of steps may be relevant. Consequently, each project will have its specific workflow: 

{% mermaid %}
graph LR
  A[Define FAIRification Objectives] --> B[Build your team]
  B --> C[Have a FAIR data steward on board]
  C --> D[Pre-FAIR Assesment]

  click A "./metroline_steps/define_fairification_objectives"
  click C "./metroline_steps/have_a_fair_data_steward_on_board"
  click D "./metroline_steps/pre_fair_assessment"
{% endmermaid %}

[//]: # (![FAIR workflow image.png]&#40;assets/img/main/FAIR%20workflow%20image.png&#41;)


The FAIR Metroline is under development, in alignment with the development of the Dutch National Health Data Catalogue. Over the coming months, we will add detailed how-to descriptions and real-life examples of FAIR Metroline that will particularly help projects and initiatives to onboard (meta)data to the Dutch National Health Data Catalogue. This already is a first effective step to make your data more FAIR. We also collaborate with the health domain funders and their efforts to stimulate incorporating FAIR into projects from the start. 

For the current status of the steps see the status page.

## How to contribute

The FAIR Metroline will be richer and more feasible to execute if we better consider the organisational context and existing best practices. As a result, the FAIR Metroline is a cooperative effort between the Health-RI Hub and Nodes, involving the many public and private organisations and initiatives that address the reuse of care and research data. We invite you to collaborate with us as we continue to refine the various FAIR Metroline phases. To find out more, e-mail fairservicedesk@health-ri.nl.

## Overview Metroline steps

<div>
  {% for graph in site.data.graphs.main %}
    <button onclick="showGraph('{{graph.id}}')">{{graph.label}}</button>
  {% endfor %}
</div>

<div id="graph-container">
  {% for graph in site.data.graphs.main %}
  <div id="{{ graph.id }}" class="mermaid">
    {{ graph.definition }}
  </div>
  {% endfor %}
</div>

<script src="assets/js/graphController.js"></script>

<script>
  window.onload = () => {
    const graphVisibility = {
      // maybe play around with some filtering for sections? Since you could have more than one graph in a section?
      // {% assign filtered_graphs = site.data.graphs.main | where: "visible", false %}
      {% for graph in site.data.graphs.main %}
        "{{ graph.id }}": {{ graph.visible | downcase }}{% unless forloop.last %},{% endunless %}
      {% endfor %}
    };
    initGraphs(graphVisibility)
  };
</script>



direct hit 
Define FAIRification Objectives

running shirt 

 Build the Team

mechanic 

Have a FAIR data steward on board

woman lifting weights 

Get Training

bookmark tabs 

Design Solution Plan

check mark button 

Pre-FAIR Assessment

locked with key 

Data access and retrieval

books 

Assess availability of your metadata

passport control 

Select Identifier Scheme

card file box 

Register resource level metadata

card file box 

Register record level metadata

hammer and wrench 

Apply common data elements

magnifying glass tilted right 

Analyse data semantics

memo 

Design eCRF (data collection)

building construction 

Create or reuse a semantic (meta)data model

open book 

(ToDo) Use ontologies in the data model

person: red hair 

Obtain Informed Consent

laptop computer 

(ToDo) Enter data in eCRF (data collection)

card file box 

(ToDo) Apply core metadata model

hammer and wrench 

Transform and expose FAIR (meta)data

locked with key 

Define access conditions

Question Mark 

Query (use) over resources

check mark button 

Assess FAIRness

chequered flag 

Did you reach your FAIRification objectives

 

Models and further reading 

The Metroline - Steps for your FAIRification Workflow 

Critical Steps towards Large-Scale Implementation of the FAIR Data Principles

Processes and workflows assessed in the FAIR Metroline: 

Generic

De Novo

FAIRopoly

FAIR Plus

GO FAIR

5 Pillars of FAIRification (unpublished)

Trust Framework (unpublished)