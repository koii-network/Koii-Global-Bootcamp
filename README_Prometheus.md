# Prometheus: Add README for Koii-Global-Bootcamp

## Project Overview

The Koii Global Bootcamp is a comprehensive developer learning program designed to introduce developers to web3 technologies and distributed computing through a progressive, hands-on curriculum.

### Program Focus
This bootcamp provides a structured pathway for developers to learn and build distributed applications on the Koii network, with each lesson building upon the previous one to develop critical blockchain and distributed systems skills.

### Key Learning Objectives
- Master fundamental cryptographic principles essential for web3 development
- Learn to deploy distributed applications on a decentralized cloud infrastructure
- Understand mechanism design and tokenized payment systems
- Gain practical experience with blockchain technologies and distributed computing

### Curriculum Highlights
The bootcamp consists of four progressive lessons:
- **Cryptography 101**: Introduction to core cryptographic primitives and token deployment
- **Basic Distributed App Deployment**: Building a low-fidelity DOS game on Koii
- **Mechanism Design and Tokenized Payments**: Developing a distributed web crawler with tokenized incentives
- Advanced Distributed Systems Concepts

### Benefits
- Hands-on, project-based learning approach
- Step-by-step guidance for web3 development
- Practical skills in distributed computing
- Exposure to cutting-edge blockchain technologies

## Getting Started, Installation, and Setup

### Prerequisites

Before getting started, ensure you have the following installed:
- [Node.js](https://nodejs.org/en/download/) (v20.18.1 LTS recommended)
- [Git](https://git-scm.com/downloads)
- [Visual Studio Code](https://code.visualstudio.com/download) (optional, but recommended)
- [Yarn](https://classic.yarnpkg.com/lang/en/docs/install) (optional, but recommended)

### Quick Start

1. Clone the repository:
```bash
git clone https://github.com/koii-network/global.git
cd global
```

2. Install dependencies for a specific lesson:
```bash
cd Lesson_X_ProjectName  # Replace X with the lesson number
yarn install  # or npm install
```

### Running Projects

Each lesson has its own setup and running instructions. Generally, you can use these commands:

- To run in development mode:
```bash
yarn dev  # or npm run dev
```

- To build for production:
```bash
yarn build  # or npm run build
```

- To run tests:
```bash
yarn test  # or npm test
```

### Platform-Specific Notes

#### Windows
- Use Command Prompt or PowerShell as an administrator
- Ensure PowerShell script execution is enabled

#### macOS
- Install Git using Homebrew: `brew install git`
- Install Yarn using: `sudo npm install --global yarn`

#### Linux
- Use your distribution's package manager to install Node.js and Git
- Install Yarn using: `npm install --global yarn`

### Troubleshooting

If you encounter issues:
- Verify all prerequisites are correctly installed
- Check that you're using the recommended Node.js version (v20.18.1)
- Join the [Koii Discord channel](https://discord.gg/koii-network) for support

### Additional Resources

- [Koii Documentation Portal](https://www.koii.network/docs/develop/onboarding/welcome-to-koii)
- [Koii Desktop Node Download](https://www.koii.network/nodes)