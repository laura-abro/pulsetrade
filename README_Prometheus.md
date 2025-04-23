# Project Overview

## Purpose
PulseTrade is an advanced AI-powered trading platform designed to revolutionize the financial trading experience by combining cutting-edge artificial intelligence with blockchain technology. The platform provides users with intelligent, secure, and efficient trading services across multiple blockchain networks.

## Core Functionality
PulseTrade offers a comprehensive trading ecosystem that empowers users with:

- **AI-Driven Trading Strategies**: Leveraging machine learning algorithms to analyze market trends, predict potential opportunities, and execute trades with precision.
- **Multi-Chain Support**: Seamless trading capabilities across Ethereum and Starknet blockchains.
- **Sub-Account Management**: Flexible trading infrastructure allowing users to create and manage multiple trading sub-accounts with customizable profit-sharing models.
- **Advanced Security**: Enterprise-grade security protocols with AI-powered monitoring to protect user investments.

## Key Features
1. **Intelligent Portfolio Management**
   - Real-time market trend analysis
   - Algorithmic trading suggestions
   - Dynamic portfolio optimization
   - Risk assessment and mitigation strategies

2. **Blockchain Trading Infrastructure**
   - Trade execution across multiple blockchain networks
   - Secure smart contract-based trading mechanisms
   - Transparent transaction tracking
   - Instant trade settlement

3. **AI-Enhanced User Experience**
   - Personalized trading recommendations
   - Adaptive learning algorithms
   - Intuitive user interface
   - 24/7 AI-powered customer support

## Typical Use Cases
- Professional traders seeking advanced trading tools
- Investors looking for data-driven investment strategies
- Blockchain enthusiasts interested in multi-chain trading
- Financial institutions wanting AI-powered trading solutions

## Platform Highlights
- Supports multiple blockchain networks
- Advanced AI trading algorithms
- Secure and transparent trading infrastructure
- User-friendly interface
- Comprehensive trading analytics

## Getting Started

### Prerequisites
- Node.js (version 18 or later)
- npm (Node Package Manager)

### Installation Steps
1. Clone the repository
```bash
git clone https://github.com/your-username/pulsetrade.git
cd pulsetrade
```

2. Install dependencies
```bash
npm install
```

### Environment Configuration
1. Create a `.env.local` file in the project root
2. Copy the contents from `.env.sample` and fill in the required environment variables:
   - Particle Network credentials (Project ID, Client Key, App ID)
   - WalletConnect Project ID
   - Firebase configuration details
   - Ethereum contract address

Example `.env.local`:
```
NEXT_PUBLIC_PROJECT_ID=your_particle_project_id
NEXT_PUBLIC_CLIENT_KEY=your_particle_client_key
NEXT_PUBLIC_APP_ID=your_particle_app_id
NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID=your_walletconnect_project_id
# ... other Firebase and contract configurations
```

### Running the Development Server
To start the local development server:
```bash
npm run dev
```
The application will be available at `http://localhost:3000`

### Building for Production
To create a production build:
```bash
npm run build
```

### Additional Commands
- Lint the project: `npm run lint`
- Start production server: `npm start`
- Deploy to GitHub Pages: `npm run deploy`

### Troubleshooting
- Ensure all environment variables are correctly configured
- Check that you have the correct Node.js version installed
- If you encounter dependency issues, try clearing npm cache and reinstalling: 
  ```bash
  npm cache clean --force
  npm install
  ```

## Deployment

### Prerequisites
- Node.js (version 18 or later)
- npm (Node Package Manager)

### Local Deployment

1. **Development Server**
   ```bash
   # Install dependencies
   npm install

   # Run development server
   npm run dev
   ```
   The application will be available at `http://localhost:3000`

2. **Production Build**
   ```bash
   # Build the application
   npm run build

   # Start the production server
   npm run start
   ```

### Deployment Platforms

#### GitHub Pages
This project supports deployment to GitHub Pages:
```bash
# Predeploy (builds the application)
npm run predeploy

# Deploy to GitHub Pages
npm run deploy
```

#### Vercel (Recommended)
The project is Next.js based and optimized for Vercel deployment:
1. Connect your GitHub repository to Vercel
2. Vercel will automatically detect the Next.js configuration
3. Deploy with zero configuration

#### Docker
While no explicit Dockerfile is present, you can create a standard Next.js Dockerfile:
```dockerfile
FROM node:18-alpine
WORKDIR /app

# Copy package files
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy project files
COPY . .

# Build the application
RUN npm run build

# Expose port and start production server
EXPOSE 3000
CMD ["npm", "start"]
```

### Environment Configuration
1. Copy `.env.sample` to `.env.local`
2. Fill in the required environment variables
3. Ensure sensitive information is not committed to version control

### Hosting Recommendations
- **Vercel**: Recommended for Next.js applications
- **Netlify**: Good alternative with easy GitHub integration
- **GitHub Pages**: Suitable for static exports
- **Self-hosted Docker**: For custom infrastructure needs

### Notes
- Ensure all environment variables are properly configured
- Check network connectivity and API endpoint configurations
- Verify blockchain wallet and authentication providers are correctly set up

## Project Structure

The project follows a modern Next.js and TypeScript application structure:

```
├── public/                   # Static assets and images
│   ├── logo.png
│   ├── dashboard1.png
│   └── ...

├── src/
│   ├── app/                  # Next.js app router pages and layouts
│   │   ├── admin/            # Admin-related pages
│   │   ├── ai-chat/          # AI chat functionality pages
│   │   ├── trading/          # Trading-related pages
│   │   ├── layout.tsx        # Main application layout
│   │   └── page.tsx          # Home/landing page

│   ├── components/           # Reusable React components
│   │   ├── ai-chat/          # Components specific to AI chat
│   │   ├── chats/            # Chat-related components
│   │   ├── trading/          # Trading interface components
│   │   ├── ui/               # Shared UI components (buttons, inputs, etc.)
│   │   ├── Footer.tsx
│   │   ├── Header.tsx
│   │   └── ...

│   ├── lib/                  # Utility functions and services
│   │   ├── hooks/            # Custom React hooks
│   │   ├── services/         # API and data service integrations
│   │   │   ├── ai-chat.ts
│   │   │   ├── ethereum-trading.ts
│   │   │   └── starknet-trading.ts
│   │   ├── firebase.ts       # Firebase configuration
│   │   └── utils.ts          # Utility functions

├── contracts/                # Smart contract definitions
│   └── PulseTrade.sol        # Main smart contract

├── config files              # Configuration for various tools
│   ├── next.config.mjs
│   ├── tailwind.config.ts
│   ├── tsconfig.json
│   └── postcss.config.mjs
```

### Key Directories
- `public/`: Contains static assets like images and SVGs
- `src/app/`: Next.js application routes and page components
- `src/components/`: Reusable React components organized by feature
- `src/lib/`: Utility functions, hooks, and service integrations
- `contracts/`: Blockchain smart contract definitions

### Key Configuration Files
- `next.config.mjs`: Next.js configuration
- `tailwind.config.ts`: Tailwind CSS configuration
- `tsconfig.json`: TypeScript configuration
- `package.json`: Project dependencies and scripts

## Technologies Used

### Frontend
- **Framework**: Next.js 14
- **Language**: TypeScript
- **UI Libraries**: 
  - Radix UI (for accessible UI components)
  - Lucide React (icons)
  - Recharts (data visualization)

### Styling
- Tailwind CSS
- Class Variance Authority
- Tailwind Merge

### Web3 & Blockchain
- Ethers.js
- Viem
- Web3.js
- Starknet.js
- Particle Network (Authentication)

### Authentication & Identity
- Particle Network Auth Core
- iExec Data Protector
- Firebase Authentication

### State Management & Utilities
- React
- React DOM
- Clsx (utility for conditional class names)

### Deployment & Development
- ESLint
- PostCSS
- GitHub Pages (deployment)

### Additional Tools
- React Hot Toast (notifications)
- Cross-env (environment management)

## Feature Highlights

### 🔐 Smart Authentication
- Seamless wallet connection using Particle Network's ConnectKit
- Support for multiple authentication methods (email, social media)
- Enterprise-grade security with advanced AI monitoring

### 📊 AI-Powered Trading Intelligence
- Advanced machine learning algorithms for market trend analysis
- Real-time trading suggestions optimized for your portfolio
- Intelligent portfolio management and diversification strategies

### 🤖 AI Trading Capabilities
- Automated trade execution based on market patterns
- Adaptive strategies that align with your risk preferences
- Predictive trend analysis to inform investment decisions

### 💹 Trading Features
- Execute trades across multiple blockchain networks
- Real-time transaction tracking and notifications
- Comprehensive trading history and performance dashboards

### 🌐 Multi-Platform Support
- Web application with responsive design
- Compatible with different blockchain ecosystems
- Supports both desktop and mobile interfaces

### 🛡️ Enhanced User Experience
- Effortless account creation
- Intuitive user interface
- 24/7 customer support
- Personalized trading insights and recommendations

## Configuration

### Environment Variables
The project uses environment variables for configuration. Copy the `.env.sample` file to `.env` and fill in the following variables:

#### Particle Network Configuration
- `NEXT_PUBLIC_PROJECT_ID`: Your Particle Network project ID
- `NEXT_PUBLIC_CLIENT_KEY`: Particle Network client key
- `NEXT_PUBLIC_APP_ID`: Particle Network application ID

#### WalletConnect Configuration
- `NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID`: WalletConnect project ID from cloud.walletconnect.com

#### Firebase Configuration
- `NEXT_PUBLIC_FIREBASE_API_KEY`: Firebase API key
- `NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN`: Firebase authentication domain
- `NEXT_PUBLIC_FIREBASE_PROJECT_ID`: Firebase project ID
- `NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET`: Firebase storage bucket
- `NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID`: Firebase messaging sender ID
- `NEXT_PUBLIC_FIREBASE_APP_ID`: Firebase app ID
- `NEXT_PUBLIC_FIREBASE_MEASUREMENT_ID`: Firebase measurement ID

#### Contract Addresses
- `NEXT_PUBLIC_ETH_CONTRACT_ADDRESS`: Ethereum contract address

### Next.js Configuration
The project uses the following Next.js configuration options:
- `reactStrictMode`: Enabled for better React development experience
- `images.unoptimized`: Image optimization is disabled
- `output`: Set to 'export' for static site generation
- Production builds use a custom asset prefix and base path `/pulsetrade/`

### Tailwind CSS Configuration
- Dark mode is supported using the `class` strategy
- Custom theme extensions include:
  - Keyframe animations
  - Gradient backgrounds
  - Custom color palette
  - Responsive border radii
- Uses `tailwindcss-animate` plugin for enhanced animations

### Build and Runtime Configuration
- Supports both development and production environments
- Production builds have specific path and asset handling
- Static site export is configured

### Recommended Tools
- Node.js
- npm or yarn
- Next.js
- Tailwind CSS
- WalletConnect
- Particle Network SDK

### Notes
- Always keep environment variables secure and do not commit sensitive information
- Verify all configuration values before deployment
- Some configuration may require additional setup in respective service dashboards

## License

This project is licensed under the MIT License. 

For the full license text, please see the [LICENSE](LICENSE) file in the repository.

### MIT License Summary
- You are free to use, modify, and distribute this software
- Commercial use is permitted
- Modification and distribution are allowed
- Private and commercial use is allowed
- The only requirement is to include the original license and copyright notice in any substantial portion of the software

Copyright (c) 2024 Soos3D

For complete details and restrictions, please review the full license text.