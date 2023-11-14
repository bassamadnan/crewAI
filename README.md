# CrewAI

🤖 Cutting-edge framework for orchestrating role-playing, autonomous AI agents. By fostering collaborative intelligence, CrewAI empowers agents to work together seamlessly, tackling complex tasks.

## Why CrewAI?

The power of AI collaboration has too much to offer.
CrewAI is designed to bridge to enable AI agents to assume roles, share goals, and operate in a cohesive unit - much like a well-oiled crew. Whether you're building a smart assistant platform, an automated customer service ensemble, or a multi-agent research team, CrewAI provides the backbone for sophisticated multi-agent interactions.

## Getting Started

To get started with CrewAI, follow these simple steps:

1. **Installation**:

```shell
pip install crewai
```

2. **Setting Up Your Crew**:

```python
from crewai import Agent, Task, Crew, Process

# Define your agents with roles and goals
researcher = Agent(role='Researcher', goal='Discover new insights')
writer = Agent(role='Writer', goal='Create engaging content')

# Create tasks for your agents
task1 = Task(description='Investigate the latest AI trends', agent=researcher)
task2 = Task(description='Write a blog post on AI advancements', agent=writer)

# Instantiate your crew with a sequential process
crew = Crew(
  agents=[researcher, writer],
  tasks=[task1, task2],
  process=Process.sequential
)

# Get your crew to work!
crew.kickoff()
```

## Key Features

- **Role-Based Agent Design**: Customize agents with specific roles, goals, and tools.
- **Autonomous Inter-Agent Delegation**: Agents can autonomously delegate tasks and inquire amongst themselves, enhancing problem-solving efficiency.
- **Flexible Task Management**: Define tasks with customizable tools and assign them to agents dynamically.
- **Processes Driven**: Currently only supports `sequential` task execution but more complex processes like consensual and hierarchical being worked on.

![CrewAI Mind Map](/crewAI-mindmap.png "CrewAI Mind Map")


## How CrewAI Compares

- **Autogen**: While Autogen excels in creating conversational agents capable of working together, it lacks an inherent concept of process. In Autogen, orchestrating agents' interactions requires additional programming, which can become complex and cumbersome as the scale of tasks grows.

- **ChatDev**: ChatDev introduced the idea of processes into the realm of AI agents, but its implementation is quite rigid. Customizations in ChatDev are limited and not geared towards production environments, which can hinder scalability and flexibility in real-world applications.

**CrewAI's Advantage**: CrewAI is built with production in mind. It offers the flexibility of Autogen's conversational agents and the structured process approach of ChatDev, but without the rigidity. CrewAI's processes are designed to be dynamic and adaptable, fitting seamlessly into both development and production workflows.

## Contribution

CrewAI is open-source and we welcome contributions. If you're looking to contribute, please:

- Fork the repository.
- Create a new branch for your feature.
- Add your feature or improvement.
- Send a pull request.
- We appreciate your input!

### Installing Dependencies
```bash
poetry lock
poetry install
```

### Virtual Env
```bash
poetry shell
```

### Running Tests
```bash
poetry run pytest
```

### Packaging
```bash
poetry build
```

### Installing Locally
```bash
pip install dist/*.tar.gz
```

## License
CrewAI is released under the MIT License

