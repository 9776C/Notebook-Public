# Scoring System Overview

## Identify:

### Problems with Old Scoring (and Intake):

Our past bot used rollers to pull blocks from the basket and score them. This method worked decently well and was able to move a lot of blocks pretty quickly. But had some issues:

1. **Rubber band entanglement** - The intake relied on rubber bands, which were really good at intaking but would get entangled with other bots. This would either:
    - Break the rubber bands completely
    - Make our bot stuck to the opponent for the rest of the match
2. **Jamming when overheated** - The system would jam if the motors got too hot during extended use
3. **Size** - The system was almost or more than half the bot and we couldn't fit under the goal
4. **Middle/Bottom goal** - The old system could *barely* score in the middle goal if at all, and could only really score one block at a time in the bottom goal.

### What Worked Well:

- Fast block movement
- Effective intake (when not entangled)
- Generally consistent performance under normal conditions

### Goals for New Scoring System:

- **Extremely fast** scoring capability
- **More reliable** (jamming)
- **No overheating** issues under full match load
- Ability to score **specific quantities** of blocks (important for autonomous)
- **Color sorting** capability for strategic play
- Fit under long goal

## Brainstorm:

### Research - Current Meta:

Looking at top-performing bots at competitions, we've identified several effective scoring mechanisms:

1. Basket - What we used before, moderate speed
2. Lever - Currently the fastest method (6 blocks in ~0.5 seconds)
3. S-bot -
4. C-bot - 


### Dual-Chamber Idea:

Regardless of which mechanism we choose, we're considering using **2 scoring chambers side-by-side** that converge into one output point. But there are multiple way to push the blocks:
- [Arc Scoring](01-arc-scoring.md)
- [Linear Scoring](02-linear-scoring.md)


#### Potential Advantages:

- **~12 block capacity** (double the standard 6)
- **Color sorting** - one color per chamber
- **Strategic flexibility** - can score from either chamber independently
- **Redundancy** - if one jams, we can still use the other
- **Very fast** - SPEED 

---

## Scoring Methods Under Consideration:

1. [Arc Scoring](01-arc-scoring.md) - Arc/lever mechanism analysis
2. [Linear Scoring](02-linear-scoring.md) - Linear elastic-powered system
3. [S Scoring](03-S-scoring.md) - S-shaped path variation
4. [C Scoring](04-C-scoring.md) - C-shaped path variation



	  Zach/Daren 12/10/2025-12/12/2025