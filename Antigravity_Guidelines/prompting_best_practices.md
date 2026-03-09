# File: prompting_best_practices.md  
  
# Antigravity Prompting Best Practices  
  
This document captures prompting patterns that improve reliability, clarity, and reproducibility when interacting with agents inside the Antigravity environment.  
  
These guidelines were observed during early experimentation with agent-assisted prototyping workflows.  
  
---  
  
## 1. Prefer Structured Context Over Long Prompts  
  
Agents perform better when important information is stored in project files rather than repeatedly embedded in prompts.  
  
Instead of writing long prompts that restate system details, store the information in persistent files.  
  
Example project structure:  
  
```  
Prototype_Context/  
Agentic_Prototyping.md  
Brief.md  
CTO_Brief.md  
```  
  
Then prompts can reference the files directly:  
  
```  
Refer to Prototype_Context/Brief.md and summarize the architecture.  
```  
  
This improves consistency and reduces token usage.  
  
---  
  
## 2. Separate Context, Task, and Output  
  
Prompts should clearly separate the following components:  
  
- Context  
- Task  
- Expected Output  
  
Example structure:  
  
```  
Context:  
Refer to Prototype_Context/Brief.md  
  
Task:  
Analyze the system architecture.  
  
Output:  
- architecture overview  
- key components  
- recommended next step  
```  
  
This structure improves reasoning quality and reduces ambiguity.  
  
---  
  
## 3. Keep Prompts Task-Oriented  
  
Agents perform best when prompts request a single focused action.  
  
Good example:  
  
```  
Analyze the Prototype_Context folder and summarize the prototype concept.  
```  
  
Bad example:  
  
```  
Analyze the prototype, propose architecture, generate tasks, and evaluate maturity models.  
```  
  
Breaking work into smaller prompts improves agent reasoning and reliability.  
  
---  
  
## 4. Maintain Stable System Instructions  
  
Agent prompts should maintain a consistent system role whenever possible.  
  
Example system role:  
  
```  
You are an Antigravity agent responsible for analyzing project context and maintaining timeline records.  
```  
  
Keeping system instructions stable helps improve prompt caching and reduces token overhead.  
  
---  
  
## 5. Provide Explicit Output Formats  
  
When requesting analysis, define the expected structure of the response.  
  
Example:  
  
```  
Output Format:  
- Summary  
- Key Observations  
- Recommended Next Action  
```  
  
This reduces hallucinations and improves response consistency.  
  
---  
  
---