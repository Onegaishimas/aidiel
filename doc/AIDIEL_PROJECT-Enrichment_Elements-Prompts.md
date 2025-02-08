## AI Use Case Analysis Enhancement Prompts

## Problem Statement [`problem_statement`]

This prompt generates a structured problem statement for the AI use case.

### Prompt Template
```
User: You are an advanced artificial intelligence assistant. Your task is to craft effective problem statements using clarity, specificity, and alignment with operational goals. Read the provided <AI_Use_Case_Details> and write a problem statement to meet the following criteria:

Begin with "The problem is..." or "Currently...".
Clearly describe what issue or challenge needs to be addressed.
Explain why this is significant, providing relevant context.
Identify who is affected by this problem and how.
Ensure the statement is concise, avoids verbosity, and focuses exclusively on articulating the problem (not solutions).

Example Effective Problem Statement: Current cargo inspection methods are labor-intensive and prone to human error, limiting their ability to process the growing volume of containers efficiently. This inefficiency impacts resource allocation and delays timely identification of contraband or security risks.

<AI_Use_Case_Details>
*Use Case Name: {{ $json.use_case_name }}
*Agency: {{ $json.agency }}
*Agency Abbreviation: {{ $json["abr"] }}
*Bureau: {{ $json.bureau }}
*Use Case Topic Area: {{ $json.topic_area }}
*Is the AI use case found in the below list of general commercial AI products and services?: {{ $json.commercial_ai }}
*What is the intended purpose and expected benefits of the AI?": {{ $json.purpose_benefits }}
*Describe the AI system's outputs.: {{ $json.outputs }}
*Is the AI use case Safety or Rights impacting?: {{ $json.sri }}
</AI_Use_Case_Details>

Output: Write the problem_statement with clarity, specificity, and relevance while adhering to the above criteria.
```

## Solution Assertion [`solution_assertion`]

This prompt generates a comprehensive solution description based on the problem statement and use case details.

### Prompt Template
```
User: A chat between a serious user and an artificial intelligence assistant. The assistant provides expert articulation of relevant aspects of AI use cases based on a modicum of input information. Write a 250-word "solution assertion" that incorporates and addresses the information in <AI_Use_Case_Details> using the format in <template>...being mindful of the problem statement in <problem_statement>...ensuring clarity, consistency, and alignment with operational goals.

<AI_Use_Case_Details>
*Use Case Name: {{ $json.use_case_name }}
*Agency: {{ $json.agency }}
*Agency Abbreviation: {{ $json["abr"] }}
*Bureau: {{ $json.bureau }}
*Use Case Topic Area: {{ $json.topic_area }}
*Is the AI use case found in the below list of general commercial AI products and services?: {{ $json.commercial_ai }}
*What is the intended purpose and expected benefits of the AI?": {{ $json.purpose_benefits }}
*Describe the AI system's outputs.: {{ $json.outputs }}
*Is the AI use case Safety or Rights impacting?: {{ $json.sri }}
</AI_Use_Case_Details>

<template>
Solution Description:
Provide a concise overview of the AI-enabled solution, explicitly stating the problem it addresses and the technologies involved. Describe how the solution integrates into existing workflows and how it improves operational efficiency.

AI-Driven Approach:
Detail the specific AI technologies used (e.g., machine learning, natural language processing, computer vision) and how they function to solve the problem. Highlight innovative features or unique capabilities that contribute to the solution's effectiveness.

Measurable Impacts:
- Increased Accuracy: Describe how the solution improves accuracy or precision in addressing the problem.
- Reduced Processing Times: Explain how the solution saves time or improves efficiency.
- Resource Optimization: Highlight how the solution optimizes resources, such as personnel or materials.
- Operational Efficiency: Discuss how the solution integrates seamlessly into workflows and enhances decision-making.

Solution Summary:
- Problem Addressed: Clearly state the core issue the solution targets.
- AI-Driven Approach: Briefly describe the AI methodologies used to solve the problem.
- Measurable Benefits: Summarize the tangible outcomes of the solution.
</template>

<problem_statement>
{{ $json.problem_statement }}
</problem_statement>
```

## Value Category and Rationale [`value_category`, `value_category_rationale`]

This prompt categorizes the AI use case and provides detailed justification for the categorization.

### Prompt Template
```
User: You are an advanced AI assistant tasked with categorizing AI use cases into one of three value categories. Your response must adhere to the structure and formatting provided below, ensuring a detailed, insightful, and contextually accurate justification. Analyze the provided use case details, focusing on the core transformative impact of the AI solution.

Value Categories:

Efficiency Amplifier: Streamlines existing processes, reduces resource consumption, or improves speed and accuracy within current workflows.

Capability Enhancer: Introduces new capabilities, expands operational boundaries, or enables tasks previously constrained by resource or technical limitations.

Breakthrough Enabler: Achieves novel outcomes, redefines operational paradigms, or transcends traditional limitations entirely.

Instructions:
1. Carefully review the provided use case details, including the problem statement, solution assertion, outputs, and intended benefits.
2. Determine the single value category—Efficiency Amplifier, Capability Enhancer, or Breakthrough Enabler—that best represents the primary transformative impact of the AI solution.
3. Provide a detailed, structured justification for your categorization in 300 words, citing 3-4 specific points from the use case.
4. Ensure that the justification directly connects the use case's unique features to the selected category, avoiding overlap or ambiguity.

Input:
Problem Statement: {{ $json.problem_statement }}
Use Case Name: {{ $json.use_case_name }}
Agency: {{ $json.agency }}
Bureau: {{ $json.bureau }}
Use Case Topic Area: {{ $json.topic_area }}
Intended Purpose and Expected Benefits: {{ $json.purpose_benefits }}
AI System Outputs: {{ $json.outputs }}
Safety or Rights Impact: {{ $json.sri }}
Solution Assertion: {{ $json.solution_assertion }}

Response Template:

CATEGORY: <Efficiency Amplifier | Capability Enhancer | Breakthrough Enabler>  

## Rationale:  
Provide a structured narrative that includes:
1. **Introduction**: State the selected value category and explain why it applies to this AI use case.
2. **Point 1**: Describe a specific feature or functionality of the solution and its transformative impact.
3. **Point 2**: Highlight how the AI expands or optimizes operational boundaries or efficiencies.
4. **Point 3**: Explain the measurable or qualitative outcomes that support this categorization.
5. **Conclusion**: Summarize how the selected category best represents the core impact of the AI solution.

### Example:
CATEGORY: Capability Enhancer  

The AI-driven Non-Intrusive Inspection (NII) 3D Imaging Tool is categorized as a "Capability Enhancer" because it introduces advanced capabilities that extend beyond traditional imaging methods. It provides high-resolution, 3D imaging for detailed analysis, overcoming limitations of two-dimensional systems. Machine learning algorithms trained on contraband patterns empower agents to identify hidden narcotics accurately, enhancing operational reach and speed. This seamless integration into existing workflows exemplifies its role as a capability-expanding tool.

Requirements:
- The value category must be exactly one of: "Efficiency Amplifier," "Capability Enhancer," or "Breakthrough Enabler."
- Avoid generic statements; ground your analysis in specific details from the use case.
- Ensure clarity, precision, and logical consistency in your justification.
```

## Technical Elements [`technical_elements`]

This prompt analyzes the technical components and requirements of the AI solution.

### Prompt Template
```
User: Based on the provided use case details, analyze and identify the technical elements required for this AI solution. Consider both AI/ML components and supporting infrastructure.

Please analyze the technical elements across these categories:
1. Data Elements: Input data requirements, data flows, data storage/processing needs
2. AI/ML Components: Models, algorithms, training requirements, inference needs
3. Infrastructure Components: Computing resources, networking, storage, security requirements
4. Integration Elements: APIs, interfaces, data exchange requirements
5. Operational Requirements: Monitoring, maintenance, scaling considerations

Provide your response in this structure:

##Technical Architecture Overview:
Analyze how the different technical components work together to deliver the solution, including:
- High-level architecture description
- Key technical dependencies
- Critical system interactions
- Performance considerations
- Security and compliance requirements

##Technical Components List
COMPONENTS:
- Data: [comma-separated list of data components and requirements]
- AI/ML: [comma-separated list of AI/ML components and requirements]
- Infrastructure: [comma-separated list of infrastructure components]
- Integration: [comma-separated list of integration requirements]
- Operations: [comma-separated list of operational requirements]

##Implementation Considerations:
Describe the key technical considerations and challenges that need to be addressed for successful implementation, including:
- Technical risks and mitigations
- Critical dependencies
- Performance requirements
- Security requirements
- Scaling considerations

<AI_Use_Case_Details>
*Problem Statement that inspired the AI Use Case: {{ $json.problem_statement }}
*Use Case Name: {{ $json.use_case_name }}
*Agency: {{ $json.agency }}
*Bureau: {{ $json.bureau }}
*Use Case Topic Area: {{ $json.topic_area }}
*What is the intended purpose and expected benefits of the AI?": {{ $json.purpose_benefits }}
*Describe the AI system's outputs.: {{ $json.outputs }}
*Is the AI use case Safety or Rights impacting?: {{ $json.sri }}
*Solution Assertion: {{ $json.solution_assertion }}
*Value Category: {{ $json.value_category }}
*Value Category Rationale: {{ $json.value_category_rationale }}
</AI_Use_Case_Details>

Remember: Focus on identifying all necessary technical components while considering:
- Alignment with stated problem and solution
- Support for identified stakeholder needs
- Appropriateness for value category
- Technical feasibility and scalability
- Security and compliance requirements

IMPORTANT: The COMPONENTS: section must be included exactly as formatted above for automated processing.
```

## Stakeholders [`stakeholders`]

This prompt generates a comprehensive stakeholder analysis for the AI use case.

### Prompt Template
```
Review the information provided in <AI_Use_Case_Details>:

<AI_Use_Case_Details>
*Use Case Name: {{ $json.use_case_name }}
*Agency: {{ $json.agency }}
*Bureau: {{ $json.bureau }}
*Use Case Topic Area: {{ $json.topic_area }}
*Intended Purpose and Expected Benefits: {{ $json.purpose_benefits }}
*AI System Outputs: {{ $json.outputs }}
*Safety or Rights Impact: {{ $json.sri }}
*Problem Statement: {{ $json.problem_statement }}
*Solution Assertion: {{ $json.solution_assertion }}
*Value Category: {{ $json.value_category_rationale }}
*Value Category Rationale: {{ $json.value_category_rationale }}
*Technical Elements {{ $json.technical_elements}}
</AI_Use_Case_Details>

Based on the AI use case provided in <AI_Use_Case_Details>, analyze the AI use case and generate a comprehensive stakeholder analysis following the standardized template. For each section:

1. Identify specific roles and responsibilities rather than generic groups
2. Detail clear relationships and dependencies between stakeholders

Stakeholder Analysis

Mission Interests:
- Subject Matter Experts: [Domain specialists]
- Field Personnel: [Operational staff]
- Supervisory Staff: [Managerial roles]

External Stakeholders:
- Partner Agencies: [Collaborating organizations]
- Regulated Entities or Demographics: [Regulatory/compliance/Law Enforcement entities]
- Private Sector Interests: [Economic, bureaucratic, public service intersections]
- Public Impact: [Affected populations]
```
