# Solana Trivia Duel - Complete Specification

**Project:** Solana Trivia Duel
**Type:** Gamified Dapp (Web-based multiplayer trivia game with crypto stakes)
**Blockchain:** Solana
**Timeline:** 26 days

---

## Concept Overview

**What is it?**
A competitive 1v1 trivia game where players stake SOL tokens to enter matches. Winner takes the pot. Think **Kahoot meets poker** - knowledge-based competition with real money stakes on blockchain.

**Core Value Proposition:**
- **For Players:** Fun way to earn SOL while testing knowledge
- **For Judges:** First Solana trivia dapp, showcases speed & low fees
- **For Ecosystem:** Onboards new users through familiar game mechanics

---

## Complete User Flow

### Flow 1: First-Time User (Onboarding)

**Step 1: Landing Page**
```
User visits: solana-trivia-duel.vercel.app

Sees:
- Hero section: "Challenge Your Friends. Win Solana."
- Live stats: "🔥 234 matches today | 💰 12.5 SOL won"
- How it works (3 steps)
- CTA: "Connect Wallet to Play"
```

**Step 2: Wallet Connection**
```
User clicks "Connect Wallet"
→ Modal appears with wallet options:
   - Phantom (recommended)
   - Solflare
   - Backpack

User selects Phantom
→ Phantom extension pops up
→ User approves connection
→ Wallet connected ✅

UI now shows:
- Wallet address (truncated): "5Kb8...9xYz"
- SOL balance: "2.45 SOL"
- "Play Now" button enabled
```

**Step 3: View Dashboard**
```
After connection, user sees Dashboard:

Left Panel:
- User stats (matches: 0, wins: 0, SOL earned: 0)
- Leaderboard (top 10 players)

Center Panel:
- "Quick Play" button (find random opponent)
- "Create Room" button (play with friend)
- Active matches count: "🎮 12 live matches"

Right Panel:
- Recent winners feed
- Tutorial video link
```

---

### Flow 2: Playing a Match (Quick Play)

**Step 1: Join Match Queue**
```
User clicks "Quick Play"
→ Stake selection modal appears:

"Choose Your Stake"
○ 0.1 SOL (Beginner)
○ 0.5 SOL (Intermediate) ← Default
○ 1.0 SOL (Expert)
○ Custom amount

[Confirm & Find Opponent]

User selects 0.5 SOL
→ Clicks confirm
→ Solana transaction prompt appears
```

**Step 2: Stake Transaction**
```
Phantom wallet pops up:

"Approve Transaction"
From: Your Wallet
To: Escrow Account (Program)
Amount: 0.5 SOL
Fee: 0.000005 SOL

[Approve] [Reject]

User clicks Approve
→ Transaction processing...
→ ✅ Staked! Finding opponent...
```

**Step 3: Matchmaking**
```
Loading screen appears:

"🔍 Finding worthy opponent..."
[Animated spinner]
"Players online: 47"

⏱️ Wait time: 5-30 seconds

Match found!
→ Opponent details appear:
   "vs. CryptoNinja420"
   "Win rate: 67% (20-10)"
   "Level: 12"

[Get Ready!] countdown: 3...2...1...
```

**Step 4: Game Begins**
```
Game screen layout:

┌─────────────────────────────────────────┐
│ Round 1/10          ⏱️ 15s             │
├─────────────────────────────────────────┤
│                                         │
│  Question:                              │
│  What year was Solana founded?          │
│                                         │
│  A) 2017                                │
│  B) 2018                                │
│  C) 2019                                │
│  D) 2020                                │
│                                         │
├─────────────────────────────────────────┤
│ YOU: 0 pts    |    OPPONENT: 0 pts     │
└─────────────────────────────────────────┘

User clicks answer (B) 2018
→ Button highlights
→ Timer keeps running for opponent
→ Both submitted

Round result appears:
✅ YOU: Correct! (+100 pts)
❌ OPPONENT: Wrong! (+0 pts)

[Next Round] auto-advances in 2s
```

**Step 5: Match Progression**
```
10 rounds total
Categories mix:
- Crypto/Blockchain (4 questions)
- General Knowledge (3 questions)
- Pop Culture (2 questions)
- Random (1 question)

Scoring:
- Correct answer: +100 pts
- Speed bonus: +0-50 pts (faster = more)
- Wrong answer: 0 pts

Real-time score updates after each round
Opponent's avatar shows their reaction (✅/❌)
```

**Step 6: Match End**
```
After Round 10:

🏆 VICTORY! 🏆

Final Score:
YOU: 850 pts
OPPONENT: 650 pts

Prize: 0.95 SOL
(0.5 your stake + 0.45 opponent stake)
Platform fee: 0.05 SOL (5%)

[Claim Winnings]

User clicks "Claim Winnings"
→ Solana transaction auto-executes
→ 0.95 SOL transferred to wallet
→ ✅ Claimed!

Post-match options:
[Play Again] [View Stats] [Share Win]
```

---

### Flow 3: Creating Private Room (Play with Friend)

**Step 1: Create Room**
```
User clicks "Create Room"
→ Room setup modal:

Room Settings:
- Stake amount: 0.5 SOL
- Number of questions: 10
- Time per question: 15s
- Categories: [Select categories]

[Create Room]

Room created!
Room Code: ZXCV-1234
Room Link: solana-trivia-duel.app/room/ZXCV-1234

[Copy Link] [Share on Twitter]
```

**Step 2: Wait for Opponent**
```
Waiting room screen:

"Waiting for opponent..."
Room Code: ZXCV-1234
Stake: 0.5 SOL

[Copy Invite Link]

Share this link with your friend!

⏱️ Room expires in: 9:45
```

**Step 3: Friend Joins**
```
Friend opens link
→ Sees room details:
   "CryptoKing invited you!"
   Stake: 0.5 SOL
   Questions: 10

   [Join Match] [Decline]

Friend clicks Join
→ Stakes 0.5 SOL
→ Both players ready
→ Match starts (same flow as Quick Play)
```

---

### Flow 4: Post-Match Experience

**Win Scenario:**
```
✅ Match won
→ SOL credited to wallet
→ Stats updated:
   - Wins: +1
   - Total earned: +0.45 SOL (profit)
   - Win streak: +1
→ Achievement unlocked? (e.g., "First Win!")
→ Leaderboard position updated
```

**Loss Scenario:**
```
❌ Match lost
→ Stake lost (held in opponent's winnings)
→ Stats updated:
   - Losses: +1
   - Win streak: Reset to 0
→ Encouragement message:
   "Better luck next time! 🎯"
   "Study up and try again!"
→ [Play Again] button
```

**Draw Scenario (Rare):**
```
🤝 DRAW!
Both players: 750 pts

Stakes returned:
YOU: 0.5 SOL (refund)
OPPONENT: 0.5 SOL (refund)

No platform fee on draws.

[Play Again]
```

---

## Technical Flow (Behind the Scenes)

### Architecture Overview

```
┌──────────────┐
│   Frontend   │  Next.js + React + Tailwind
│   (Browser)  │  Wallet Adapter
└──────┬───────┘
       │
       │ WebSocket (Socket.io)
       │ REST API
       │
┌──────▼───────┐
│   Backend    │  Node.js + Express
│   Server     │  Socket.io Server
└──────┬───────┘
       │
       ├─────────┐
       │         │
┌──────▼─────┐ ┌▼────────────┐
│ PostgreSQL │ │   Solana    │
│  Database  │ │ Blockchain  │
└────────────┘ └─────────────┘
```

---

### Technical Flow Step-by-Step

**1. User Connects Wallet**
```typescript
Frontend:
- User clicks "Connect Wallet"
- Wallet Adapter triggers Phantom
- User approves connection
- Frontend receives public key
- Store public key in React state
- Display wallet address in UI
```

**2. User Joins Match Queue**
```typescript
Frontend:
- User selects stake amount (0.5 SOL)
- Frontend calls Solana to create escrow transaction
- User approves transaction in Phantom
- Transaction confirmed on Solana blockchain
- Frontend emits WebSocket event: "join_queue"

Backend (WebSocket):
- Receives "join_queue" event
- Validates transaction on Solana
- Add user to matchmaking queue
- Match algorithm:
  - Find player with same stake amount
  - Similar skill level (optional)
  - FIFO if multiple matches
- When match found:
  - Create match instance
  - Emit "match_found" to both players
```

**3. Match Gameplay**
```typescript
Backend:
- Generate 10 random questions from database
- Send questions one-by-one (not all at once - prevent cheating)
- Track both players' answers in real-time
- Calculate scores:
  - Correct = 100 pts
  - Speed bonus = (15 - time_taken) * 3.33 pts
- After each round:
  - Broadcast results to both players
  - Update scores
- After 10 rounds:
  - Determine winner
  - Trigger payout

Solana Smart Contract (or Backend):
- Escrow holds both stakes (1.0 SOL total)
- Winner address authorized to claim
- Execute transfer:
  - Winner gets 0.95 SOL
  - Platform wallet gets 0.05 SOL (fee)
- Transaction confirmed
- Emit "payout_complete"

Frontend:
- Display winner animation
- Show final scores
- Update user stats
- Refresh wallet balance
```

**4. Leaderboard Update**
```typescript
Backend (PostgreSQL):
- After each match:
  UPDATE users
  SET wins = wins + 1,
      total_earned = total_earned + 0.45,
      win_streak = win_streak + 1
  WHERE public_key = 'winner_address';

- Recalculate leaderboard rankings
- Broadcast top 10 to all connected clients

Frontend:
- Receive leaderboard update via WebSocket
- Animate position changes
- Highlight user's position
```

---

## Key Features Breakdown

### MVP Features (Must-Have - Week 1-2)

**1. Wallet Integration**
- Connect/disconnect wallet
- Display wallet address
- Show SOL balance
- Support Phantom, Solflare, Backpack

**2. Matchmaking**
- Quick play (random opponent)
- Join queue system
- Stake selection (0.1, 0.5, 1.0 SOL)
- Match opponents by stake amount

**3. Game Mechanics**
- 10 multiple-choice questions per match
- 15-second timer per question
- Real-time answer submission
- Scoring: correct + speed bonus
- Winner determination

**4. Solana Transactions**
- Stake escrow (before match)
- Winner payout (after match)
- Transaction confirmations
- Error handling

**5. Basic UI**
- Landing page
- Dashboard
- Game screen
- Results screen
- Responsive design (mobile + desktop)

---

### Enhanced Features (Nice-to-Have - Week 3)

**6. Leaderboard**
- Top 10 players (by total earnings)
- User ranking display
- Win/loss records
- Win streaks

**7. Match History**
- Past matches list
- Opponent names
- Scores
- SOL won/lost
- Date/time

**8. User Profile**
- Avatar (Solana NFT or default)
- Username (linked to wallet)
- Total stats:
  - Matches played
  - Win rate
  - Total earned
  - Highest win streak
- Achievement badges

**9. Private Rooms**
- Create room with code
- Share invite link
- Custom stake amounts
- Friend vs friend matches

**10. Category Selection**
- Choose question categories:
  - Crypto/Blockchain
  - Solana Ecosystem
  - General Knowledge
  - Sports
  - Movies
  - Science
- Difficulty levels (Easy, Medium, Hard)

---

### Advanced Features (Optional - If Time Permits)

**11. Tournament Mode**
- Bracket-style tournaments
- 8-16 players
- Higher stakes
- Winner-takes-all pot
- Scheduled tournaments

**12. Practice Mode**
- Play solo (no stakes)
- Study questions
- Category practice
- No opponent needed

**13. Social Features**
- Share wins on Twitter
- Challenge specific users
- Friend system
- Chat during matches

**14. Power-ups (Gamification)**
- 50/50 (eliminate 2 wrong answers)
- Extra time (+5 seconds)
- Skip question
- Purchase with SOL or earn through wins

**15. NFT Integration**
- Mint winner NFTs for achievements
- Special avatars
- Trophy collection
- Rare question packs

---

## UI/UX Mockup Description

### Color Scheme (Solana Branding)
```
Primary: Purple (#9945FF - Solana brand)
Secondary: Cyan (#14F195 - Solana gradient)
Background: Dark (#0E0E10 - modern dark mode)
Text: White (#FFFFFF)
Accent: Gold (#FFD700 - for winners/prizes)
Error: Red (#FF4444)
Success: Green (#00FF00)
```

### Typography
```
Headings: Outfit (bold, modern)
Body: Inter (readable, clean)
Monospace: JetBrains Mono (for wallet addresses, code)
```

### Component Style
```
Cards: Dark with subtle purple glow
Buttons: Gradient (purple to cyan)
Inputs: Dark with white border
Modals: Glassmorphism effect
Animations: Smooth transitions (0.3s ease)
```

### Layout
```
Desktop:
┌─────────────────────────────────────┐
│  [Logo]        [Menu]     [Wallet]  │ ← Header
├─────────────────────────────────────┤
│ Sidebar │      Main Content         │
│  Stats  │                           │
│  Leader │                           │
│  board  │                           │
│         │                           │
└─────────────────────────────────────┘

Mobile:
┌─────────────┐
│   Header    │
├─────────────┤
│             │
│   Content   │
│             │
│             │
├─────────────┤
│ Bottom Nav  │
└─────────────┘
```

---

## Question Database Structure

### Sample Questions

**Category: Solana Blockchain**
```json
{
  "id": 1,
  "category": "solana",
  "difficulty": "easy",
  "question": "What year was Solana founded?",
  "answers": ["2017", "2018", "2019", "2020"],
  "correct": 0,
  "explanation": "Solana was founded in 2017 by Anatoly Yakovenko."
}
```

**Category: Crypto General**
```json
{
  "id": 2,
  "category": "crypto",
  "difficulty": "medium",
  "question": "What consensus mechanism does Solana use?",
  "answers": ["Proof of Work", "Proof of Stake", "Proof of History", "Proof of Authority"],
  "correct": 2,
  "explanation": "Solana uses Proof of History (PoH) combined with Proof of Stake."
}
```

**Category: Pop Culture**
```json
{
  "id": 3,
  "category": "pop_culture",
  "difficulty": "easy",
  "question": "Which movie won Best Picture at the 2024 Oscars?",
  "answers": ["Oppenheimer", "Barbie", "Poor Things", "The Holdovers"],
  "correct": 0,
  "explanation": "Oppenheimer won Best Picture at the 96th Academy Awards."
}
```

### Question Pool Size
- **MVP:** 200-500 questions (sufficient for initial launch)
- **Enhanced:** 1,000+ questions (reduce repetition)
- **Advanced:** 5,000+ questions with community submissions

### Question Sources
- Custom written (crypto/Solana specific)
- Open Trivia Database API (general knowledge)
- Community submissions (moderated)

---

## Monetization & Economics

### Revenue Model

**Platform Fee:**
- 5% of each match pot
- Example: 1.0 SOL pot → 0.05 SOL fee
- Distributed:
  - Winner: 0.95 SOL
  - Platform: 0.05 SOL

**Projected Revenue (Conservative):**
```
Assumptions:
- 100 matches/day
- Average stake: 0.5 SOL
- Platform fee: 5%

Daily revenue:
100 matches × 1.0 SOL pot × 5% = 5 SOL/day

Monthly revenue:
5 SOL/day × 30 days = 150 SOL/month

At $100/SOL = $15,000/month
At $200/SOL = $30,000/month
```

**Optional Revenue Streams:**
- Premium features (tournament entry)
- NFT sales (achievement badges)
- Sponsored questions (brand partnerships)
- Power-ups marketplace

---

## Success Metrics

### Hackathon Judging Criteria

**Product Quality (25%):**
- ✅ Zero critical bugs
- ✅ Smooth gameplay (no lag)
- ✅ Professional UI
- ✅ Mobile responsive

**Technical Implementation (20%):**
- ✅ Clean codebase
- ✅ Solana integration depth
- ✅ Real-time multiplayer working
- ✅ Secure escrow logic

**Originality (20%):**
- ✅ First Solana trivia game
- ✅ Unique crypto-trivia niche
- ✅ Fresh take on quiz games

**UX/Design (15%):**
- ✅ Intuitive navigation
- ✅ Beautiful UI (Solana branding)
- ✅ Smooth animations
- ✅ Clear feedback

**Vision (10%):**
- ✅ Roadmap for growth
- ✅ Community building potential
- ✅ Sustainable revenue model

**Social Proof (10%):**
- ✅ 50+ users before submission
- ✅ Twitter engagement
- ✅ Testimonials/feedback

---

## Development Phases

### Phase 1: Foundation (Days 1-7)
- Project setup (Next.js + TypeScript)
- Wallet integration
- Basic UI components
- WebSocket setup
- Quiz game logic (local testing)
- **Deliverable:** Alpha version (1v1 locally)

### Phase 2: Blockchain Integration (Days 8-14)
- Solana escrow transactions
- Winner payout logic
- Matchmaking backend
- Question database
- **Deliverable:** Beta version (full game loop on Devnet)

### Phase 3: Polish & Features (Days 15-21)
- Leaderboard
- Match history
- UI/UX refinement
- Edge case handling
- Performance optimization
- **Deliverable:** Production-ready

### Phase 4: Launch & Marketing (Days 22-26)
- Video trailer
- Indie.fun page
- Social media campaign
- User testing
- **Deliverable:** Submission ✅

---

## Risk Mitigation

**Technical Risks:**
- WebSocket scaling → Use Socket.io clustering
- Solana network congestion → Retry logic + user feedback
- Cheating (answer inspection) → Server-side validation, questions sent one-by-one

**Scope Risks:**
- Too many features → Focus on MVP first, add enhancements if ahead
- Polish takes longer → Allocate full Week 3 for refinement

**User Risks:**
- Low adoption → Seed with test users, friends, community
- Wallet friction → Clear onboarding tutorial

---

## Competitive Advantages

**vs. Traditional Trivia Apps:**
- ✅ Real money stakes (higher engagement)
- ✅ Instant payouts (Solana speed)
- ✅ Transparent/provably fair (blockchain)
- ✅ Low fees vs. centralized platforms

**vs. Other Crypto Games:**
- ✅ Skill-based (not pure gambling)
- ✅ Accessible (no complex DeFi knowledge)
- ✅ Social (play with friends)
- ✅ Quick matches (5-10 minutes)

**vs. Nothing (Market Gap):**
- ✅ First Solana trivia game
- ✅ Unique positioning in ecosystem

---

## Summary

**What we're building:**
A sleek, fast-paced 1v1 trivia game where players stake SOL, answer 10 questions, and winner takes the pot. Built on Solana for instant settlements and low fees.

**Why it wins:**
- First of its kind on Solana (huge differentiation)
- Familiar game mechanics (low barrier to entry)
- Showcases Solana's strengths (speed, fees)
- Feasible in 26 days (proven tech stack)
- Fun, engaging, shareable (viral potential)

**Tech stack:**
Next.js, TypeScript, Tailwind CSS, Socket.io, Solana Web3.js, PostgreSQL

**Timeline:**
15 days core development + 11 days polish/marketing

**Win probability:**
60%+ for top 3 ($2k-$5k prize)

---

**Next Step:** Review this spec, confirm it excites you, then we start building! 🚀

**Bismillah, let's make this happen!**

---

*Document created: 2025-11-16*
*Status: Ready for development*
