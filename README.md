# GitTogether

Dating wrapper on top of GitHub
my yc caliber idea

hidden formula:
100 users, $100/month, $10k MRR

Normal dating apps:

- Fake bios
- Vibes > substance
- Zero signal

**GitHub = high-signal identity**

- Skills
- Consistency
- Obsession
- Taste (tech stack, OSS, side projects)

### User Flow

1. Login with GitHub OAuth
2. App auto-builds:
   - Skill graph
   - Interest vectors
   - Personality proxies (from behavior)

3. You swipe / match / connect
4. Chat unlocks **only after mutual intent**

## What Data You Pull From GitHub (IMPORTANT)

### Raw Inputs

- Repos (own + starred)
- Languages used (%)
- Commit frequency (time-of-day too)
- OSS contributions
- README tone (serious vs meme)
- Issues / PR comments (optional, risky)
- Topics/tags

### Derived Signals (this is your secret sauce)

- **Builder vs Talker**
  - Commits > stars

- **Depth vs Breadth**
  - Few langs deeply vs many shallow

- **Solo vs OSS**
- **Night owl vs morning grinder**
- **Experimental vs production mindset**

## Matching Logic (don’t do dumb cosine similarity only)

### Layered Matching

1. **Hard Filters**
   - Location / remote
   - Age range (legal stuff)
   - Intent (dating / collab / both)

2. **Skill Affinity**
   - Language overlap (weighted)
   - Domain overlap (web, infra, crypto, ML)

3. **Mindset Compatibility**
   - OSS heavy ↔ OSS heavy
   - Indie hacker ↔ indie hacker
   - ICPC grind ↔ ICPC grind

4. **Contrast Bonus (important)**
   - Frontend ↔ backend
   - Builder ↔ designer
   - Hardcore ↔ soft-skilled

Perfect similarity is boring.

## Chat & Interaction Rules (this decides success)

### Rules to avoid degeneracy:

- No instant DMs
- Unlock chat only after:
  - Mutual like
  - OR shared repo discussion

- First message prompt is **auto-generated**

  > “You both starred X and use Rust. What do you like/hate about it?”

### Services

- GitHub API (batched + cached)
- Background jobs (profile re-sync)
- Vector DB (optional later)

### Data Model (simplified)

```
User
- github_id
- skill_vector
- activity_score
- intent

Match
- user_a
- user_b
- score
- created_at

Message
- match_id
- sender
- content
```

## Privacy & Safety (skip this = dead product)

Hard rules:

- No private repos
- No commit diffs shown
- Opt-in visibility
- “Hide activity timing” toggle

Also:

- Women will be minority initially → protect them
- Rate limit likes
- Soft shadow bans for creeps

---

## Cold Start Problem (this will kill you if ignored)

### Hacky but effective:

- Invite-only alpha
- Target:
  - OSS contributors
  - Hackathon folks
  - Twitter/X devs

Let density build in **one niche first**:

> “Rust + OSS people in India / EU”

Don’t go global day 1.

---

## Monetization (don’t lie to yourself)

NOT subscriptions initially.

Possible:

- Boost visibility (soft)
- Events / meetups
- Hiring funnel later (careful)
- Premium insights (“who viewed your profile”)

If you monetize too early → trust dies.
