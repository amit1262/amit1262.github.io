---
layout: default
title: Key Projects
permalink: /key-projects/
---

<section class="projects">
  <ol class="styled-number">
    <li>
      <article class="project-summary">
      <h3><a href="/key-projects/agentic_ai_network_study/">Agentic AI System for No-Code Network Study in Healthcare (Ongoing)</a></h3>
      <div class="project-links">
        <a href="https://github.com/amit1262/chatbot" target="_blank">GitHub</a>
      </div>
      <p>Network studies allow clinical researchers to run the same data analysis across multiple institutions or databases using a common data model, ensuring consistency and reproducibility. Traditionally, setting up such studies requires writing complex R code, which can be a barrier for clinical researchers with limited programming experience.</p>
      <p> <strong> Key Contributions of this project: </strong></p>
      <ul>
        <li> A user-friendly system that uses multiple AI agents to enable researchers to design network studies using natural language</li>
        <li> Validation of final study specification for integrity and completeness </li>
      </ul>
      <p> <strong> Key Technologies: </strong> LangChain, LangGraph frameworks, Python, Model Context Protocol (MCP), Strategus (OHDSI) </p>
    </article>
    </li>
    <!-- <li>
      <article class="project-summary">
        <h3><a href="/key-projects/llm-based-mapping">LLM-based Cross-Domain Data Mapping</a></h3>
        <p>This project utilizes a language model to map data from non-omop format to OHDSI OMOP format</p>
      </article>
    </li> -->
    <li>
      <article class="project-summary">
        <h3><a href="/key-projects/video-events-detection/">Video Analytics System for Natural Language-Driven Surveillance</a></h3>
        <p>
          This project designs a modular, AI-powered video analytics system capable of responding to natural language queries. It combines object detection (YOLO, GroundingDINO), tracking (DeepSORT), action recognition (SlowFast, TimeSformer), and fine-tuned VideoLLMs. A custom query agent translates user queries into subtasks and invokes models for real-time insights. The system targets industrial scenes (e.g., ports), addressing challenges like occlusion, poor lighting, and ambiguous motion patterns.
        </p>
      </article>
    </li>
    <li>
      <article class="project-summary">
      <h3><a href="/key-projects/smrtfridge/">SmrtFridge: IoT-based, User Interaction-driven Food Item & Quantity Sensing</a></h3>
      <div class="project-links">
        <a href="https://github.com/amit-smu/SmrtFridge-System" target="_blank">GitHub</a>
        <a href="https://www.youtube.com/watch?v=Scd7vlfSipw" target="_blank">Presentation Video</a>
        <a href="https://ink.library.smu.edu.sg/cgi/viewcontent.cgi?article=5649&context=sis_research" target="_blank">Full Paper</a>
      </div>
      <p>SmrtFridge is a smart fridge prototype that uses thermal and RGB sensing, combined with deep learning, to identify food items and estimate remaining quantity—without the need for RFID tags or user labeling. It leverages natural user interactions (e.g., door openings) to trigger video capture and processing. The system, triggered by natural interactions, achieves ~85% accuracy in classification and ~75% accuracy in quantity estimation. Its low-intrusion design makes it promising for real-world adoption in smart kitchens.</p>
    </article>
    </li>
    <li>
      <article class="project-summary">
      <h3><a href="/key-projects/collabcam/">CollabCam: Deep Learning based System for Energy-Efficient Pervasive Vision</a></h3>
      <div class="project-links">
          <a href="https://github.com/amit-smu/edge_collaboration" target="_blank">GitHub</a>
          <a href="https://dl.acm.org/doi/full/10.1145/3736420" target="_blank">Full Paper</a>
      </div>
      <p>CollabCam is an edge-based vision system enabling collaborative inference in multi‑camera deployments. Each camera sends mixed-resolution frames, downsampled in shared FoVs, and collaboratively uses peer camera bounding boxes to boost detection. It cuts down network and energy usage by 25‑35%, while keeping accuracy losses under 2‑5% when compared to non‑collaborative approaches.</p>
      </article>
    </li>
  </ol>

  <!-- Repeat for more projects -->
</section>
<script src="/scripts.js"></script>
