---
layout: default
title: SmrtFridge System
permalink: /key-projects/video-events-detection/
---

<div class="project-details">
    <h3>Video Analytics System for Natural Language-Driven Surveillance</h3>
    <p><strong>Problem:</strong> Traditional surveillance systems require manual rule-setting and lack adaptability to
        dynamic environments like ports or industrial sites. They often fail in challenging scenarios like occlusions,
        aerial views, or ambiguous human-object interactions.</p>
    <p><strong>Solution &amp; Architecture:</strong> This system enables natural language-driven video analysis using a
        pipeline of:</p>
    <ul>
        <li><strong>Object Detection:</strong> YOLOv8, Detectron2, GroundingDINO, and OWL-ViT models fine-tuned on
            marine/industrial datasets.</li>
        <li><strong>Tracking:</strong> DeepSORT for temporal tracking of people, containers, cranes, and spreaders.</li>
        <li><strong>Action Recognition:</strong> Models like SlowFast and TimeSformer detect meaningful actions over
            N-frame windows.</li>
        <li><strong>Video LLMs:</strong> InternVideo 2.5, Llava, and VideoLLaMA3 tested on port and domestic videos
            using context-aware prompts.</li>
        <li><strong>Query Agent:</strong> Breaks down user queries into subtasks (e.g., proximity detection, container
            motion) and interprets results using GPT-4 or similar LLMs.</li>
    </ul>
    <p><strong>System Architecture: </strong></p>
    <img src="/projects/images/video_event_detection_system.jpg" style="max-width: 80%; height: auto; display: block; margin: 0 auto;"/>
    <p><strong>Experiments & Observations:</strong> The team evaluated multiple VideoLLMs across scenarios (with/without
        blur/highlighting), revealing hallucination risks and gaps in temporal reasoning. Prompt engineering,
        object-aware attention, and subtask chaining significantly improved relevance.</p>
    <p><strong>Impact:</strong> The proposed architecture supports near-real-time analytics in industrial setups with
        minimal rule authoring. It offers an extensible framework for querying unstructured video via conversational
        input—helping ensure safety (e.g., worker too close to moving container) and increasing automation in
        surveillance tasks.</p>
</div>
