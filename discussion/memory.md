


- long context
	- 10M, 1M context
- compression
- context engineering
- persistent memory
	- file system
		- read and write
	- https://manus.im/blog/Context-Engineering-for-AI-Agents-Lessons-from-Building-Manus
- dream based memory



# Evolution of memory 

### Expanding Context Windows: Scaling Working Memory

Initially, the primary approach to giving an agent "memory" was simply to expand the model's context window.

By allowing models to ingest hundreds of thousands (or millions) of tokens at once, the agent could hold an entire codebase or conversation history in its immediate attention. However, this brute-force approach functions purely as an expanded working memory. It is computationally expensive, vulnerable to "lost-in-the-middle" retrieval failures, and fundamentally resets once the session ends. It does not allow the agent to build structural knowledge or learn from one episode to the next.

The first move (2023–2024) was brute force — 4K → 32K → 200K → 1M tokens. The implicit theory was that memory is just attention over a long-enough buffer. If the agent can see the whole trajectory, it can reason over the whole trajectory. This worked surprisingly well for a while and is still the dominant primitive.


He frames the context window as working memory and then does the back-of-envelope: humans hold about seven items in working memory; current models hold millions or tens of millions of tokens. But we're trying to stuff everything in, including unimportant or wrong information. The brute-force approach doesn't seem reasonable. If you try to process real-time video and naively record all tokens, a million tokens is only about 20 minutes of video. Even a 10-million-token context window holds only about 20 minutes of raw video — laughably insufficient for a persistent assistant that needs to understand a user's life over weeks or months. "We're kind of using duct tape right now… shove it all in the context window… this seems a bit unsatisfying.


### Context Engineering 

To move beyond ephemeral working memory, architectures shifted toward context engineering and retrieval-augmented generation (RAG). Here, memory became a distinct, searchable database rather than a continuous stream of tokens.

More recently, this has evolved into modeling memory as an actual file system that the agent actively manages. Using standard tools (like bash or grep), an agent can organically split, hierarchically organize, and update its own memory files as it works [05:34]. In multi-agent environments, this allows for discrete permission scopes—such as read-only access to organization-wide runbooks and read-write access for active task state. While this grants agents a functional scratchpad and procedural memory, it remains a reactive, siloed process where individual agents might fail to share high-level insights.


 Then the cracks showed. Needle-in-a-haystack benchmarks uncovered "context rot": as tokens accumulate, recall degrades — so even below the hard limit, the agent gets less out of each token. Frontier agents started running tasks equivalent to ~70 hours of human work, with complexity doubling roughly every 7 months per METR, and that exposed the real bottleneck: context is cumulative, every tool call and every reasoning step gets carried forward, and you hit a wall that isn't the token limit — it's signal-to-noise. The response was to treat context as a finite resource with diminishing marginal returns, where the discipline is finding the smallest set of high-signal tokens that maximize the desired outcome.

 That discipline is what people now call context engineering, and it splits roughly two ways. The external-controller school — RAG, sliding windows, summarization, vector stores for episodic memory — treats memory management as plumbing around the model. The newer "Memory-as-Action" framing pushes back on this: rule-based operations decouple memory management from the agent's reasoning policy, making it impossible to learn a coherent strategy that balances task performance against resource costs end-to-end. Context curation should be an intrinsic, learnable capability of the agent itself. You're seeing this in MemAct, Memex (indexed experience memory with explicit Read/Compress actions), and Weaviate-style dual-store architectures. The common move: the agent decides what to write, what to recall, what to forget — memory becomes part of the policy, not a wrapper around it.



### Dreaming: Offline Memory Consolidation

Context engineering, even the learned variety, is within-session memory management. The agent is still doing it while working. Dreaming is a scheduled process that runs between sessions, reviewing agent sessions and memory stores, extracting patterns, and curating memories so agents improve over time. Anthropic frames this as the difference between "learning" during work and "understanding" after work.


The most recent leap in agent memory transitions systems from real-time state management to offline self-improvement. Anthropic recently introduced this as "Dreaming," an asynchronous, out-of-band batch process that runs entirely separate from an agent's active tasks.

Mechanically: a dream reads an existing memory store alongside past session transcripts and produces a new, reorganized store — duplicates merged, stale or contradicted entries replaced, new insights surfaced. The input store is never modified, so you can review and discard. It analyzes up to 100 historical sessions and the entire memory store, writes results to a new memory file rather than overwriting, and is currently in research preview behind the dreaming-2026-04-21 beta header. Critically, dreaming surfaces patterns a single agent can't see on its own — recurring mistakes, convergent workflows, team-wide preferences — and in multiagent setups it pulls shared learnings across agents


Operating remarkably similarly to hippocampal replay in biological neural networks, Dreaming extracts generalized abstractions from raw episodic traces. While an agent (or a swarm of agents) executes discrete tasks during its "waking" state, the Dreaming process later scans through the transcripts of those sessions to look for recurring patterns, failed tool calls, and successful strategies


The resonance with your work is almost on-the-nose. This is offline replay-driven consolidation: recent experience replayed during downtime, schema-consistent items integrated, noise pruned, and — the part I think is genuinely interesting — cross-agent consolidation that synthesizes separate learnings into a unified memory entry

auto-dream 

```
You are performing a dream — a reflective pass over your memory files. Synthesize what you've learned recently into durable, well-organized memories so that future sessions can orient quickly.
Memory directory: ~/.claude/projects/<project>/memory/
This directory already exists — write to it directly with the Write tool (do not run mkdir or check for its existence). system prompt for claude.
```


REM sleep random. Randomness 

spatial temporal recombination and creativity

