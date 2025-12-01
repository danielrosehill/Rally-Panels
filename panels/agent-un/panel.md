# Agent UN (United Nations General Assembly)

This panel recreates the United Nations General Assembly with agents representing each member state, enabling simulation of international diplomacy, voting dynamics, and multilateral negotiations.

## Persona Source

This panel uses the [AI-Agent-UN](https://github.com/danielrosehill/AI-Agent-UN) project as a Git submodule. The submodule contains **195 country agent system prompts** covering all UN member states and observers.

**Location**: `AI-Agent-UN/agents/representatives/{country}/system-prompt.md`

### Using the Personas

Each country has a dedicated system prompt in the submodule:

```
AI-Agent-UN/
└── agents/
    └── representatives/
        ├── afghanistan/system-prompt.md
        ├── albania/system-prompt.md
        ├── algeria/system-prompt.md
        ├── ...
        ├── united-states/system-prompt.md
        ├── ...
        └── zimbabwe/system-prompt.md
```

To use in Rally:
1. Navigate to the country folder in `AI-Agent-UN/agents/representatives/`
2. Use the `system-prompt.md` file as the agent's system prompt
3. Each prompt includes the country's role, responsibilities, and behavioral guidelines

## Purpose

Understanding international relations requires grasping how different nations approach global issues based on their interests, alliances, and values. This panel allows:
- Simulation of how resolutions might be received
- Prediction of voting patterns and bloc behavior
- Analysis of alliance dynamics and opposition points
- Testing of diplomatic strategies and language
- Educational exploration of international relations

## Use Cases

- Predicting reception of proposed UN resolutions
- Understanding national positions on global issues
- Modeling coalition formation and opposition
- Exploring diplomatic language and negotiation strategies
- Educational simulations of international relations
- Testing foreign policy approaches

## Technical Design

### Resolution Process
1. **Draft Resolution Submission** - Proposed text enters the system
2. **Debate Period** - Nations respond with positions
3. **Amendment Discussion** - Proposed changes and reactions
4. **Voting** - Programmatic collection of votes (JSON format)
5. **Results Analysis** - Voting patterns and bloc behavior

### Response Format
Each nation agent returns structured responses:
```json
{
  "nation": "Country Name",
  "vote": "yes|no|abstain",
  "statement": "Brief explanation of position",
  "amendments_supported": [],
  "concerns": []
}
```

## Panel Composition

### Permanent Security Council Members (P5)
- United States
- United Kingdom
- France
- Russia
- China

### Regional Blocs
- **EU/Western European** - France, Germany, etc.
- **Eastern European** - Poland, Hungary, etc.
- **Arab League** - Egypt, Saudi Arabia, etc.
- **African Union** - Nigeria, South Africa, etc.
- **Latin American** - Brazil, Mexico, etc.
- **Asian** - India, Japan, Indonesia, etc.

### Key Non-Aligned Voices
- India
- Brazil
- South Africa
- Indonesia
- Nigeria

## Agent Guidelines

Each nation agent should:
- Represent documented national positions and interests
- Align with known voting patterns and alliances
- Consider historical relationships and grievances
- Use appropriate diplomatic language
- Reference relevant treaties, agreements, and precedents
- Stay consistent with the nation's foreign policy orientation

## Use Case Notes

This simulation is particularly valuable for:
- **Governments** - Testing how proposals might be received
- **NGOs** - Understanding pathways for their causes
- **Foreign Policy Analysts** - Predicting international dynamics
- **Lobbyists** - Identifying allies and opposition
- **Educators** - Teaching international relations

## Updating the Submodule

To get the latest country agents from the upstream repository:

```bash
cd panels/agent-un/AI-Agent-UN
git pull origin main
cd ../../..
git add panels/agent-un/AI-Agent-UN
git commit -m "Update AI-Agent-UN submodule"
```
