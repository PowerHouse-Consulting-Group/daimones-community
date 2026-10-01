# PH Discussion Thread Draft — post at producthunt.com/p/daimones (Discussions tab)

TITLE (pick one):
A) We benchmarked our $600 VM against GPT-5.4 on philosophy. We won. Here is the methodology.
B) Can an open-weight model out-reason frontier labs in a specialized domain? Our reproducible test says yes.

---

BODY:

Hello Product Hunt. I am Vasilis, solo founder of daimones. We launch here on October 13, and before that I want to put our central claim on the table where it can be challenged.

The claim: a self-hosted AI running an open-weight model (Qwen 27B, quantized) on a single $600/month VM can outperform frontier commercial models in a specialized domain, when the evaluation is done honestly.

What we did. We built a 10-question benchmark on Aristotelian philosophy, scored on four rubrics: terminology, structure, fidelity to primary sources, and reasoning. The part most benchmarks skip: we gave every model the identical Aristotle system prompt. Same input conditions, same rubric, same scoring. No vendor gets a home-field advantage.

Results from the September 2026 run:

- daimones: 84/100
- ChatGPT (GPT-5.4): 79
- Gemini 3.6-flash: 70.4
- Grok 4.3: 64.7

Full methodology, questions, and raw responses are published on our blog so anyone can reproduce or attack it. We did not test Claude because we have no API access, and we say so instead of hiding it.

Why this matters beyond our product. The frontier labs optimize for breadth and safety-by-hedging. A small team that owns its stack can optimize for depth in one domain: retrieval over primary philosophical texts, orthography validation for polytonic Greek, term injection tuned to Aristotelian vocabulary. That is not a fair fight in general knowledge. It is a fair fight in philosophy, and depth won.

The honest caveats, because you would find them anyway:
1. Ten questions is a small sample. We publish the rubric so you can judge whether it is fair, not just whether we won.
2. Our benchmark was built by us. Of course there is bias risk. The mitigation is full transparency of questions and scoring, and the identical-prompt rule.
3. We scored ourselves. If anyone wants to re-score the raw responses with our published rubric, the files are all there.

You can talk to the system right now without signup: the live demo runs as a HuggingFace Space (thevasilis/daimones). It is a thin proxy to our VM, single-turn and rate-limited, because it is one GPU-less box doing honest work.

Questions I am happy to answer here before launch: the benchmark design, the RAG stack, the sovereign-infrastructure economics, or why we chose Aristotle as the first persona instead of something more marketable.

Launching October 13. The demo link is open now if you want to form your own opinion first.

---

POSTING NOTES (not part of the body):
- Post this from your logged-in account under the product's Discussions tab
- Reply to every comment yourself in the first hours; founder responsiveness drives PH's "maker engagement" signal
- Do NOT ask for upvotes anywhere in the thread or replies
- If someone attacks the benchmark, thank them and point to the raw files; defensiveness is the worst outcome
- Best posting time: 1-2 days before launch (Oct 11-12) so the thread has traction on launch day
