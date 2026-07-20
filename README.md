# Sina Naeemi

Software engineer and independent ML researcher working on model internals, mechanistic interpretability, and reliable AI systems.

I build empirical tools and controlled experiments for examining how language models represent and use information. A recurring distinction in my work is between **decodability**—what can be read from an activation—**behavioral improvement**—what changes in an output—and **causal use**—what the model's computation depends on when an intervention is made.

My research spans sparse autoencoders, activation steering, Jacobian-lens readouts, and latent intermediate computation. Alongside research, I build production AI and infrastructure systems that keep model behavior grounded in structured context, preserve human review, and treat reliability as an engineering requirement.

## Current research

**SmolLM3/J-space — ongoing.** I am designing controlled experiments that test whether alternative supervision changes causally used intermediate representations rather than merely changing outputs. The work uses SmolLM3-3B, Jacobian-lens readouts, matched controls, and activation interventions as measurement tools. It is ongoing research, not a publication or a completed causal result.

The evaluation is designed to keep three findings separate: a representation may be decodable without affecting behavior; an intervention may improve a response without establishing a durable intermediate representation; and a causal-use claim requires appropriate controls, interventions, and replication. The aim is to test those distinctions directly before crediting an approach with an improvement.

## Selected work

1. [**Steering a GPT with Its Own Features**](https://ceena.dev/sae-steering) — completed public artifact. I trained a language model and sparse autoencoders on residual-stream activations, learned sparse feature directions, and applied inference-time residual-stream interventions. Distributed, layerwise activation interventions causally redirected generated behavior without weight edits, while also exposing the limits of sparse feature analysis in superposed representations.
2. **Latent Intermediate Representations in SmolLM3-3B — ongoing** — controlled research on whether different supervision formats change intermediate computation in ways that survive matched controls and causal tests. No public repository is linked while the work remains in progress.
3. [**Inference Benchmark**](https://ceena.dev/inference) — a public benchmarking API and dashboard for comparing LLM-serving configurations across workload profiles. It records configurations and results for like-for-like comparisons and clearly flags simulated results when a model server is unavailable.
4. [**Production AI systems**](https://ceena.dev) — grounded, human-in-the-loop systems that turn unstructured inputs into reviewable workflows, with explicit uncertainty handling and reliability controls.

## Research approach

- Separate causal interventions from readouts: an interpretable signal is not automatically a causally used one.
- State hypotheses as hypotheses and distinguish them from observed results.
- Design matched controls and falsification checks before claiming an improvement.

## Tools

Python, PyTorch, TypeScript, React, Next.js, FastAPI, SQL, Redis, Docker, TensorRT-LLM, and Azure.

## Links

- [Website](https://ceena.dev)
- [LinkedIn](https://www.linkedin.com/in/sina-naeemi-74a3581b8/)
