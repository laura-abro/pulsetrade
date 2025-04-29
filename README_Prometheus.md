# PulseTrade: AI-Powered Blockchain Trading Platform - Revolutionizing Financial Technology

## Project Overview

PulseTrade is an advanced AI-powered trading platform designed to revolutionize the financial trading experience. By leveraging cutting-edge artificial intelligence and blockchain technologies, the platform offers intelligent, secure, and user-friendly trading services.

### Key Objectives

- Provide an AI-driven trading solution that simplifies complex financial decision-making
- Offer advanced market analysis and predictive trading strategies
- Ensure enterprise-grade security and user data protection
- Create an accessible and intuitive trading experience for users of all skill levels

### Core Features

#### Intelligent Trading Capabilities
- Advanced AI algorithms for market trend analysis
- Real-time trading suggestions optimized for individual portfolios
- Machine learning-powered portfolio management and diversification strategies

#### Security and Trust
- Enterprise-grade security infrastructure
- Advanced AI monitoring for transaction protection
- Multi-chain support (Ethereum, Starknet)

#### User Experience
- Seamless account creation and onboarding
- Real-time transaction tracking and notifications
- 24/7 customer support
- Customizable trading strategies

### Technology Stack
- Next.js 14 frontend framework
- Blockchain integrations (Ethereum, Starknet)
- AI and machine learning technologies
- Web3 authentication
- Firebase for backend services
- Tailwind CSS for responsive design

PulseTrade bridges the gap between traditional trading platforms and modern AI-driven financial technologies, empowering users to make smarter, more informed trading decisions.

## Getting Started, Installation, and Setup

### Quick Start

PulseTrade is a Next.js-based AI-powered trading platform. Follow these steps to get started quickly:

#### Prerequisites

- Node.js (v14+)
- npm or yarn
- A modern web browser
- MetaMask or StarkNet Argent Wallet (for blockchain interactions)

#### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/patrickkish1/pulsetrade.git
   cd pulsetrade
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

#### Development Mode

Run the development server:
```bash
npm run dev
```
The application will be available at `http://localhost:3000`

#### Production Build

To create a production build:
```bash
npm run build
```

To start the production server:
```bash
npm start
```

#### Deployment

The project supports GitHub Pages deployment:
```bash
npm run predeploy  # Builds the application
npm run deploy     # Deploys to GitHub Pages
```

### Important Notes

- Ensure you have the latest version of your preferred blockchain wallet (MetaMask or Argent)
- Configure your `.env` file with necessary API keys and blockchain network settings
- The platform requires an active internet connection for real-time trading signals and blockchain interactions

### Recommended Environment

- **Operating System**: Linux, macOS, or Windows 10/11
- **Node.js**: Latest LTS version
- **Browser**: Latest versions of Chrome, Firefox, or Edge

## Deployment

### Deployment Options

#### Local Production Build
To create a production build of the application, use the following commands:

```bash
# Build the application
npm run build

# Start the production server
npm run start
```

#### GitHub Pages Deployment
The project includes a GitHub Pages deployment script:

```bash
# Predeploy (builds the application)
npm run predeploy

# Deploy to GitHub Pages
npm run deploy
```

#### Vercel Deployment
The application is configured for easy deployment on Vercel:

- The project uses Next.js static export (`output: 'export'`)
- GitHub repository is configured for `/pulsetrade` base path in production
- Recommended deployment method is through Vercel's GitHub integration

##### Deployment Considerations
- Ensure all environment variables are properly configured
- The application uses static export, which means server-side rendering is limited
- Image optimization is disabled (`unoptimized: true`)

#### Docker Deployment
While no explicit Docker configuration is present in the repository, the application can be containerized using a standard Next.js Dockerfile:

```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build
EXPOSE 3000
CMD ["npm", "start"]
```

### Supported Platforms
- Vercel (Recommended)
- GitHub Pages
- Self-hosted (Node.js)
- Docker (with custom Dockerfile)

## Feature Highlights

#### Trading Platform Features

##### Smart Trading Infrastructure
- **AI-Powered Market Analysis**: Advanced algorithms analyze real-time market trends and provide intelligent trading suggestions tailored to your investment profile
- **Comprehensive Portfolio Management**: Intelligent portfolio optimization using machine learning techniques to maximize returns and minimize risks

##### User Experience
- **Seamless Onboarding**: Quick account creation using email or social media credentials
- **Real-Time Transaction Tracking**: Instant updates and detailed notifications about your trading activities
- **Multi-Chain Support**: Trading capabilities across multiple blockchain networks including Ethereum and Starknet

##### Security and Support
- **Enterprise-Grade Security**: Advanced AI-monitored security protocols to protect your investments
- **24/7 Customer Support**: Round-the-clock assistance for all your trading needs

##### Dashboard Capabilities
- **Detailed Trading Dashboard**: Comprehensive overview of:
  * Total account balance
  * Open trading positions
  * Profit and loss statistics
  * Performance win rate
- **Trade History**: Detailed log of recent trades with profit/loss tracking

##### Advanced Trading Tools
- **Trade Execution Platform**: Streamlined interface for executing trades across different cryptocurrencies
- **AI Trading Strategies**: Customizable trading approaches powered by machine learning algorithms
- **Multi-Asset Trading**: Support for various cryptocurrency pairs and trading instruments

## Configuration

### Environment Configuration

The project uses environment variables for configuration, which can be set by creating a `.env` file based on the `.env.sample` template. Key configuration options include:

#### Particle Network
- `NEXT_PUBLIC_PROJECT_ID`: Particle Network project identifier
- `NEXT_PUBLIC_CLIENT_KEY`: Particle Network client key
- `NEXT_PUBLIC_APP_ID`: Particle Network application identifier

#### WalletConnect
- `NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID`: WalletConnect project identifier

#### Firebase Configuration
- `NEXT_PUBLIC_FIREBASE_API_KEY`: Firebase API key
- `NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN`: Firebase authentication domain
- `NEXT_PUBLIC_FIREBASE_PROJECT_ID`: Firebase project identifier
- `NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET`: Firebase storage bucket
- `NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID`: Firebase messaging sender ID
- `NEXT_PUBLIC_FIREBASE_APP_ID`: Firebase application identifier
- `NEXT_PUBLIC_FIREBASE_MEASUREMENT_ID`: Firebase measurement identifier

#### Contract Addresses
- `NEXT_PUBLIC_ETH_CONTRACT_ADDRESS`: Ethereum contract address (currently set to `0xe8da3071c06445ca26475f0fa1161ee5e8956929`)

### Build and Deployment Configuration

#### Next.js Configuration
- React Strict Mode is enabled
- Image optimization is disabled
- Production build includes a `/pulsetrade/` asset prefix and base path
- Configured for static export

### Styling Configuration

#### Tailwind CSS
- Dark mode support is enabled
- Custom theme extensions include:
  - Keyframe animations
  - Custom color palette
  - Gradient backgrounds
  - Custom border radius
  - Chart color definitions
- Uses `tailwindcss-animate` plugin for enhanced animations

### Plugin and Extension Details
- Tailwind CSS with custom configuration
- Animated UI components
- Responsive design with theme customization

## Project Structure

The project is organized into multiple key directories, each serving a specific purpose in the application architecture:

### Root Directory
- Configuration files for the project, including `package.json`, `next.config.mjs`, `tailwind.config.ts`, and various environment-specific files (`.env.sample`, `.gitignore`)

### `src` Directory
Primary source code for the application, structured into several subdirectories:

#### `src/app`
Contains Next.js page components and route definitions:
- Different pages for various features like admin, trading, AI chat, and prop firm
- `layout.tsx` and `page.tsx` for core application structure
- Routing-specific page components

#### `src/components`
Reusable React components organized into subdirectories:
- `ai-chat`: Components for AI chat functionality
- `chats`: Group chat and messaging components
- `trading`: Trading-related interface components
- `ui`: Reusable UI components like buttons, inputs, and dialogs

#### `src/lib`
Utility and service modules:
- `hooks`: Custom React hooks for various functionalities
- `services`: Service modules for different integrations (AI chat, trading)
- Utility functions and configuration files

### `contracts`
Contains smart contract files, specifically `PulseTrade.sol`

### `public`
Static assets like images and logos

### Specialized Subdirectories
- `koii/task-template`: Koii blockchain task-related files
- `particle-auth-aa`: Particle authentication and account abstraction components
- `starknetNethermind`: Starknet-specific smart contract project
- `tradeLLM`: Trade Language Model service with configuration and utility files

### Additional Project Configurations
- Multiple configuration files for tools like ESLint, Prettier, and build systems
- Environment-specific configuration files

## Technologies Used

#### Frontend Framework
- Next.js 14.2.4
- React 18
- TypeScript 5

#### Blockchain and Web3 Technologies
- Ethers.js
- Web3.js
- Viem
- Starknet
- Particle Network Authentication
- iExec DataProtector
- Web3Mail

#### UI and Styling
- Tailwind CSS
- Radix UI Components
- Shadcn/ui components
- Recharts (Data Visualization)
- Lucide React Icons

#### AI and Language Models
- Groq SDK
- LangChain
- LangGraph

#### Backend and API
- Express.js
- Node.js (>=18.0.0)

#### Data and Trading
- CCXT (Cryptocurrency Exchange Trading Library)
- Yahoo Finance API
- Polygon API

#### State Management and Utilities
- React Hooks
- Firebase
- Redis
- Node Cache

#### Development Tools
- ESLint
- PostCSS
- Nodemon
- gh-pages (Deployment)

#### Authentication and Security
- Particle Network AuthKit
- Firebase Authentication
- Express Rate Limiting

#### Monitoring and Logging
- Pino (Logging)

#### External Services
- Groq (AI Inference)
- Polygon (Market Data)

## Additional Notes

### Project Complexity and Integration

This platform represents a sophisticated, multi-technology ecosystem that integrates AI, blockchain, and web technologies. Users should be aware of the intricate interactions between various components and potential complexity in setup and configuration.

### Security Considerations

- The platform utilizes multiple blockchain networks and decentralized technologies, which require careful wallet management and security practices.
- Encrypted data protection is implemented through iExec's Data Protectors to ensure user data privacy.
- Multi-wallet support (MetaMask and Argent) provides flexibility in blockchain interactions.

### Performance Expectations

- AI-driven trade recommendations may vary based on market conditions and the current state of machine learning models.
- Real-time data processing relies on WebSocket connections and may experience slight latencies during high-traffic periods.

### Scalability Notes

- The architecture supports horizontal scaling through Kubernetes and cloud infrastructure (AWS/GCP).
- Blockchain interactions are optimized using Layer 2 solutions like StarkNet to minimize transaction costs and improve speed.

### Learning Resources

Users are encouraged to explore the platform's integrated learning modules, especially the Koii task-based tutorials that provide educational content and token rewards for skill development.

### Experimental Features

Some platform features, particularly those involving multi-LLM AI trade signal generation, are experimental and may undergo continuous refinement based on performance and user feedback.

## Contributing

We welcome contributions to PulseTrade! Whether you're fixing bugs, adding features, or improving documentation, your help is appreciated.

### Getting Started

1. **Fork the Repository**: Create a fork of the PulseTrade repository on GitHub.

2. **Clone Your Fork**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/pulsetrade.git
   cd pulsetrade
   ```

3. **Install Dependencies**:
   ```bash
   npm install
   ```

### Development Guidelines

#### Code Style
- Follow the existing code style and conventions.
- The project uses ESLint with Next.js core web vitals configuration.
- Run linting before submitting a pull request:
  ```bash
  npm run lint
  ```

#### Development Workflow
- Create a new branch for your contribution:
  ```bash
  git checkout -b feature/your-feature-name
  ```
- Make your changes and commit with clear, descriptive commit messages.

#### Running the Project
- Start the development server:
  ```bash
  npm run dev
  ```
- Build the project:
  ```bash
  npm run build
  ```

### Submitting Contributions

1. Push your changes to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```

2. Open a Pull Request (PR) against the main repository.

3. Ensure your PR description clearly explains:
   - The problem you're solving
   - Your proposed solution
   - Any relevant context or background information

### Code of Conduct
- Be respectful and considerate of others.
- Collaborate constructively.
- Help maintain a welcoming and inclusive community.

### Reporting Issues
- Use GitHub Issues to report bugs or suggest improvements.
- Provide detailed information:
  - Steps to reproduce
  - Expected behavior
  - Actual behavior
  - Environment details (OS, browser, etc.)

### Note
All contributions are subject to review. Maintainers may request changes or provide feedback to ensure code quality and alignment with the project's goals.

## License

This project is licensed under the MIT License. 

### License Details

The MIT License is a permissive open-source license that allows you to:
- Use the software commercially
- Modify the software
- Distribute the software
- Privately use the software

### Conditions

- Include the original copyright notice and license text in any substantial portion of the software
- The software is provided "as is" without warranty

For the full license text, please see the [LICENSE](LICENSE) file in the repository.

### Copyright

Copyright (c) 2024 Soos3D