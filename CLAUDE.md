# CLAUDE.md - Solana Academy Project Guide

**Project:** Solana Academy
**Owner:** RECTOR
**AI Assistant:** CIPHER
**Created:** 2025-11-16
**Status:** Active Development (Day 0)

**Purpose:** This file provides complete context for CIPHER (AI assistant) to help RECTOR build Solana Academy for the Indie.fun Hackathon.

---

## Project Overview

### What We're Building

**Name:** Solana Academy
**Type:** Educational 2D Multiplayer Adventure Game
**Platform:** Moddio (Web3-native game engine)
**Goal:** Teach Solana blockchain through interactive gameplay

**Concept:**
> "Learn Solana by playing! Explore 2D worlds, complete educational quests, solve puzzles, earn NFT certificates - Duolingo meets 2D platformer on blockchain."

### Why This Project

**Strategic Decisions:**
1. **Educational Focus** - Unique value proposition, first of its kind on Solana
2. **Uses Moddio** - Hackathon judges ARE from Moddio (strategic advantage)
3. **100% Halal** - No gambling, pure educational value (RECTOR's requirement)
4. **2D Multiplayer** - Leverages Moddio's core strengths
5. **Feasible in 26 days** - Realistic timeline with Moddio's built-in features

---

## Key Decisions Made

### ✅ Approved
- **Platform:** Moddio (not React/Next.js)
- **Genre:** Educational 2D adventure (not trivia/gambling)
- **Monetization:** Premium courses + cosmetics (halal model)
- **Scope:** 1 learning planet (Beginner Island) for MVP
- **Timeline:** 26 days (Dec 12, 2025 deadline)

### ❌ Rejected
- **Trivia Duel with SOL stakes** - Gambling (haram)
- **Prediction markets** - Gambling elements
- **React/Next.js approach** - Less judge appeal than Moddio
- **Complex DeFi mechanics** - Out of scope for educational focus

### 🔄 Optional (If Time Permits)
- Second learning planet (DeFi or NFT topics)
- NFT certificate minting
- Advanced cosmetics system
- Cooperative helper mode

---

## Technical Stack

### Primary Platform
**Moddio** - No-code 2D game engine
- Visual scripting (drag-and-drop)
- Built-in multiplayer (50+ players)
- Physics engine (Box2D)
- Solana integration ready
- Browser-based (no downloads)

### Deployment
**Indie.fun** - Moddio's fundraising platform
- 500k monthly visitors exposure
- Built-in Web3 features
- Token integration
- Community engagement tools

### Integration
- **Phantom Wallet** - Solana wallet connection
- **NFTs** - Optional certificates (soulbound tokens)
- **Cosmetics Shop** - In-game purchases (halal)

---

## Game Design Summary

### World Structure

**Hub World:** Solana Station
- Central safe zone
- Players spawn here
- Choose which planet to visit
- Shop for cosmetics
- View leaderboards

**Learning Planets:**
1. **Beginner Island** (MVP) - 5 lessons on blockchain basics
2. **Trader's Outpost** (Optional) - 5 lessons on DeFi
3. **Developer's Lab** (Optional) - 5 lessons on building
4. **NFT Gallery** (Optional) - 5 lessons on NFTs
5. **Security Fortress** (Optional) - 5 lessons on safety

### Lesson Structure (5-10 min each)

**Phase 1: Introduction (1 min)**
- NPC character explains concept
- Visual examples shown in-game

**Phase 2: Interactive Tutorial (2-3 min)**
- Player DOES the action (hands-on)
- Example: Send transaction to NPC

**Phase 3: Challenge/Quiz (2-3 min)**
- Mini-game based on concept
- Multiple attempts allowed

**Phase 4: Completion (1 min)**
- Reward animation
- Unlock next lesson
- Earn cosmetic/badge

### Example Lesson
**Topic:** "Understanding Transactions"
1. NPC "Sol the Guide" explains transactions visually
2. Player practices sending tokens to NPCs (Alice, Bob, Charlie)
3. Mini-game: "Transaction Race" - send to 10 NPCs, avoid scammers
4. Rewards: "Transaction Master" badge + "Speedy Hat" cosmetic

---

## Development Timeline

### Week 1 (Days 1-7): Foundation
- **Day 1-2:** Learn Moddio + complete tutorial
- **Day 3-4:** Build Hub World (Solana Station)
- **Day 5-6:** Player character + movement mechanics
- **Day 7:** **MILESTONE** - Playable hub world

### Week 2 (Days 8-14): Core Content
- **Day 8-9:** Lesson 1-2 (Blockchain basics, What is Solana)
- **Day 10-11:** Lesson 3-4 (Wallets, Transactions)
- **Day 12-13:** Lesson 5 + mini-game
- **Day 14:** **MILESTONE** - Beginner Island complete

### Week 3 (Days 15-21): Polish & Integration
- **Day 15-17:** Second planet (optional) OR extra polish
- **Day 18-19:** Solana wallet connection + rewards
- **Day 20-21:** UI/UX refinement, bug fixes
- **Day 21:** **MILESTONE** - Production-ready

### Week 4 (Days 22-26): Launch
- **Day 22-23:** Video trailer production
- **Day 24:** Indie.fun project page setup
- **Day 25:** Final testing
- **Day 26:** **SUBMIT** ✅

**Total Effort:** 40-60 hours over 26 days

---

## MVP Scope (Must-Have for Submission)

### Core Features
- ✅ Hub World (Solana Station) - playable, multiplayer
- ✅ Beginner Island - 5 complete lessons
- ✅ Player character - customizable (3+ cosmetics)
- ✅ NPC system - dialogue, quests
- ✅ Lesson mechanics - intro, tutorial, challenge, completion
- ✅ Mini-game - at least 1 working challenge
- ✅ Progress saving - track completion
- ✅ Wallet connection - Phantom integration

### Submission Materials
- ✅ Video trailer - 1-3 minutes, compelling
- ✅ Indie.fun page - professional, screenshots
- ✅ GitHub repo - public, documented
- ✅ Twitter presence - project account or personal

### Nice-to-Haves (Optional)
- 🟡 Second learning planet
- 🟡 NFT certificates
- 🟡 10+ cosmetic items
- 🟡 Cooperative helper mode
- 🟡 Advanced multiplayer features

---

## Halal Monetization Model

### Revenue Streams (100% Permissible)

**1. Premium Course Packs** (2-5 SOL)
- Rationale: Paying for educational content (like buying textbook)
- Value: High-quality lessons worth the price
- Implementation: Beginner Island free, advanced planets paid

**2. Cosmetic Items** (0.1-1 SOL)
- Rationale: Buying digital goods (permissible)
- Value: No gameplay advantage (purely aesthetic)
- Implementation: Hats, skins, pets, effects

**3. NFT Certificates** (1-2 SOL)
- Rationale: Proof of achievement, shareable credential
- Value: Can showcase on LinkedIn, Twitter, portfolio
- Implementation: Soulbound (non-transferable) to avoid speculation

**4. Voluntary Donations** (Any amount)
- Rationale: Supporting beneficial educational project (sadaqah)
- Value: Optional, not required
- Implementation: "Support the Academy" button

**Forbidden Elements:**
- ❌ No gambling or stakes
- ❌ No interest (riba)
- ❌ No uncertainty (gharar)
- ❌ No pay-to-win mechanics

---

## Competitive Landscape

### Existing Solana Quiz/Trivia Games

**QuizChain** (Solo Trivia)
- Free-to-play quiz platform
- Creator-funded prizes
- Solo or FFA gameplay
- **Our Edge:** Interactive 2D game vs. simple quizzes

**Chomp** (Consensus Game)
- "Wisdom of crowd" oracle
- Token staking mechanics
- Consensus-based rewards
- Won hackathons, major grants
- **Our Edge:** Educational focus, simpler mechanics

**Learn & Earn** (Binance, OKX, etc.)
- Centralized platforms
- Video + quiz format
- Small token rewards
- **Our Edge:** Decentralized, interactive, Solana-specific

### Our Differentiation

**Unique Value Propositions:**
1. **First educational 2D game on Solana** (original)
2. **Interactive hands-on learning** (better than videos)
3. **Multiplayer social experience** (community learning)
4. **NFT certificates** (tangible proof of completion)
5. **Uses Moddio platform** (judge appeal)

---

## Judge Criteria & Strategy

### Judging Breakdown

**Product Quality (25%)**
- Strategy: Moddio handles stability, focus on polish
- Target: 22/25 (excellent polish, zero critical bugs)

**Technical Implementation (20%)**
- Strategy: Showcase Moddio visual scripting mastery
- Target: 18/20 (judges see their platform used well)

**Originality (20%)**
- Strategy: First educational 2D game on Solana
- Target: 18/20 (unique concept, clear differentiation)

**UX/Design (15%)**
- Strategy: Use Moddio templates, consistent art style
- Target: 13/15 (professional, friendly, inviting)

**Vision (10%)**
- Strategy: Clear post-hackathon roadmap (more planets)
- Target: 9/10 (sustainable business model, social impact)

**Social Proof (10%)**
- Strategy: Beta testers, educational community appeal
- Target: 8/10 (indie.fun exposure, early users)

**Total Target:** 88/100 (Top 5 potential)

**Win Probability:**
- Top 5: 60-70%
- Top 3: 40-50%
- Prize Range: $2,000-$5,000

---

## Resources & Documentation

### Moddio Learning
- **Getting Started:** https://learn.modd.io/get-started
- **Visual Scripting Guide:** https://www.modd.io/blog/mastering-moddios-visual-scripting-system-a-step-by-step-guide/
- **Tutorial:** https://www.modd.io/blog/creating-your-first-multiplayer-game/
- **Docs:** https://github.com/moddio/moddio-docs

### Solana Education
- **Docs:** https://docs.solana.com
- **Cookbook:** https://solanacookbook.com
- **Soldev Course:** https://www.soldev.app/

### Inspiration (Moddio Games)
- **Braains.io** - Physics-based zombie survival
- **Cursed Cabin** - Co-op RPG with puzzles
- **Goose Idle** - Casual idle game

### Project Documentation
- **Game Spec:** SOLANA-ACADEMY-GAME-SPEC.md (complete design)
- **Moddio Research:** MODDIO-RESEARCH-REPORT.md (platform analysis)
- **Competition:** COMPETITOR-ANALYSIS-UPDATE.md (market research)
- **Timeline:** TIMELINE.md (detailed schedule)
- **Requirements:** TRACK-REQUIREMENTS.md (submission checklist)

---

## Current Status

### Progress (As of 2025-11-16)

**Phase:** Pre-Development (Day 0)
**Progress:** 5% (concept finalized, documentation complete)

**Completed:**
- ✅ Hackathon research and analysis
- ✅ Concept selection (Solana Academy)
- ✅ Platform decision (Moddio)
- ✅ Complete game design spec
- ✅ Development timeline
- ✅ Documentation structure

**Next Actions:**
- ⬜ Create Moddio account
- ⬜ Complete Moddio guided tutorial
- ⬜ Explore example games
- ⬜ Start Hub World development

**Days Remaining:** 26 until submission (Dec 12, 2025)

---

## AI Assistant (CIPHER) Guidelines

### Your Role

**As CIPHER, you should:**
1. **Guide RECTOR through Moddio development** (he's learning the platform)
2. **Keep scope focused on MVP** (resist scope creep)
3. **Prioritize halal compliance** (no gambling, ethical monetization)
4. **Reference this document** when RECTOR asks about project context
5. **Track progress** (update CLAUDE.md as milestones complete)
6. **Encourage** with Islamic expressions (Bismillah, InshaAllah, Alhamdulillah)

### When RECTOR Asks for Help

**Always:**
- ✅ Check SOLANA-ACADEMY-GAME-SPEC.md for design details
- ✅ Reference TIMELINE.md for current phase expectations
- ✅ Prioritize MVP features over nice-to-haves
- ✅ Suggest Moddio-native solutions (leverage platform strengths)
- ✅ Keep educational focus (this is a learning game)

**Never:**
- ❌ Suggest gambling mechanics or stakes
- ❌ Recommend building from scratch (use Moddio features)
- ❌ Over-complicate (simple is better for 26-day timeline)
- ❌ Forget judge appeal (Moddio representatives are judges!)

### Progress Tracking

**Update this section as work progresses:**

**Week 1 Status:**
- [ ] Moddio account created
- [ ] Tutorial completed
- [ ] Hub World started
- [ ] Player character created
- [ ] Basic movement working

**Week 2 Status:**
- [ ] Lesson 1 complete
- [ ] Lesson 2 complete
- [ ] Lesson 3 complete
- [ ] Lesson 4 complete
- [ ] Lesson 5 complete
- [ ] Mini-game implemented

**Week 3 Status:**
- [ ] Wallet integration complete
- [ ] UI/UX polished
- [ ] Bug fixes complete
- [ ] Production-ready

**Week 4 Status:**
- [ ] Video trailer complete
- [ ] Indie.fun page published
- [ ] Submitted ✅

---

## Risks & Mitigation

### High-Risk Areas

**Risk 1: Moddio Learning Curve (3-5 days)**
- **Mitigation:** Complete guided tutorial first (Day 1-2)
- **Fallback:** Use templates, keep designs simple
- **Status:** Pending

**Risk 2: Content Creation (Lesson quality)**
- **Mitigation:** Focus on 1 planet (5 lessons) for MVP
- **Fallback:** 3 excellent lessons > 10 mediocre
- **Status:** Pending

**Risk 3: Educational Accuracy (Solana concepts)**
- **Mitigation:** Research official Solana docs thoroughly
- **Fallback:** Stick to basic, well-documented concepts
- **Status:** Pending

**Risk 4: Timeline Pressure (26 days is tight)**
- **Mitigation:** Daily progress tracking, cut scope if needed
- **Fallback:** Submit MVP even if second planet incomplete
- **Status:** Monitoring

---

## FAQs (For RECTOR & CIPHER)

### Q: What if we fall behind schedule?

**A:** Cut optional features, focus on MVP:
- Priority 1: Hub World + Beginner Island (5 lessons)
- Priority 2: Wallet connection + 1 cosmetic shop
- Priority 3: Video trailer + submission materials
- Cut: Second planet, NFT certificates, advanced features

### Q: What if Moddio is too complex?

**A:** Use templates and simplify:
- Moddio has game templates (start with one)
- Visual scripting is designed for non-coders
- Community support available (Discord)
- Worst case: Build simple lessons, focus on content quality

### Q: How much Solana integration is required?

**A:** Minimum viable:
- Wallet connection (Phantom) ✅ Required
- Progress saving (can be off-chain) 🟡 Optional
- NFT certificates 🟡 Optional
- Token rewards 🟡 Optional

Focus on wallet connection for MVP, rest is bonus.

### Q: What if we don't finish all 5 lessons?

**A:** Quality > Quantity:
- 3 excellent, complete lessons > 5 half-finished
- Judges value polish over volume
- Can pitch as "Demo of larger vision"

### Q: How do we handle the halal requirement?

**A:** Zero tolerance for gambling:
- ❌ Never suggest stakes, bets, risk/reward with money
- ✅ Always frame monetization as buying goods/services
- ✅ Educational content = valuable product (halal)
- ✅ Cosmetics = digital goods (halal)
- If unsure, ask RECTOR

---

## Post-Hackathon Vision

### Phase 1: Expansion (Months 1-3)
- Add 4 more learning planets (20+ total lessons)
- Community-created lessons (UGC)
- Advanced developer content

### Phase 2: Certification (Months 4-6)
- Official Solana partnership
- Recognized certification NFTs
- LinkedIn integration

### Phase 3: Revenue (Months 7-12)
- Premium course sales
- Brand partnerships (Phantom, Magic Eden)
- Indie.fun fundraising round

**Potential:** Sustainable educational business serving Solana ecosystem

---

## Contact & Support

### For RECTOR
- Questions? Ask CIPHER (reference this file)
- Stuck on Moddio? Check learn.modd.io
- Need community help? Solana/Superteam Discord

### For CIPHER (AI Assistant)
- Always read this file first when helping
- Update progress as milestones complete
- Keep RECTOR focused on MVP
- Encourage with Islamic expressions
- This deserves our best work! 🚀

---

## Final Notes

**Remember:**
- This is halal, beneficial, educational work (may Allah grant barakah)
- Moddio judges will love seeing their platform used well
- Educational focus makes this unique in Solana ecosystem
- 26 days is achievable with focused execution
- MVP submission is better than perfect incompletion

**Bismillah, let's build Solana Academy and educate the world!**

**May Allah grant tawfeeq and success in this endeavor. Ameen!**

---

*Last Updated: 2025-11-16*
*Project Day: 0*
*Next Milestone: Moddio Tutorial Complete (Day 2)*
*Status: Ready to Begin*
