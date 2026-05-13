# §1.1 The thread

<!-- Last updated: 2026-05-05 -->

---

When I sat down to write this thesis, it felt like connecting dots with a thread. Seven years of experiments, analyses, papers across hippocampal neurons, large language models, and self-improving agents looked, at first glance, like stars with no relation to one another. Until I found the constellation.

The thread that connects all is memory.

It has always been memory. From the start.

The pull, for me, was almost philosophical before it was scientific. Perhaps like many students of neuroscience, I started as a student of philosophy and psychology, drawn by the deepest quest: know thyself. I believed that studying memory was the key to understanding ourselves. As Oliver Sacks put it: "We are our memories." This was the reason I worked on the first serious project of my scientific career [sun2020].

[sun2020] revealed that the hippocampus encodes not just *where* you are, but events --- discrete, transferable units of experience. The most striking demonstration came from a simple manipulation: we changed the maze geometry from a square to a circle. Place cells scrambled completely, every spatial field remapping to a new location. But the cells tracking which lap the animal was on --- the event code --- barely moved. Square or circle, lap three was still lap three. The event is more abstract than the map.

[zutshi2025] pressed on a different question: what is memory *for*? The answer was action. Memories are the key not to the past, but to the future. The brain was not just recording where it had been --- it was preparing for where it needed to go. The activity patterns of hippocampal neurons reflect an internally generated action plan, updated moment to moment. I can still remember the excitement when I first saw it: rotating a three-dimensional UMAP embedding of hundreds of neurons, watching the manifold organize itself according to the animal's unfolding plan.

[yang2024selection] followed memory into a different brain state --- NREM sleep --- asking which fragments the sleeping brain chooses to replay during sharp wave ripples, and why. Three analogies help me picture it. A bridge: connecting waking experience to sleeping consolidation across two very different brain states. An emergency room: triaging what needs to be prioritized before morning. A tag: attached during waking, followed during sleep. None of these is fully precise. All three are pointing at something true.

[yang2023nreps] extended this picture by asking how the geometry of hippocampal memory shifts across brain states. NREM sleep, as expected, faithfully recapitulates the manifold of activity seen during waking maze exploration --- the sleeping brain replays the day's experience in recognizable form. But REM sleep does not resemble waking activity at all. The manifold is something else entirely. The dominant picture of sleep-dependent memory consolidation --- sequential replay, faithful reactivation --- holds for NREM and breaks for REM. If REM matters for memory, it matters in some other way. Perhaps it transforms rather than replays. Perhaps it abstracts, or generalizes across experiences in a form that faithful reactivation cannot. That question is still open.

The memories I have been tracing in the brain above are episodic. LLM "memory" is a different thing entirely. It is closer to semantic memory: the entire human internet data encoded during pretraining, parameterized by billions or trillions of weights. The training corpus becomes the weights, and the weights become parametric memory, compressed and distributed.

Yang et al. (2024) looked inside the residual stream of 23 language models and found something interesting: a linear "truth direction" — a direction in activation space that reliably separates what the model internally represents as true from what it represents as false. When a model is instructed to lie, the truth vector rotates with respect to its orginal direction. Suggesting that LLM has a internal representation of what it regard as true.

CASAL (Yang et al., 2026) started by asking: does an LLM "know" what it knows? Surprisingly, yes — but only if you look inside. The internal activations encode a clear boundary between what the model knows and what it does not, and yet the outputs don't honour that boundary: the model hallucinates, producing confident answers that is wrong with respect to both the ground truth even when its own hidden states have already flagged as unknown. Why? We hypothesized that the standard training objective provides a learning signal from outside — from the training corpus, from human raters, from a reward model. We proposed an alternative: train directly from the model's own internal representations.


