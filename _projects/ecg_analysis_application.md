---
layout: distill
title: ECG Analysis Application
description: We created an application for the automatic diagnosis of 12-lead ECG images.
img: assets/img/ecg-application.png
importance: 1
category: Technion
date: 2023-01-22

authors:
  - name: Idan Levy
    url: "https://idanlevy.com"
    affiliations:
      name: Technion

# Optionally, you can add a table of contents to your post.
# NOTES:
#   $$ E = mc^2 $$
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - we may want to automate TOC generation in the future using
#     jekyll-toc plugin (https://github.com/toshimaru/jekyll-toc).
toc:
  - name: Background
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: Application Demonstration
  - name: Diagnosed Diseases
  - name: Clinical Trial
  - name: Discussion

# Below is an example of injecting additional post-specific styles.
# If you use this post as a template, delete this _styles block.
_styles: >
  .fake-img {
    background: #bbb;
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: 0 0px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 12px;
  }
  .fake-img p {
    font-family: monospace;
    color: white;
    text-align: left;
    margin: 12px 0;
    text-align: center;
    font-size: 16px;
  }

---

## Background

There are over 100 different cardiac conditions which are mostly diagnosed by 
interpreting 12-lead electrocardiogram (ECG) tests. We created a mobile application that can interpret the ECG test automatically, 
without any human intervention. The purpose of the application is not to replace the expert cardiologist's interpretation, but to serve 
as an assistant to medical personnel in providing the best immediate response and save lives by diagnosing conditions that require immediate action.
While an expert cardiologist will know how to interpret the test, the technician that completes the exam or the nurse/doctor/physician that provides 
immediate care to the patient might not know how to interpret the ECG correctly. It can take a couple of hours until an expert cardiologist will see the 
test, and these hours can be critical in certain conditions.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/ecg-application.png" title="Application for the automatic diagnosis of 12-lead ECG images" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Application for the automatic diagnosis of 12-lead ECG images.
</div>

***

## Application Demonstration

The application allows taking a video of an ECG test. The video is sent to our servers, where it is processed and the relevant frames are passed through a neural network that 
interprets the ECG. In less than 10 seconds, a result is sent back from the server to the application with the interpretation.
The user can go back to past results and see the diagnosis of the machine for each ECG, along with an explainability image that 
shows the locations on the ECG test which the neural network gave more weight to.

Screenshots of the application:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/ecg-application-2.png" title="Application for the automatic diagnosis of 12-lead ECG images - App demonstration 2" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Demonstration of the application.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/ecg-application-3.png" title="Application for the automatic diagnosis of 12-lead ECG images - App demonstration 2" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Video demonstration:
video

## Diagnosed Diseases

We diagnose a total of 23 different cardiac conditions, with accuracy scores of 85% or higher.

## Clinical Trial

The application is currently being used by several doctors in different hospitals around the world. We are gathering new 
data that will help us to automatically diagnose new cardiac conditions and also improve the accuracy of our results.
For the clinical trial, we have received approval from the Helsinki committee.

## Discussion

We created a neural network that can diagnose different cardiac conditions, based on 12-lead ECG images.
Our model currently needs a couple of hundred images of a cardiac condition to successfully diagnose a new cardiac condition.
We are researching ways in which we can reduce this number while still getting high accuracy results.
The clinical trial will help us to gather new data, and also test the performance of our model on unseen data.