# AI Use Case TOPIC|CONTEXT|QUESTION|ANSWER (tcqa) group prompts

This prompt generates five tcqa groups per use case derived from the use case's repective improvement elements.

The prompt is the same for all six improvement elements, except for the third element in the AI Use Case Details block.

The following version is specific to - **Problem Statement:** {{$json["problem_statement"]}}

### Prompt Template

```
Generate exactly **five** structured "Topic | Context | Question | Answer" groups based on the provided AI use case details. 
Ensure strict adherence to the following format:

---
### **Topic:** [Insert Topic Here]
**Context:** [Provide a brief description of the background and significance.]
**Question:** [Provide a clear, structured question related to the AI use case.]
**Answer:** [Provide a structured and informative answer.]
### END ###
---

**AI Use Case Details:**
- **Use Case ID:** {{$json["use_case_Id"]}}
- **Use Case Name:** {{$json["use_case_name"]}}
- **Problem Statement:** {{$json["problem_statement"]}}

⚠️ IMPORTANT: 
- Do **not** include introductory or concluding text.
- Abstract and generalize references to specific agency(s), bureau(s), and other specific organizational considerations.
- Abstract and generalize references to activities and goals in terms of specific missions.  
- Ensure each `Topic`, `Context`, `Question`, and `Answer` appears on a separate line.
- Separate each group using `### END ###`.
- The response **must** contain exactly five structured groups.

Assistant:
```




