# Agent Game Maker

Welcome to **Agent Game Maker**! This tool leverages AI assistance to help you create quick, simple Pygame projects effortlessly. Designed as an example project, it demonstrates how multi-agent systems can streamline development workflows. 

## Table of Contents
- [Introduction](#introduction)
- [How It Works](#how-it-works)
- [Cost](#cost)
- [Installation](#installation)
- [Usage](#usage)
- [Example Project](#example-project)
- [Development Journey](#development-journey)
- [Learnings and Challenges](#learnings-and-challenges)
- [What’s Next](#whats-next)
- [Contributing](#contributing)
- [License](#license)

## Introduction

**Agent Game Maker** is a Python application that utilizes multi-agent systems to collaboratively design and develop Pygame projects. By interacting with these AI agents, users can describe the game they envision, and the system autonomously handles the planning, file generation, error handling, and iterative improvements. This tool exemplifies how intelligent automation can empower developers to focus on creativity while the system manages the technical complexities of game development.

## How It Works

1. **User Input:** Begin by describing the Pygame game you wish to create. Provide details such as game type, mechanics, visual elements, and any specific features you desire.

2. **AI Planning:** The system initiates multiple planning iterations where AI agents discuss and outline the project structure. This ensures a logical and playable game design, emphasizing clean architecture and maintainable code.

3. **File Generation:** Based on the AI-generated project plan, the tool automatically creates the necessary Python files within the `app` directory. Each file is meticulously crafted to align with best practices and the specified game mechanics.

4. **Error Handling:** The system runs the game and captures any runtime errors. If errors are detected, AI agents analyze the issues and attempt to fix them iteratively, enhancing the game's stability and performance.

5. **Feedback Loop:** Users can provide feedback on the game, prompting further refinements and enhancements by the AI agents. This iterative process ensures continuous improvement and alignment with user expectations.

This workflow showcases the seamless integration of event-driven architecture with sophisticated AI agents, embodying our core philosophy of creating powerful and accessible systems through intelligent automation.

## What This Sample Doesn't Have

- Type validation
- Agent frameworks
- Model configuration
- Frontend interface
- Data persistence
- Dynamic prompting
- Agent Routing
- Updated XML file

## Cost

The cost of using **Agent Game Maker** ranges between **$0.50 to $2.00** per project, depending on the number of planning iterations required. More iterations allow for a more refined and polished game structure, enhancing the overall quality and playability. This pricing model ensures that users can tailor their project development to their specific needs and budgets.

## Installation

Ensure you have **Python** installed on your machine. Follow these steps to set up the project:

1. **Install Poetry:**

   Poetry is used for dependency management and packaging. To install Poetry, run:

   ```bash
   curl -sSL https://install.python-poetry.org | python3 -
   ```

   Alternatively, refer to the [Poetry installation guide](https://python-poetry.org/docs/#installation) for more options.

2. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/agent-game-maker.git
   cd agent-game-maker
   ```

3. **Install Dependencies:**

   ```bash
   poetry install
   ```

4. **Set Up Environment Variables:**

   Create a `.env` file in the root directory and add your Anthropic API key:

   ```env
   ANTHROPIC_API_KEY=your_api_key_here
   ```

## Usage

Run the `agent_game_maker.py` script to start creating your Pygame project:

```bash
poetry run python agent_game_maker.py
```

Follow the on-screen prompts to describe your game and specify the number of planning iterations. The tool will handle the rest, generating the project files and assisting with error resolution.

## Example Project

**Agent Game Maker** serves as an exemplary demonstration of how multi-agent systems can empower individuals to develop complex applications without extensive coding knowledge. By automating the planning and error-handling processes, it allows developers to focus on creative aspects, enhancing productivity and project quality.

## Development Journey

Creating **Agent Game Maker** was an insightful journey into building a multi-agent system using raw Python. The project was structured with all functionalities contained within a single file, `agent_game_maker.py`. This monolithic approach presented challenges, particularly with managing asynchronous operations (`async`/`await`) and ensuring smooth interactions between multiple AI agents.

One of the biggest hurdles was handling the asynchronous nature of the agents. Implementing `asyncio` required a solid understanding of concurrent programming in Python, which was a significant learning curve. Additionally, coordinating multiple agents to collaboratively plan, generate, and debug the Pygame project exposed limitations in scalability and maintainability. The system often fell into loops trying to resolve errors, highlighting the need for a more robust state management solution.

This journey not only demonstrated the potential of multi-agent systems in automating game development but also provided valuable lessons in managing complexity and ensuring system robustness.

## Learnings and Challenges

### Managing Asynchronous Operations

One of the initial challenges was mastering `asyncio` for handling concurrent tasks. Ensuring that multiple agents could operate simultaneously without causing race conditions or deadlocks required deep dives into asynchronous programming paradigms. This experience highlighted the importance of understanding the underlying mechanics of concurrency to build reliable systems.

### Scalability Concerns

While a single-file architecture was suitable for a small-scale project, scaling to accommodate dozens or hundreds of agents revealed significant drawbacks. The lack of modularity made it difficult to manage dependencies and maintain clean code. This realization emphasized the need for a more scalable architecture that could support dynamic context and extensive agent interactions.

### State Management

Effective state management was crucial for ensuring that agents could maintain context and collaborate efficiently. The monolithic structure made it challenging to track state changes and debug issues, the XML file leaves a lot to be desired compared to more dynamic systems. Learning about advanced state management techniques became a priority to enhance the system's integrity and performance.

### Error Handling and Resilience

Implementing robust error handling mechanisms was essential to prevent the system from falling into infinite loops when encountering unresolved errors. Developing strategies for graceful degradation and automated recovery improved the system's resilience and user experience.

### User Feedback Integration

Incorporating user feedback into the development loop proved to be a powerful tool for iterative improvement. Designing intuitive feedback interfaces and ensuring that agents could adapt based on user input enhanced the system's responsiveness and adaptability.

### Transition to Frameworks

The challenges encountered with raw Python paved the way for exploring more sophisticated frameworks. Recognizing the limitations of a single-file approach and the complexities of managing extensive agent interactions motivated the transition to frameworks that offer better scalability, modularity, and state management capabilities.
