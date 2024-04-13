---
layout: page
title: General-Purpose Reliable Automation for Preprocessing EEG (GRAPE)
description: Automating EEG preprocessing steps.
img: 
importance: 1
category: Other
related_publications:
---
### What we did
We implemented established methods and built an EEG preprocessing library in Python to automate some aspects of the very tedious task. We are calling it GRAPE. These are the preprocessing steps that have been implemented. Also, thank you [MNE-Python](https://mne.tools/stable/index.html), because GRAPE wouldn't otherwise exist. We are currently preparing the manuscript for this!

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Preprocessing Procedure Overview</title>
    <script src="https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.min.js"></script>
    <script>mermaid.initialize({startOnLoad:true});</script>
</head>
<body>
    <div class="mermaid">
        flowchart TB
        A(Filtering):::set
        B(Bad channel detection):::set
        C(Bad channel removal):::set
        D(Independent Component Analysis):::set
        E(Artifact identification):::set
        F(Artifact removal):::set
        G(Epoch segmentation):::set
        H(Evoked signal extraction):::set
        A-->B
        B-->C
        C-->D
        D-->E
        E-->F
        F-->G
        G-->H
        classDef set stroke:#000000, stroke-width:2px,color:#000000, fill:#fff
    </div>
</body>
</html>
