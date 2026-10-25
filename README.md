<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Custom Agent Harness

**Project Link:** [View Project](https://nextwork.ai/projects/fbd360ae-3944-42e5-8cc2-2a8a8d6a55b8)

**Author:** Nessim Saidani  

---

![Image](https://nextwork.ai/nessim/uploads/fbd360ae-3944-42e5-8cc2-2a8a8d6a55b8_lryaaeda)

## Defining the Harness and Client Boundary

### Separating harness responsibilities from the thin client

I'm creating a costum agent harness to learn how model can verify the changes and use diffrent tools

## Launching a Thin Terminal Adapter

### Preparing the starter TUI for harness exploration

In this step, I'm setting up tbe starter TUI so that I can verify the supported node.js and configure local access

![Image](https://nextwork.ai/nessim/uploads/fbd360ae-3944-42e5-8cc2-2a8a8d6a55b8_qb82ejyk)

### Keeping interface responsibilities out of the runtime

The TUI handles user interactionwhile the agent harness handles backend , communication and openrouter model 

## Creating Provider-Independent Model Contracts

### Defining message, tool, and adapter contracts

In this step, I'm defining types so that I can communicate between my UI , harness and models 

### Protecting the TUI from provider-specific response types

The shared types keep messaging consistent between TUI and agent harness while the adapter handles communicating withg OpenRouter 

![Image](https://nextwork.ai/nessim/uploads/fbd360ae-3944-42e5-8cc2-2a8a8d6a55b8_9obbg321)

### Recognizing the limits of a model without tools

I observed that the adapter can try to do the task but cannot accés the tools

## Orchestrating a Stateful Agent Runtime

### Building the model, tool, and message loop

In this step, I'm building the agent loop so that I can call the tools and move the message trace into the composition root 

![Image](https://nextwork.ai/nessim/uploads/fbd360ae-3944-42e5-8cc2-2a8a8d6a55b8_xcef8l3r)

### Preserving conversation state across submissions

The message trace is stored in the message of the main function of 'src/index.ts' and updated after we get the reesult from runAgent()

## Grounding Workspace Insights with Read-Only Tools

### Adding bounded workspace inspection capabilities

In this step, I'm adding read-only tools so that the harness can read files inside my local file system

![Image](https://nextwork.ai/nessim/uploads/fbd360ae-3944-42e5-8cc2-2a8a8d6a55b8_0lxjl2nj)

### Defining capabilities through the tool registry

The harness can perform actions that read file , list directories and search text but not the actions that requires changing file of texts

## Executing Changes Through Approval-Gated Tools

### Adding consequential tools behind a policy boundary

In this step, I'm adding consequential tools behind approval policy so that I can update local file afteer reviewing changes 

### Requiring approval before workspace changes and commands

The harness requests approval through the CLI before running tools in the agent loop

## Persisting Agent Context Across Client Restarts

![Image](https://nextwork.ai/nessim/uploads/fbd360ae-3944-42e5-8cc2-2a8a8d6a55b8_vn0q5kj4)

### Saving session history outside the bounded workspace

In this project extension, the session survives because it stores the conversation in a JSON file 

## Reflecting on the Agent Harness Build

### Tools and concepts developed

The key tools I used include openrouter and typescript Key concepts I learnt include agent harness , tool calling , agent loop and guardrails .

### Project timeline and challenges

This project took me approximately two hours The most challenging part was debugging and setting up the tools

### Next steps in agent engineering

I did this project today to learn how to build an custom agent Another skill I want to learn is how to deploy the agents and extand its tools 

---

*Built with [NextWork](https://nextwork.ai) - [View this project](https://nextwork.ai/projects/fbd360ae-3944-42e5-8cc2-2a8a8d6a55b8)*
