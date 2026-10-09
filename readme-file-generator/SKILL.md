---
name: readme-file-generator
description: Generates comprehensive, professional README.md files by analyzing the repository structure, source code, dependencies, and documentation. Optimized for learning projects, technical experiments, and software portfolios.
allowed-tools: ["Read", "Glob", "Grep", "Write"]
version: 1.1.0
author: BODYsuperman
license: Apache-2.0
keywords: [documentation, readme, markdown, learning, project, portfolio, technical]
---

# README Generator

Automatically generates high-quality README.md files by analyzing the project structure, source code, dependencies, configuration, experiments, and documentation.

This skill is designed for both **software projects** and **learning / experimentation repositories**.

For learning projects, the README should emphasize:

* What is being learned
* Learning goals
* Learning roadmap
* Concepts covered
* Hands-on implementations
* Experiments
* Key technical insights
* Project structure
* How to run the examples
* Learning progress
* References

The README should accurately reflect the actual repository and must not invent features, results, or capabilities.

---

## What This Skill Does

This skill helps create professional and informative README files by:

* Analyzing project structure and identifying key components
* Detecting programming languages and frameworks
* Finding configuration and dependency files
* Identifying source code, examples, experiments, tests, and scripts
* Understanding the purpose and type of the repository
* Detecting whether the repository is a product, library, application, learning project, or experimentation repository
* Identifying learning topics and technical concepts from the codebase
* Identifying datasets, models, APIs, and external services
* Finding documentation, notes, and learning materials
* Generating a README structure appropriate for the repository
* Following README and GitHub documentation best practices

---

# Instructions

When generating a README, follow these steps.

## 1. Project Discovery

First, analyze the repository structure.

Use `Glob` to identify:

* Main source directories
* Configuration files
* Dependency files
* Documentation files
* Notebook files
* Example directories
* Test directories
* Dataset directories
* Scripts
* Docker configuration
* CI/CD configuration
* Existing README files

Look for common files such as:

```text
package.json
pyproject.toml
requirements.txt
setup.py
Cargo.toml
go.mod
pom.xml
build.gradle
build.gradle.kts
composer.json
Gemfile
Dockerfile
docker-compose.yml
compose.yml
Makefile
LICENSE
CLAUDE.md
```

For machine learning and AI projects, also look for:

```text
.ipynb
*.py
*.pt
*.pth
*.ckpt
*.safetensors
datasets/
data/
models/
checkpoints/
experiments/
notebooks/
```

Use `Read` to examine important configuration and documentation files.

Use `Grep` to identify:

* Test files
* Entry points
* Training scripts
* Main classes
* Model definitions
* API endpoints
* Important configuration
* TODO/FIXME items
* CI/CD configuration
* Learning topics and technical concepts

---

# 2. Determine Repository Type

Before generating the README, determine what type of repository this is.

Possible categories include:

### Production Project

Examples:

* Web application
* Backend service
* CLI tool
* Library
* API
* SaaS application

### Learning Project

Examples:

* Programming learning repository
* Java / Python learning project
* Spring Boot learning project
* PyTorch learning repository
* Machine learning experiments
* LLM learning repository

### Technical Experiment

Examples:

* Model experiments
* Benchmarking
* Proof of concept
* Algorithm implementation
* Research reproduction

### Portfolio Project

A project primarily intended to demonstrate technical skills.

A repository may belong to multiple categories.

For example:

```text
Learning + Experimentation
Learning + Portfolio
Production + Portfolio
```

Choose the README structure based on the repository's actual purpose.

---

# 3. Content Analysis

Based on the repository analysis, determine:

* Project purpose
* Primary programming language(s)
* Frameworks and libraries
* Dependencies
* Build commands
* Run commands
* Test commands
* Configuration requirements
* Database requirements
* External services
* APIs
* Main modules
* Important source files
* Datasets
* Models
* Experiments
* Documentation
* License

For learning repositories, additionally determine:

* Learning objectives
* Topics covered
* Learning progression
* Implemented concepts
* Experiments performed
* Important technical observations
* Completed and unfinished topics
* Relationship between different examples

Do not infer technical capabilities that are not supported by the repository.

---

# 4. Learning Project Analysis

If the repository is primarily a learning project, do NOT present it as a production-ready application.

Instead, explain it as a hands-on technical learning repository.

The README should answer:

```text
Why was this repository created?

What technologies or concepts are being studied?

What has actually been implemented?

What experiments have been performed?

What did the experiments demonstrate?

What has been learned?

What is planned next?
```

Prefer sections such as:

```text
## 🎯 Learning Goals

## 📚 Learning Roadmap

## 🧪 Experiments

## 💡 Key Learnings

## 📂 Project Structure

## 🚀 Getting Started

## 📝 Notes

## 🗺️ Roadmap

## 📖 References
```

Do not force traditional product sections such as:

```text
Features
API Documentation
Production Deployment
Contributing
```

unless they are actually relevant.

---

# 5. README Generation

Generate the README based on the repository type.

## Standard Project README

For normal software projects, use an appropriate structure such as:

```text
# Project Name

## Overview

## Features

## Tech Stack

## Architecture

## Project Structure

## Prerequisites

## Installation

## Configuration

## Usage

## Testing

## Deployment

## API Documentation

## Roadmap

## Contributing

## License
```

Only include relevant sections.

---

# Learning Project README

For learning and experimentation repositories, prefer:

```text
# Project Name

> One-line description

## 🎯 Learning Goals

## 📚 Learning Roadmap

## 🧠 Topics Covered

## 🧪 Experiments

## 💡 Key Learnings

## 🛠️ Tech Stack

## 📂 Project Structure

## 🚀 Getting Started

### Requirements

### Installation

### Running Examples

## 📊 Results

## 📝 Notes

## 🗺️ Roadmap

## 📖 References

## 📄 License
```

Adapt the structure based on the actual repository.

---

# 6. Learning Roadmap

For learning repositories, create a roadmap based on the actual repository.

Example:

```markdown
## 📚 Learning Roadmap

### Fundamentals

- [x] Tensor operations
- [x] Automatic differentiation
- [x] Dataset and DataLoader

### Computer Vision

- [x] CNN
- [x] ResNet
- [ ] Vision Transformer

### Sequence Models

- [x] RNN
- [ ] LSTM
- [ ] GRU

### Transformers

- [x] Attention
- [x] Multi-Head Attention
- [ ] Transformer

### LLM

- [ ] Tokenization
- [ ] Embeddings
- [ ] Fine-tuning
- [ ] RAG
- [ ] AI Agents
```

Only mark an item as completed if the repository contains evidence that it has actually been implemented or studied.

Do not fabricate learning progress.

---

# 7. Experiments

For repositories containing experiments, identify and document them.

For each significant experiment, explain:

* What was tested
* Why it was tested
* Implementation
* Dataset or input
* Model or algorithm
* Important configuration
* Result, if available
* Key observation

Example:

```markdown
## 🧪 Experiments

### Character-Level RNN

Implemented a character-level RNN for Chinese poetry generation.

The experiment demonstrates:

- Sequence modeling
- Hidden state propagation
- Teacher-forcing style training
- Autoregressive text generation
```

Do not invent numerical results.

If actual results exist in the repository, report them accurately.

---

# 8. Key Learnings

For learning repositories, identify important concepts demonstrated by the code.

Examples:

```markdown
## 💡 Key Learnings

### Residual Connections

The project implements:

y = x + F(x)

The shortcut connection provides a direct path for gradients,
which helps optimize deeper networks.

### Sequence Modeling

The RNN maintains a hidden state that carries information
from previous time steps.
```

Keep explanations concise and technically accurate.

Do not turn the README into a textbook.

The README should provide enough context to understand the project while linking or referring to detailed notes when available.

---

# 9. Project Structure

Explain the actual repository structure.

Example:

```text
project/
├── data/
├── models/
├── experiments/
├── notebooks/
├── src/
├── tests/
├── README.md
└── requirements.txt
```

Add a short explanation for important directories.

Do not document directories that do not exist.

---

# 10. Writing Style

Use:

* Clear and concise language
* Active voice
* Professional but approachable tone
* Markdown headings
* Tables when useful
* Code blocks with proper syntax highlighting
* Short paragraphs
* Technical terminology accurately
* English by default for GitHub README files

Avoid:

* Excessive marketing language
* Unnecessary emojis
* Generic AI-generated descriptions
* Repeated explanations
* Claims that cannot be verified
* Overly long introductions

Use emojis sparingly and only when they improve readability.

---

# 11. Accuracy Rules

This is especially important.

Never invent:

* Features
* APIs
* Performance numbers
* Benchmarks
* Supported platforms
* Test results
* Architecture components
* Deployment capabilities
* Learning progress
* Completed roadmap items

If information cannot be determined from the repository, either:

1. Omit it, or
2. Clearly mark it as `TODO`

For example:

```markdown
> TODO: Add benchmark results.
```

Do not create fake benchmark numbers or technical claims.

---

# 12. Existing README

If `README.md` already exists:

1. Read the existing README.
2. Preserve valuable project-specific information.
3. Identify outdated or missing sections.
4. Improve rather than blindly overwrite.
5. Do not remove useful information without a reason.

If significant changes are required, summarize what will be changed before writing.

---

# 13. Output

Before writing `README.md`:

1. Analyze the repository.
2. Determine the repository type.
3. Identify the major topics and components.
4. Create an appropriate README structure.
5. Check for missing information.
6. Generate the README.

If the user explicitly asks to directly generate or update the README, write it to:

```text
README.md
```

Otherwise, present the proposed README and ask before overwriting an existing README.

---

# 14. Special Handling for AI / Machine Learning Projects

For AI, ML, Deep Learning, LLM, or AI Agent repositories, additionally inspect:

```text
models/
datasets/
data/
notebooks/
experiments/
training/
inference/
evaluation/
prompts/
agents/
rag/
embeddings/
```

Look for:

* Model architectures
* Training scripts
* Inference scripts
* Datasets
* Evaluation methods
* Prompt templates
* Embedding models
* Vector databases
* RAG pipelines
* Agent workflows
* LLM providers
* Model checkpoints

When appropriate, include:

```text
## 🧠 Concepts

## 🧪 Experiments

## 🤖 Models

## 📊 Results

## 🔄 Workflow

## 🏗️ Architecture
```

Only include sections supported by the actual repository.

---

# 15. Special Handling for Portfolio Projects

If the repository appears to be used as a technical portfolio project, emphasize:

* Engineering decisions
* Architecture
* Technical challenges
* Important implementation details
* Key technologies
* Lessons learned
* Demonstrable results

Do not exaggerate the project as production-ready unless the repository clearly supports that claim.

---

# Configuration

This skill adapts to project type.

| Project Type | Key Files                                        | Focus                                   |
| ------------ | ------------------------------------------------ | --------------------------------------- |
| Python       | `pyproject.toml`, `requirements.txt`, `setup.py` | Environment, dependencies, scripts      |
| Node.js      | `package.json`                                   | npm, scripts, framework                 |
| Java         | `pom.xml`, `build.gradle`                        | JDK, Spring, Maven/Gradle               |
| Rust         | `Cargo.toml`                                     | Cargo, modules, features                |
| Go           | `go.mod`                                         | Go modules, packages                    |
| AI / ML      | notebooks, models, datasets, scripts             | Models, experiments, training           |
| Learning     | source code, notes, examples                     | Learning roadmap, concepts, experiments |
| Generic      | Repository structure                             | Purpose, structure, usage               |

---

# Tool Requirements

* **Read**: Examine configuration, source code, documentation, and important implementation files
* **Glob**: Find relevant files and directories
* **Grep**: Search for patterns, tests, entry points, APIs, models, and technical concepts
* **Write**: Create or update `README.md`

---

# Limitations

* Cannot generate screenshots unless screenshot files already exist in the repository
* May miss custom build processes not represented in configuration files
* Cannot determine undocumented requirements with certainty
* Cannot infer results that are not recorded
* Cannot guarantee that generated commands work without executing them
* Generated README should be reviewed by the project owner

---

# Best Practices

When using this skill:

1. Run from the project root.
2. Analyze before writing.
3. Prefer actual repository evidence over assumptions.
4. Preserve useful existing documentation.
5. Do not fabricate features or results.
6. For learning projects, document learning progress rather than pretending the project is production software.
7. Keep the README focused on the repository.
8. Link to detailed documentation when the repository contains extensive notes.
9. Update the README when the project structure changes significantly.

---

# Error Handling

* **No project files found**: Ask the user to confirm the working directory.
* **Multiple languages detected**: Identify the primary language and document the others where relevant.
* **Existing README**: Read and improve it rather than blindly replacing it.
* **Missing key information**: Omit unsupported claims or use `TODO`.
* **Ambiguous project purpose**: Infer cautiously from repository structure and documentation; if still unclear, ask the user.
* **Incomplete project**: Clearly describe the current state instead of presenting it as complete.

---

# Related Skills

Related skills may include:

* `changelog-generator` — Create or update CHANGELOG.md
* `api-doc-generator` — Generate API documentation
* `license-picker` — Add or select a license

---

# Changelog

### Version 1.1.0

* Reworked for learning and experimentation repositories
* Added learning roadmap generation
* Added experiment analysis
* Added key learning extraction
* Added AI / ML project support
* Added portfolio project support
* Added stronger anti-hallucination rules
* Improved handling of existing README files
* Changed author from GLINCKER Team to BODYsuperman

### Version 1.0.0

* Initial version based on the original README Generator concept

---

# Author

**BODYsuperman**

GitHub: `BODYsuperman`
