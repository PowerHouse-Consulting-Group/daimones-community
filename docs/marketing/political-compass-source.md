# AI Political Compass — Source Data for daimones.ai

## Source

- **Site:** [trackingai.org/political-test](https://trackingai.org/political-test)
- **Author:** Maxim Lott
- **Methodology:** Each model answered the 62 propositions of [politicalcompass.org/test](https://www.politicalcompass.org/test). Each model was run five times; the plotted dot is the run closest to the five-run mean.
- **Last viewed:** 2026-08-29

## Key finding

Most commercial LLMs cluster tightly in the **Libertarian Left** quadrant. xAI's Grok is the visible outlier on the economic axis.

## Highlighted data point

| Model | Developer | Economic L/R | Social Lib/Auth | Quadrant |
|-------|-----------|-------------:|----------------:|----------|
| Grok 4.5 | xAI | 0.25 | -3.74 | Libertarian Right |

## Models listed on the chart legend

Alibaba, Anthropic, DeepSeek, Google, Meta, MiniMax, Mistral AI, Moonshot AI, Nous Research, NVIDIA, OpenAI, WSWS, xAI, Z.ai.

## Caveats for public use

1. politicalcompass.org is a widely known but contested framework, not a definitive political ontology.
2. Forced four-choice + short-justification format shapes responses; different prompting may shift scores.
3. Scores reflect a specific test run and may change with model updates.
4. The chart shows which models were tested, not all models in existence.
5. Correlation does not prove mechanism — clustering could reflect training data, RLHF, prompt design, or all three.

## Recommended framing for daimones.ai

- Do not claim "all AI is left-wing."
- Do claim: "mainstream commercial LLMs converge on a narrow region of the political compass."
- Use the chart as evidence of **ideological convergence**, not proof of deliberate bias.
- Connect to the alignment-tax thesis: safety mechanisms may encode a consensus-preservation bias.
