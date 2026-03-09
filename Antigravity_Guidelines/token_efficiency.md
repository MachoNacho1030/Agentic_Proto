# File: token_efficiency.md  
  
# Token Efficiency Guidelines for Antigravity  
  
Efficient token usage improves agent performance, reduces latency, and lowers computational cost.  
  
This document describes practical techniques for reducing unnecessary token consumption.  
  
---  
  
## 1. Use Retrieval Instead of Context Dumping  
  
Avoid sending entire project context into prompts.  
  
Instead, retrieve only the relevant files.  
  
Bad example:  
  
```  
Analyze everything in the Prototype_Context folder.  
```  
  
Better example:  
  
```  
Refer to Prototype_Context/Brief.md and analyze the architecture section.  
```  
  
This approach minimizes unnecessary token usage.  
  
---  
  
## 2. Summarize Long Memory Logs  
  
Agent timelines can grow very large over time.  
  
Instead of loading the entire timeline into prompts, older entries should be summarized.  
  
Example pattern:  
  
```  
Recent entries → detailed  
Older entries → summarized  
```  
  
Example timeline summary:  
  
```  
Timeline Summary  
- Initial prototype concept generated  
- Context folder created  
- Dashboard architecture proposed  
```  
  
This keeps context small while preserving historical information.  
  
---  
  
## 3. Avoid Repeating Static Information  
  
Static project information should live in files rather than prompts.  
  
Examples of static information:  
  
- project goals  
- architecture descriptions  
- maturity models  
- system instructions  
  
By storing these in files, agents can reference them without repeating tokens in each interaction.  
  
---  
  
## 4. Prefer References Over Copying  
  
Use file references instead of copying content into prompts.  
  
Example:  
  
```  
Refer to Prototype_Context/CTO_Brief.md  
```  
  
instead of pasting the entire document.  
  
---  
  
## 5. Trim Irrelevant Context  
  
Only include information relevant to the current task.  
  
Large prompts with unrelated content can degrade model performance.  
  
The goal is to provide:  
  
```  
maximum signal  
minimum tokens  
```  
  
---  
  
---