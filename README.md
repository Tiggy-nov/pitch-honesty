# Investor Narrative Architect

A model-agnostic skill for founders, investors, board members, and operators who need to turn a startup into a clear, exciting, evidence-backed venture narrative.

The skill runs in three passes:

1. **Investment Truth** — determine whether there is a venture-scale investment story before polishing language.
2. **Narrative Architecture** — sequence investor beliefs using strategic narrative, tension, simplicity, evidence, and reveal.
3. **Investor Room Simulation** — simulate the conversation after the founder leaves the room and expose where the story breaks.

The core rule is:

> Conviction through clarity, tension, and evidence — never hype.

## Repository structure

- `SKILL.md` — canonical, full version of the skill.
- `SYSTEM_PROMPT.md` — shorter portable instruction block for any AI system.
- `STARTER_PROMPTS.md` — reusable commands for common workflows.
- `INTAKE_TEMPLATE.md` — founder/company information to provide before analysis.
- `EVALUATION_RUBRIC.md` — investor scorecard and gating logic.
- `examples/SYNTHETIC_EXAMPLE.md` — small fictional example showing how to use the system.
- `CHANGELOG.md` — version history.

## Recommended usage

### ChatGPT

For a dedicated deck project, attach `SKILL.md` together with the pitch deck, customer notes, financials, product material, and market research. Then use one of the commands in `STARTER_PROMPTS.md`.

If you have access to a workspace feature that supports reusable skills/plugins, use the text of `SKILL.md` as the canonical skill instructions and keep the remaining files as reference material.

Do **not** put this entire skill into global Custom Instructions. It is intentionally specialised and should only activate for company narrative / fundraising work.

### Claude

Create a dedicated Project for the company and upload `SKILL.md`, `EVALUATION_RUBRIC.md`, and relevant company materials. Put the short operating instruction from `SYSTEM_PROMPT.md` into the Project instructions if desired.

For agent environments that support file-based skills, keep `SKILL.md` as the canonical source.

### Other AI tools

Upload `SKILL.md` as project knowledge or paste `SYSTEM_PROMPT.md` into the system/instruction layer. The framework does not depend on a specific model.

### Phase-aware storytelling

Version 1.1 adds a fundraising-stage layer inspired by Reece Chowdhry's October 2026 essay on what VCs mean by storytelling.

The same strategic narrative is now expressed at three densities:
- **Attention** — first 30 seconds / first call: earn the right to continue.
- **Detail** — partner meetings and diligence: turn curiosity into evidence-backed belief.
- **Closing** — IC and final decision: make the case easy for an internal champion to retell and defend.

The skill now includes a 30-second attention gate, repeat-back test, useful-question test, three-chapter founder introduction, live-vs-send-ahead deck distinction, and a mission/mountain framework.

## Recommended workflow

**New company**
1. Fill in `INTAKE_TEMPLATE.md`.
2. Run `Pass 1`.
3. Fix business/evidence gaps.
4. Run `Pass 2`.
5. Build or rewrite the deck.
6. Run `Pass 3`.
7. Rebuild anything that fails the investor-room test.

**Existing deck**
1. Upload the deck and source materials.
2. Ask for `Full Three-Pass Review`.
3. Do not redesign the slides until Pass 1 identifies which problems are narrative problems versus underlying business problems.

## Operating philosophy

This is not a “make my pitch sound better” prompt.

The system must be willing to say:

> This is not a storytelling problem. The underlying investment thesis is unclear.

It distinguishes facts, founder claims, model inference, investor assumptions, and unproven hypotheses. It never invents proof.

## Version

Current version: **1.1.0**
