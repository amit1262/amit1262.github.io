---
layout: default
title: Agentic AI System
permalink: /key-projects/agentic_ai_network_study/
---

<div class="project-details">
    <h3>Agentic AI System for No-Code Network Study in Healthcare </h3>
    <div class="project-links">
        <a href="https://github.com/amit1262/chatbot" target="_blank">GitHub</a>
    </div>
    <p><strong> Problem Background: </strong> Network studies enable researchers to run the same analysis across multiple institutions using a shared 
        data model like OMOP CDM. This ensures consistency while preserving local data privacy. However, setting up such studies 
        typically requires writing complex R code, which poses a barrier for clinical researchers without programming experience. 
    </p>
    <p><strong> Proposed Solution: </strong> The Strategus framework from OHDSI offers a modular, portable approach to observational research by 
        allowing study designs to be represented in a standardized <code>JSON</code> format. While this improves reproducibility 
        and reusability, creating the JSON specification still relies on R programming and understanding complex study components. 
    </p>
    <p> This project introduces an AI-powered, natural language interface to generate Strategus-compatible study specifications 
        without requiring R coding. Following are the key features: 
    </p>
    <ul>
        <li>
            A <strong>multi-agent system</strong> using the <strong>LangChain & LangGraph</strong> frameworks to decompose the study design process into 
            modular, conversational tasks handled by specialized AI agents.
        </li>
        <li>
            The system uses <strong>Model Context Protocol (MCP)</strong> to manage memory, maintain shared understanding between agents, 
            and track study context across user interactions.
        </li>
        <li>
            Built in <strong>Python</strong>, the system transforms user inputs into a complete, validated <code>JSON</code> specification, 
            ready to be executed using Strategus pipelines.
        </li>
    </ul>
</div>
