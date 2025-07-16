---
layout: default
title: Amit Sharma - Portfolio
---

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Amit Sharma - Portfolio</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <div class="container">
        <!--<img src="img/amit_hd.jpg" alt="Profile Picture" class="profile" />
        <h1>Amit Sharma, PhD</h1>
        <h3>Machine Learning | Deep Learning | Generative AI | NLP | LLMs | Computer Vision</h3>
        -->
        
        <div class="tabs">
            <div class="tab active" onclick="showTab('intro')">Introduction</div>
            <div class="tab" onclick="showTab('projects')">Key Projects</div>
        </div>

        <div id="intro" class="tab-content active">
            <h3>Background</h3>
            <p style="font-family: Calibri, sans-serif;">
                I am a researcher working in the domains of generative AI (GenAI), deep learning, computer vision, and
                IoT systems. I have hands-on experience (5+ years) developing ML algorithms, computer vision techniques,
                customization and transfer-learning of various deep learning models. So far, I have worked on multiple
                sensing modalities including RGB/visible-light cameras, infrared (IR) cameras, magnetic switches, audio
                sensors, RADAR/LiDAR & air-quality sensors.
            </p>
            <h3>Education</h3>
            <pre style="font-family: Calibri, sans-serif;">
        <b>PhD in Computer Science (2015 – 2021)</b>
        SMU, Singapore | Advisor: <a href="https://faculty.smu.edu.sg/profile/archan-misra-376" target="_blank"> Prof Archan Misra </a>
        Dissertation: Vision-based Analytics for Improved AI-driven IoT Applications [<a href="https://ink.library.smu.edu.sg/etd_coll/321/" target="_blank"> Link </a>]

        <b>M.Tech in Mobile & Ubiquitous Computing (2012-2014)</b>
        IIIT Delhi | Advisor: <a href="https://www.vinayaknaik.info/" target="_blank"> Prof Vinayak Naik </a>

        <b>B.Tech in Computer Science (2008-2012)</b>
        GJ University of Science & Technology, Hisar
      </pre>
        </div>

        <div id="projects" class="tab-content projects">
            <h3>Key Projects</h3>
            <ul>
                <li><strong>LLM Based Data Mapping</strong>: Built an LLM-based data mapping system where input data is
                    in non-OMOP format and the output
                    is in OMOP format. <a href="projects/llm_driven_data_mapping.html"> More Details </a></li>
            </ul>
        </div>
    </div>

    <script src="scripts.js"></script>

</body>

</html>
