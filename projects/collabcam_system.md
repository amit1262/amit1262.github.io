---
layout: default
title: CollabCam System
permalink: /key-projects/collabcam/
---

<div class="project-details">
     <h3>CollabCam: Deep Learning based System for Energy-Efficient Pervasive Vision</h3>
    <p><strong>Links:</strong></p>
    <div class="project-links">
        <a href="https://github.com/amit-smu/edge_collaboration" target="_blank">GitHub</a>
        <a href="https://dl.acm.org/doi/full/10.1145/3736420" target="_blank">Full Paper</a>
    </div>
    <p><strong>Problem:</strong> Deploying deep-learning–based visual analytics across multiple cameras often incurs high network bandwidth and energy consumption—especially when cameras transmit full-resolution images even for overlapping scenes.</p>
    <p><strong>Approach & Contributions:</strong> CollabCam introduces:</p>
    <ul>
    <li><strong>Mixed-Resolution Frame (MRF):</strong> Each camera transmits low‑resolution image data for overlapping regions, drastically reducing bandwidth.</li>
    <li><strong>Collaborative Inference:</strong> Cameras share translated object bounding boxes with peers as auxiliary input, enabling off-the-shelf object detectors (e.g., YOLOv3, SSD) to be retrained for collaboration without structural changes.</li>
    </ul>
    <p> <strong>System Architecture: </strong></p>
    <img src="/projects/images/collabcam_architecture.jpg" style="max-width: 70%; height: auto; display: block; margin: 0 auto;" />
    <p><strong>Experimental Results:</strong> In benchmark outdoor campus datasets, CollabCam achieves a 50–60× reduction in frame size with only a ≤2–5% drop in object detection accuracy, compared to >45–60% degradation in non‑collaborative baselines. In a Raspberry Pi prototype, it reduced energy/image frame overhead by 25–35%, and up to 45% with hardware optimization.</p>
    <p><strong>Impact:</strong> CollabCam demonstrates that efficient, energy-aware, edge‑based collaboration between cameras can enable scalable vision analytics in resource-constrained, real‑world deployments without major accuracy loss.</p>

</div>
