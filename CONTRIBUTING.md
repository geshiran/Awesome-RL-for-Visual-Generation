# Contributing

Thank you for helping improve **Awesome RL for Visual Generation**.

This repository is meant to be a polished public resource hub. Contributions should be useful to readers who want to understand how reinforcement learning and reward-based alignment interact with visual generative model interfaces.

## What to Contribute

Good contributions include:

- Public papers with stable paper, project, or code links.
- Concise notes that clarify where a method fits in the taxonomy.
- Reward models, evaluators, and benchmarks for visual generation.
- Corrections to metadata such as venue, year, task, or method family.
- Reading-roadmap suggestions for newcomers.

Please keep entries concise and neutral. This is a curated resource list, not a leaderboard.

## What Not to Contribute

Please do not submit:

- Non-public survey material.
- Internal files or local-only materials from the survey project.
- Confidential project correspondence or internal evaluation material.
- Broken links, placeholder URLs, or empty sections.
- Promotional text that does not help readers understand the method.

## Paper Entry Style

Use this style in Markdown files:

```md
- **Short Name**: Full Paper Title [[Paper]](PUBLIC_PAPER_URL) [[Code]](PUBLIC_CODE_URL) <sub>Venue Year | Model Family | Reward Type | Method</sub>
```

Omit `[[Code]]` or `[[Project]]` if no stable public link is available.

Use this style in `data/papers.yaml`:

```yaml
- id: short-lowercase-id
  name: Short Name
  title: "Full Paper Title"
  year: 2024
  venue: ICLR
  model_family: diffusion
  category: trajectory_scalar_reward
  tags:
    - policy_gradient
    - text_to_image
  links:
    paper: PUBLIC_PAPER_URL
    code: PUBLIC_CODE_URL
```

## Taxonomy Guidelines

Prefer model-interface categories over broad algorithm labels:

- **Diffusion**: denoising trajectory as policy, preference objective, reward backpropagation, distillation.
- **Flow matching**: deterministic flow, stochasticized flow, dynamic-control view, proximal RL.
- **Autoregressive visual generation**: visual token policy, outcome reward, process reward, multimodal interface.
- **GANs and VAEs**: latent action spaces, adversarial or learned rewards, controllable latent structure.
- **Rewards and evaluators**: proxy metric, human preference model, VLM judge, benchmark diagnostic.

When a method crosses categories, place it where the optimization interface is most explicit and mention the secondary category in tags.

## Pull Request Checklist

Before opening a pull request, check that:

- All links are public and stable.
- The entry has a clear model family and method category.
- The contribution does not disclose private survey material.
- The Markdown renders cleanly.
- `data/papers.yaml` remains valid YAML.

## Tone

Use academic, descriptive language. Avoid claims such as "best", "solves", or "state-of-the-art" unless the wording is tied directly to a paper title or a clearly scoped benchmark claim.
