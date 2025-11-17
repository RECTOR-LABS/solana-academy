# Starter Kits & Boilerplates

Quick-start templates to accelerate development.

---

## Recommended Starter Templates

### 1. Solana dApp Scaffold (Next.js)
**Repository:** https://github.com/solana-labs/dapp-scaffold
**Stack:** Next.js, TypeScript, Tailwind CSS, Wallet Adapter
**Use Case:** Best for general Solana dapps
**Setup:**
```bash
npx create-solana-dapp my-project
cd my-project
npm install
npm run dev
```

### 2. Anchor + Next.js Template
**Repository:** https://github.com/coral-xyz/anchor/tree/master/examples/tutorial
**Stack:** Anchor (Solana programs), Next.js frontend
**Use Case:** Projects requiring custom Solana programs
**Setup:**
```bash
anchor init my-project
cd my-project
anchor build
anchor test
```

### 3. Solana Game Starter (Phaser.js)
**Repository:** Research community examples on GitHub
**Stack:** Phaser.js + Solana Web3.js
**Use Case:** Browser-based 2D games
**Setup:**
```bash
# Generic Phaser template
npm create vite@latest my-game -- --template vanilla
cd my-game
npm install phaser @solana/web3.js @solana/wallet-adapter-react
```

### 4. Unity + Solana Template
**Repository:** https://github.com/magicblock-labs/Solana.Unity-SDK
**Stack:** Unity 3D + Solana Unity SDK
**Use Case:** 3D games or complex game mechanics
**Setup:**
- Clone repository
- Open in Unity
- Follow SDK integration guide

---

## Component Libraries

### Wallet Connection Components
```bash
npm install @solana/wallet-adapter-react \
            @solana/wallet-adapter-react-ui \
            @solana/wallet-adapter-wallets
```

### UI Component Libraries
```bash
# Tailwind CSS
npm install -D tailwindcss postcss autoprefixer

# Headless UI (for modals, dropdowns)
npm install @headlessui/react

# React Icons
npm install react-icons
```

---

## Boilerplate Features Checklist

Choose starter template that includes:
- [x] TypeScript configured
- [x] Solana Wallet Adapter integrated
- [x] Tailwind CSS setup
- [x] ESLint + Prettier
- [ ] Example transaction flow
- [ ] Devnet/Mainnet environment switching
- [ ] Responsive layout
- [ ] Dark mode (optional)

---

## Custom Setup (From Scratch)

If starting from zero, follow this order:

### Step 1: Initialize Next.js Project
```bash
npx create-next-app@latest my-solana-app --typescript --tailwind --app
cd my-solana-app
```

### Step 2: Install Solana Dependencies
```bash
npm install @solana/web3.js \
            @solana/wallet-adapter-react \
            @solana/wallet-adapter-react-ui \
            @solana/wallet-adapter-wallets \
            @solana/wallet-adapter-base
```

### Step 3: Install Additional Tools
```bash
npm install -D @types/node
npm install bs58  # For keypair encoding
```

### Step 4: Configure Wallet Adapter
Create `src/contexts/WalletContextProvider.tsx` (see examples in official docs)

### Step 5: Environment Variables
Create `.env.local`:
```
NEXT_PUBLIC_SOLANA_NETWORK=devnet
NEXT_PUBLIC_RPC_ENDPOINT=https://api.devnet.solana.com
```

---

## Testing Templates

### Jest Configuration
```bash
npm install -D jest @testing-library/react @testing-library/jest-dom
```

### Cypress E2E
```bash
npm install -D cypress
npx cypress open
```

---

## Deployment Templates

### Vercel Deployment
1. Push to GitHub
2. Import to Vercel
3. Configure environment variables
4. Deploy

### Netlify Deployment
```bash
npm run build
netlify deploy --prod
```

---

## Partner Integration Examples

### Moddio
- **Starter Project:** Check https://www.modd.io/ for official templates
- **Example Games:** Browse Moddio game gallery for inspiration

### Play Solana
- **Documentation:** TBD (research needed)
- **Examples:** Search GitHub for "Play Solana" examples

---

**Quick Start Recommendation:**

For fastest setup (Recommended for hackathon):
```bash
# Option 1: Solana dApp Scaffold
npx create-solana-dapp indiefun-project
cd indiefun-project
npm install
npm run dev
```

This gives you:
- ✅ Wallet adapter configured
- ✅ Tailwind CSS ready
- ✅ TypeScript enabled
- ✅ Example transaction flows
- ✅ Production build setup

**Time saved:** 4-6 hours of configuration

---

**Last Updated:** 2025-11-16

*Choose the template that best matches your project concept.*
