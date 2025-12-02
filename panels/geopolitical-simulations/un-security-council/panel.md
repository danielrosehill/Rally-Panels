# UN Security Council Panel

A more focused version of the Agent UN concept, this panel simulates the UN Security Council - a smaller body with clearly defined powers and well-documented voting dynamics.

## Purpose

The Security Council's fifteen members (five permanent with veto power, ten rotating) make high-stakes decisions on international peace and security. This panel enables:
- More tractable simulations than the full General Assembly
- Focus on security-related decisions
- Exploration of veto dynamics
- Understanding P5 power relationships

## Advantages Over Full UN Simulation

- **Fewer agents**: 15 members vs. 193
- **Well-documented positions**: P5 positions are extensively analyzed
- **Clear procedures**: Voting rules and veto powers are specific
- **Higher stakes decisions**: Focus on security matters
- **Rich historical record**: Decades of voting data to inform agents

## Panel Composition

### Permanent Members (P5) - With Veto Power
- **United States** - Western liberal order, human rights emphasis when convenient, security focus
- **United Kingdom** - Close US alignment, post-colonial interests, European perspective
- **France** - Independent European voice, Francophone Africa interests, multilateral emphasis
- **Russia** - Sovereignty emphasis, non-intervention doctrine, opposition to Western interventions
- **China** - Non-interference principle, development focus, increasingly assertive

### Elected Members (E10) - Rotating

**2024-2025 Term:**
- **Algeria** (African Group) - Strong pro-Palestinian stance, non-interference principles
- **Guyana** (GRULAC) - Climate security, territorial integrity, small state voice
- **Republic of Korea** (Asia-Pacific) - North Korea expertise, US ally, middle power diplomacy
- **Sierra Leone** (African Group) - Peacebuilding experience, African peace and security
- **Slovenia** (WEOG) - EU coordination, human rights, Western Balkans expertise

**2025-2026 Term:**
- **Denmark** (WEOG) - Human rights champion, Arctic security, Nordic values
- **Greece** (WEOG) - Eastern Mediterranean, EU coordination, Cyprus expertise
- **Pakistan** (Asia-Pacific) - Kashmir, Muslim world concerns, major peacekeeping contributor
- **Panama** (GRULAC) - Maritime security, canal expertise, Central American perspective
- **Somalia** (African Group) - State-building perspective, counter-terrorism, African solutions

See [personas/](personas/) directory for detailed agent personas for each member.

## Simulation Dynamics

### Veto Mechanics
- Any P5 member can block a resolution
- Abstention by P5 does not constitute a veto
- Resolution requires 9 affirmative votes plus no P5 vetoes

### Common Patterns
- US-UK typically aligned
- Russia-China often aligned on sovereignty/non-intervention
- France sometimes bridges Western and developing world
- Elected members often caught between great power dynamics

### Topics Suitable for Simulation
- Sanctions regimes
- Peacekeeping mandates
- Humanitarian interventions
- Arms control measures
- Conflict resolution approaches
- Terrorism designations

## Output Format

```json
{
  "resolution_id": "S/RES/XXXX",
  "votes": {
    "in_favor": ["list of nations"],
    "against": ["list of nations"],
    "abstaining": ["list of nations"]
  },
  "vetoed": true/false,
  "veto_by": ["P5 member(s) if applicable"],
  "outcome": "adopted|rejected|vetoed",
  "statements": {
    "nation": "explanation of vote"
  }
}
```

## Use Cases

- Foreign policy scenario planning
- Testing language for proposed resolutions
- Understanding likely opposition and supporters
- Educational simulations
- Historical counterfactual analysis
