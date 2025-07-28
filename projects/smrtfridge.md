---
layout: default
title: SmrtFridge System
permalink: /key-projects/smrtfridge
---

<div class="project-details">
    <h3>SmrtFridge: IoT‑based, User Interaction‑Driven Food Item & Quantity Sensing</h3>
    <p><strong>Links:</strong></p>
    <div class="project-links">
      <a href="https://github.com/amit-smu/SmrtFridge-System" target="_blank">GitHub</a>
      <a href="https://www.youtube.com/watch?v=Scd7vlfSipw" target="_blank">Presentation Video</a>
      <a href="https://ink.library.smu.edu.sg/cgi/viewcontent.cgi?article=5649&context=sis_research" target="_blank">Full Paper</a>
    </div>
    <p><strong>Problem:</strong> Modern consumers struggle to keep track of fridge contents without tagging food items. Existing smart fridge solutions rely on RFID or manual labeling, making adoption burdensome.</p>
    <p><strong>Solution &amp; Contributions:</strong> SmrtFridge is a consumer‑grade prototype that identifies what users place into or remove from their fridge, and estimates how much remains in a container, all without RFID tags or explicit user input. It uses a hybrid sensing pipeline:</p>
    <ul>
        <li><strong>Item Segmentation: </strong>Proposes two methods including </li>
        <ul>
            <li>Optical-flow based item segmentation (uses only RGB images/video) </li>
            <li>Thermal image based segmentation (uses thermal + RGB) </li>
        </ul>
        IR and RGB videos are automatically triggered by the user's natural interactions with the fridge door.
        <li><strong>Item Classifiation: </strong>A Deep Neural Network that classifies the extracted food images.</li>
        <li><strong>Quantify Estimation: </strong>Thermal contrast measurement (via temperature differences) to infer coarse levels of remaining food (e.g., empty/half/full).</li>
    </ul>
    <p> <strong>System Architecture: </strong></p>
    <img src="/projects/images/smrtfridge_workflow.png"/>
    <p><strong>Results:</strong> In a user study with 12 participants and 19 common food items, SmrtFridge correctly captured at least 75 % of a food item’s image in over 97 % of interactions. It achieved approximately 85 % precision and recall in identifying food items, and around 75 % accuracy in three-level quantity estimation.</p>
    <p><strong>Impact:</strong> SmrtFridge demonstrates that ambient sensing techniques can provide accurate food recognition and quantity tracking without intrusive tags—paving the way for more accessible smart kitchen applications.</p>
</div>
