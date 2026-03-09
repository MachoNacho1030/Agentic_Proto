# Agentic Prototype Story  
**Developer:** Sebastian Joshi  
**Context:** Early-stage exploration of agentic prototyping workflows within the CTO Org

---

# Background

While reviewing internal discussions about emerging AI development tools and the maturity of agentic coding ecosystems, leadership requested that the team maintain awareness of the broader landscape.

Specifically, the team was asked to track research and literature related to:

- agentic coding frameworks  
- programming language maturity in AI-assisted development  
- benchmark results across ecosystems  
- implications for SAP and ABAP development

The request emphasized periodically reassessing the **“meta-state of affairs”** of the ecosystem.

This sparked the idea to explore whether an **agent-assisted workflow could structure this research automatically**.

Rather than manually tracking articles, benchmarks, and blog posts, I wanted to see if an AI agent could help generate a **structured prototype concept** that could evolve into a lightweight research intelligence system.

---

# Original Leadership Prompt

The following prompt served as the starting point for the exploration:

> Request from Bryan, especially as Joe, Brian and Leo look into Antigravity and other tools:  
>  
> “please have the team keep up on literature reviews to understand the meta-state of affairs. I've generally told others in leadership that the non-ABAP programming languages are more mature when it comes to Agentic/vibe coding. I think the article below somewhat reinforces that, but we ought to be thinking in quarterly or some other refresh frequency to revalidate.”  
>
> SAP’s ABAP-1 Loses Every ABAP Benchmark, Even “Explaining” | Marian Zeis Blog

---

# Observing an Opportunity

After seeing this request, I realized there was an opportunity to test an **agentic prototyping workflow**.

Instead of approaching the request as a traditional research task, I experimented with using an AI prototype assistant to:

1. Interpret the leadership request
2. Ask clarifying questions
3. Generate a structured prototype brief
4. Translate the problem into a potential lightweight system

The goal was not to immediately build software, but to explore the **first stage of agentic prototyping**:


---

# Initial Experiment

Using an internal prototype assistant ("Prototype Brief Coach"), created by Brian Smith - something we all have access to - I provided the context and allowed the agent to guide the process.

The agent asked a sequence of questions about:

- intended users
- success metrics
- data sources
- system architecture
- reporting outputs

Through iterative clarification, the conversation produced a structured prototype brief for a potential internal tool.

[[Brief ]]

---

# Resulting Prototype Concept

The proposed concept was a lightweight **Agentic Coding Maturity Intelligence Dashboard**.

Its purpose would be to:

- ingest literature related to agentic coding ecosystems
- tag research by programming language and framework
- track benchmarks and ecosystem maturity
- generate quarterly briefings for leadership

Instead of manually producing literature reviews, the system would organize research and generate structured summaries.

Conceptually, the system workflow would look like:

new research  
↓  
weekly ingestion  
↓  
tagging (language, framework, benchmark)  
↓  
dashboard organization  
↓  
quarterly briefing generation


---

# Why This Experiment Matters

This exercise served as an early example of **agentic prototyping**.

Rather than starting with code, the agent was used to convert a vague request into a structured concept document that included:

- problem definition
- user roles
- success metrics
- MVP scope
- data model
- system workflows

This step helps reduce ambiguity before any engineering work begins.

---

# Takeaway

The experiment demonstrated how AI agents can assist with the **idea-to-spec stage** of prototyping.

Instead of jumping directly into development, the workflow becomes:

leadership request  
↓  
agent-assisted idea structuring  
↓  
prototype brief  
↓  
architecture exploration  
↓  
prototype build

# Why I Used Antigravity

After generating the prototype brief with the AI assistant, I wanted to test how an **agentic development environment** could manage the context and evolution of the idea.

Antigravity provided a useful environment to experiment with this because it allows agents to reason over structured project context and maintain an operational history of actions taken.

Rather than keeping the prototype discussion as a single conversation artifact, I organized the information into two key components within the Antigravity workspace.

## Prototype Context

I created a folder called: Prototype_Context


This folder contains the foundational documents that describe the prototype concept:

- the **original leadership request**
- the **agent-generated prototype brief**
- the **story documenting how the idea emerged**

These files serve as the **static context layer** of the prototype, giving the agent a clear understanding of the problem, scope, and intended outcome.

## Antigravity Timeline

To allow the agent to maintain memory of its actions, I also created a folder called:
Antigravity_Timeline


Inside this folder, the agent records a log of:

- requests made to the agent
- actions performed
- the agent’s analysis of the situation

This acts as a form of **operational memory**, allowing the system to track how the prototype evolves over time.

## Purpose of This Setup

The goal of structuring the workspace this way was to test a simple pattern for **agentic prototyping workflows**:
prototype context → agent reasoning → timeline memory → iterative development


By separating the **context layer** (documents describing the system) from the **timeline layer** (records of agent activity), the agent can reason about both the design of the system and the history of how it was developed.

This approach helps create a more structured and inspectable environment for experimenting with agent-assisted development.

# Expanding the Antigravity Environment

After establishing the initial prototype context and timeline logging, I wanted to further structure the environment to support consistent agent interactions.

While experimenting with Antigravity, it became clear that agent systems perform better when they operate within clearly defined operational guidelines. Without these guidelines, prompts can become inconsistent, overly long, or inefficient in terms of token usage.

To address this, I introduced an additional folder within the Antigravity workspace:

```
antigravity_guidelines/
```

This folder contains documentation describing best practices for interacting with the agent environment.

The goal of this folder is to provide reusable guidance for both humans and agents when working within the repository.

The guidelines currently focus on three areas:

- **Prompting Best Practices** – how to structure prompts clearly and consistently
- **Token Efficiency** – strategies for minimizing unnecessary token usage
- **Context Engineering** – how project context should be organized so the agent receives the right information at the right time

These documents allow the agent to reference stable instructions rather than repeatedly receiving large prompt explanations during interactions.

Conceptually, the project structure now separates three different concerns:

```
Prototype_Context/
    system knowledge and design documents

Antigravity_Timeline/
    historical record of agent actions and analysis

Antigravity_Guidelines/
    operational best practices for prompting and context management
```

This structure creates a clearer agent workflow environment where:

- the **context layer** defines what the system is
- the **timeline layer** records what has happened
- the **guidelines layer** defines how the agent should operate

This separation helps improve both agent reasoning and token efficiency while keeping the experiment organized and reproducible.

# Introducing Skills and Tasks

After establishing the core Antigravity environment — including the **Prototype_Context**, **Antigravity_Timeline**, and **Antigravity_Guidelines** folders — the next step was to introduce a more structured execution model for the agent.

While the initial setup allowed the agent to understand the system context and maintain a record of its actions, it did not yet define **what the agent should actually do next** or **how it should perform specific types of work**.

To address this, two additional folders were introduced:

```
skills/
tasks/
```

These folders represent two key components of an agentic workflow.

---

## Tasks: What the Agent Should Do

The **tasks** folder acts as a task queue for the agent. Each file represents a discrete unit of work that the agent can analyze and execute.

A task file typically defines:

- the objective of the task
- relevant inputs or context
- expected outputs
- current status

For example, a task might instruct the agent to identify literature sources related to agentic coding ecosystems or extract benchmark insights from a research paper.

By explicitly defining tasks, the agent gains a clear sense of **what work remains to be done**. This prevents the agent from repeatedly analyzing context without progressing toward concrete outcomes.

---

## Skills: How the Agent Performs Work

The **skills** folder defines repeatable capabilities the agent can apply when executing tasks.

Each skill documents a specific type of analysis or operation the agent may need to perform. Examples include:

- literature analysis
- benchmark extraction
- ecosystem comparison

Rather than improvising a new approach each time, the agent can reference these skill documents to understand **how a task should be completed and what form the output should take**.

This improves consistency and makes agent behavior easier to reproduce and evaluate.

---

## Combining Context, Memory, Skills, and Tasks

With the introduction of the **skills** and **tasks** folders, the Antigravity workspace now follows a more complete agent workflow structure.

```
Prototype_Context/
    Defines what the system is

Antigravity_Timeline/
    Records what has happened

Antigravity_Guidelines/
    Describes how agents should operate

Skills/
    Defines what the agent knows how to do

Tasks/
    Defines what the agent should do next
```

This structure allows the agent to reason through a clear operational loop:

```
load context
→ review timeline
→ select task
→ apply skill
→ record results
```

By separating these responsibilities into different folders, the environment becomes easier for both humans and agents to navigate, while also making the experimentation process more structured and reproducible.

# Introducing a Repository Map

As the Antigravity workspace began to grow, it became clear that the environment now contained multiple folders serving different purposes. While the structure made sense from a development perspective, an agent interacting with the repository would not automatically understand the role of each folder or how the pieces fit together.

To address this, I introduced a file called:

repo_map.md

The purpose of this file is to act as a **navigation guide for the agent**, explaining the structure of the repository and the role of each directory.

Without a repository map, an agent entering the environment would need to infer the purpose of each folder by reading files individually. This can lead to inefficient reasoning, unnecessary file reads, and increased token usage. By providing a clear description of the repository layout in a single document, the agent can quickly understand how the workspace is organized.

The repository map explains the responsibilities of each layer of the project, including:

- **Prototype_Context** – foundational documentation describing the system and the original prototype brief
- **Antigravity_Timeline** – a historical record of requests, actions, and analyses performed by the agent
- **Antigravity_Guidelines** – operational best practices for prompting, token efficiency, and context management
- **Skills** – reusable capabilities the agent can apply when performing analysis
- **Tasks** – specific work items the agent should execute

Providing this overview allows the agent to understand the environment before performing any work. The agent can read the repository map, locate the relevant folders, and follow the intended workflow without needing to rediscover the project structure each time.

Conceptually, the repository map acts as a **table of contents for the entire agent environment**, helping both humans and agents navigate the workspace more efficiently.