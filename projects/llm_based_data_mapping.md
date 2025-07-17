---
layout: default
title: LLM-based Cross-Domain Data Mapping
permalink: /llm-based-mapping
---

<h1> Turning Chaos into Consistency: Using LLMs to Map Medical Data to OMOP CDM</h1>

<p>Medical research thrives on <strong>data standardization</strong>. But in the real world, data is messy — especially
    in healthcare.</p>

<p>Datasets from different hospitals, research institutions, or countries often come in <strong>non-standard
        formats</strong>, with wildly inconsistent naming conventions, data structures, and definitions. This poses a
    major challenge when attempting to conduct <strong>reproducible, large-scale observational studies</strong> using
    frameworks like the <strong>OMOP Common Data Model (CDM)</strong>.</p>

<p>In this project, we tackled this problem using an unconventional approach: <strong>Large Language Models
        (LLMs)</strong>.</p>

<h2>The Problem: Medical Data Isn’t Always OMOP-Ready</h2>

<p>Imagine you're a researcher wanting to study diabetes-related complications across multiple institutions. You’d
    ideally want all datasets to conform to a shared schema — say, OMOP CDM. But in practice, datasets look like this:
</p>

<p>Even though both datasets may contain signals related to <strong>hypoglycemia</strong>, they use <strong>completely
        different column names</strong> (<code>blood_sugar_lvl</code> vs <code>hypoglycemia_flag</code>), and reside in
    <strong>tables with different semantics</strong>.</p>

<p>This variability makes it hard to write consistent code or perform federated analysis using tools like
    <strong>OHDSI's ATLAS</strong> or <strong>CohortMethod</strong>.</p>

<h2> Our Approach: LLM-Based Schema Mapping</h2>

<p>Instead of manually mapping or relying on syntax-based rules (which often fail when names are semantically distant),
    we used an <strong>LLM</strong> to understand the <strong>intent and semantics</strong> of the source schema and map
    it to OMOP CDM.</p>

<h3> Why not syntax-based mapping?</h3>

<p>Let’s take this example:</p>

<ul>
    <li>Source column: <code>blood_sugar_lvl</code></li>
    <li>OMOP CDM column: <code>condition_concept_id</code> (in the <code>CONDITION_OCCURRENCE</code> table)</li>
</ul>

<p>A naive string-matching approach might completely miss the connection. But an LLM understands that <em>"blood sugar
        level"</em> is conceptually related to <em>"hypoglycemia"</em> and should be represented as a
    <strong>condition</strong> in OMOP — not just a numeric observation.</p>

<h2>⚙️ How It Works</h2>

<p>The pipeline follows a <strong>Retrieve-Augment-Generate (RAG)</strong> framework:</p>

<ol>
    <li><strong>Input</strong>: Column names and table names from a non-OMOP source dataset.</li>
    <li><strong>Retrieval</strong>: Before querying the LLM, we <strong>augment the prompt with OMOP CDM
            schemas</strong>, including table and field descriptions from official documentation.</li>
    <li><strong>Prompting</strong>: The LLM is then prompted to map each source column to:
        <ul>
            <li>A target <strong>OMOP CDM table</strong></li>
            <li>The corresponding <strong>column</strong> in that table</li>
            <li>(Optional) A confidence score or rationale</li>
        </ul>
    </li>
    <li><strong>Output</strong>: A suggested mapping like:</li>
</ol>

<pre><code>{
  "blood_sugar_lvl": {
    "omop_table": "CONDITION_OCCURRENCE",
    "omop_column": "condition_concept_id"
  }
}
  </code></pre>

<p>By injecting the <strong>CDM schema into the context</strong> (RAG), we minimize hallucinations and improve the
    accuracy of mappings — especially for less obvious fields.</p>

<h2>🧪 What Makes This Novel?</h2>

<ul>
    <li> <strong>No need for identical naming</strong>: Unlike traditional ETL tools, the LLM doesn't rely on string
        similarity.</li>
    <li> <strong>Semantic reasoning</strong>: It understands the <strong>meaning</strong> behind terms, allowing
        better alignment even when naming is vague or domain-specific.</li>
    <li><strong>Schema-aware generation</strong>: By passing CDM schema descriptions into the prompt, we make the LLM
        more grounded in what tables and fields actually exist in OMOP.</li>
</ul>

<h2>Example Result</h2>

<h3>Source Schema:</h3>
<pre><code>Table: lab_results
Columns: patient_id, blood_sugar_lvl, lab_date
</code></pre>

<h3>LLM Output:</h3>
<pre><code>{
  "blood_sugar_lvl": {
    "omop_table": "MEASUREMENT",
    "omop_column": "value_as_number"
  },
  "lab_date": {
    "omop_table": "MEASUREMENT",
    "omop_column": "measurement_date"
  }
}
</code></pre>

<p><strong>Interpretation</strong>: The LLM correctly identifies that blood sugar is <em>not a condition</em>, but a
    <em>measurable lab result</em>, and places it in the <code>MEASUREMENT</code> table — a subtle but crucial
    distinction.</p>

<h2>What’s Next?</h2>

<ul>
    <li> <strong>Full ETL Automation</strong>: Use LLM-based mappings to generate
        <code>INSERT INTO ... SELECT ...</code> SQL automatically.</li>
    <li> <strong>Cross-lingual Mapping</strong>: Apply the same idea to non-English datasets.</li>
    <li><strong>Round-trip validation</strong>: Check LLM-generated mappings using domain knowledge or
        back-validation with real patient data.</li>
</ul>

<h2>Takeaway</h2>

<p>LLMs can be more than chatbots — they can become <strong>semantic translators</strong> for messy real-world data. By
    combining <strong>RAG-based prompting</strong> with <strong>schema-aware design</strong>, we can build intelligent
    systems that help bridge the gap between non-standard medical data and OMOP CDM — enabling scalable, reproducible
    research for all.</p>
