# Prometheus: Add README for Koii-Global-Bootcamp

## Project Overview

The Koii Global Bootcamp is a comprehensive developer education program designed to onboard developers to web3 and distributed computing through a structured, hands-on learning experience. This curriculum focuses on teaching essential skills for building decentralized applications (dApps) on the Koii network's Cloud2 infrastructure.

### Program Structure
The bootcamp consists of four progressive lessons, each building upon the previous one to provide a comprehensive understanding of web3 development:

- **Lesson 1: Cryptography 101** - Introduces core cryptographic primitives fundamental to web3 technologies
- **Lesson 2: Basic Distributed App Deployment** - Guides developers in creating and deploying a simple distributed application
- **Lesson 3: Mechanism Design and Tokenized Payments** - Explores advanced concepts of distributed systems and token-based economic models
- **Lesson 4: Advanced Concepts** (Implied but not explicitly detailed)

### Key Benefits
- Hands-on learning approach with practical, incremental skill development
- Introduction to distributed computing and blockchain technologies
- Comprehensive coverage of web3 development fundamentals
- Preparation for building real-world decentralized applications

### Learning Outcomes
Developers completing this bootcamp will gain practical skills in:
- Cryptographic principles
- Distributed application architecture
- Token creation and economic mechanism design
- Deployment of decentralized systems

## Getting Started, Installation, and Setup

### Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js Version 20](https://nodejs.org/en/download/prebuilt-installer)
- [Yarn](https://classic.yarnpkg.com/lang/en/docs/install) (optional, but recommended)
- [Git](https://git-scm.com/downloads)
- [Koii Desktop Node](https://www.koii.network/nodes)

### Installation Steps

1. Clone the repository:
```sh
git clone https://github.com/koii-network/global.git
cd global
```

2. Choose the specific lesson directory you want to work on (e.g., `Lesson_1_Cryptography_101`):
```sh
cd Lesson_1_Cryptography_101
```

3. Install dependencies:
```sh
yarn
```

### Development Setup

#### Environment Configuration
- Copy `.env.local.example` to `.env` and update with your specific configuration
- For tasks requiring API keys, obtain them from the respective services:
  - Gemini AI: [Get API Key](https://aistudio.google.com/app/apikey)
  - BlueSky: [Create Account](https://bsky.app/)

### Running the Project

#### Development Mode
Most lessons can be run using Yarn scripts defined in the `package.json`:
```sh
# Example commands (vary by lesson)
yarn sign-and-verify     # Lesson 1: Cryptography
yarn prod-debug          # Lesson 2: DOS Games
yarn start               # General start command
```

#### Testing
Run tests using:
```sh
yarn test
```

### Deployment Considerations
- Each lesson has specific deployment instructions
- For Koii task deployment, refer to individual lesson documentation
- Some lessons require adding the Task ID to the Koii Desktop Node

### Troubleshooting
- Ensure all prerequisites are installed correctly
- Check the specific lesson's README for detailed troubleshooting
- Join the [Koii Discord](https://discord.gg/koii-network) for additional support