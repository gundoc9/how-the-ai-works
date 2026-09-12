# Sources and how far each was checked (v22, 12 September 2026)

What "checked" means here, in three grades:
- **Full text read**: the paper was fetched and read in this session before the context was compacted; the numbers on the card were recorded at the time and one (six orders of magnitude) re-verified afterwards from the paper's own figure caption.
- **Abstract read**: the arXiv abstract page (or the journal abstract) was returned by a web search this session and read; the card's claim is checked against that abstract only. Anything in a paper's body that would qualify the claim has not been read.
- **Summary only**: no source is at this grade as of v13.

Every arXiv identifier came from a search result in this session, not from memory, and each links to `arxiv.org/abs/<id>`. Journal volumes and pages were kept only where a search result showed them; the two I could not confirm (Wei 2022, Turpin 2023) were cut back to venue and year. Each card prints the grade beside its source.

| Source | Grade | Cards | What the card claims from it | Supported by |
|---|---|---|---|---|
| Sennrich 2016, arXiv 1508.07909 | abstract | Token | subword units from byte-pair encoding, borrowed from compression | abstract |
| Kaplan 2020, arXiv 2001.08361 | full text | Token, Parameters | L(N) = (8.8e13 / N)^0.076; doubling parameters cuts loss ~5%; 1.4 tokens per word on WebText2; vocabulary 50,257; six orders of magnitude in N; constants depend on tokeniser | full text; caption re-verified |
| Holtzman 2019 v1, arXiv 1904.09751 | full text | Next token, Temperature, Sampling | temperature formula; greedy repeats, full sampling degenerates; tail holds about a third of the mass (0.31) | full text (the "within three tokens" clause was removed as unverifiable after compaction) |
| Liu 2024, TACL 12:157-173 | abstract | Context window | start and end of a long input used better than the middle | abstract |
| Ouyang 2022, NeurIPS | abstract | Training, RL | pretrain / demonstrations / rankings; 1.3B tuned preferred over 175B untuned | abstract |
| Kalai and Vempala 2024, STOC | abstract | Hallucination | calibrated models must hallucinate one-off facts at a rate tied to their frequency | abstract |
| Kalai, Nachum, Vempala, Zhang 2025, arXiv 2509.04664 | abstract | Hallucination | evaluations that reward guessing over admitting uncertainty push hallucination up; restates the 2024 bound as a rate at least the share of facts seen once | abstract, plus a body snippet with the 20% birthday example |
| Kadavath 2022, arXiv 2207.05221 | abstract | Calibration | well calibrated on multiple choice in the right format; can estimate P(true) of own answer | abstract |
| Lewis 2020, NeurIPS 33:9459-9474 | abstract | Retrieval | more specific and factual output than parameters alone | abstract |
| Cheng 2024, arXiv 2403.12958 | abstract | Knowledge cutoff | effective cutoff differs by source and from the reported one | abstract |
| Bommasani 2021, arXiv 2108.07258 | abstract | Foundation model | emergence with scale; homogenisation onto few models | abstract |
| Greshake 2023, AISec | abstract | System prompt | instructions in retrieved or pasted content can be followed (indirect prompt injection) | abstract |
| Hoffmann 2022, arXiv 2203.15556 | abstract | Parameters | for a fixed budget, data should grow as fast as parameters; earlier models undertrained | abstract (verified 3 Sep; was citation-only in v3-v11) |
| Mikolov 2013, arXiv 1301.3781 | abstract | Embedding | vectors learned from context carry syntactic and semantic similarity; vector arithmetic lands on related words | abstract plus a PDF snippet showing the arithmetic example |
| Wei 2022, NeurIPS | abstract | Reasoning tokens | writing steps raises accuracy on arithmetic and reasoning; emerges with scale | abstract |
| Turpin 2023, NeurIPS | abstract | Reasoning tokens | written explanations can omit what actually swayed the answer | abstract |
| DeepSeek-AI 2025, Nature 645:633-638 | abstract plus reward section | Reasoning tokens, RL | reasoning behaviour emerged from RL with checkable rewards; learned reward models can be gamed | abstract; the reward section states neural reward models are susceptible to reward hacking during large-scale RL |
| Sharma 2023, ICLR 2024 | abstract | Sycophancy | assistants sycophantic across tasks; preference data prefers agreeing answers over correct ones a non-negligible fraction of the time | abstract |
| Schick 2023, NeurIPS | abstract | Tool use | a model can learn which tool to call and when | abstract |
| Yao 2022, ICLR 2023 | abstract | Tool use | interleaving reasoning and actions gathers information from external sources | abstract |
| Dosovitskiy 2020, ICLR 2021 | abstract | Images as tokens | pure transformer on image patches matches the convolutional networks of the time when pre-trained on large data; 16x16 patches from the title | abstract and title |
| Singhal 2023, Nature 620:172-180 | abstract | Benchmark | 67.6% on MedQA (USMLE-style); human evaluation reveals gaps | abstract |
| Sainz 2023, Findings of EMNLP | abstract | Benchmark | contamination inflates scores; extent unknown, hard to measure | abstract |
| Packer 2023, arXiv 2310.08560 | abstract | Memory, Harness | virtual context management, text paged in and out of a fixed window like an operating system | abstract |
| Zheng 2023, arXiv 2306.05685 | abstract | Evals | a strong model as judge agreed with human raters over 80% of the time, about the human-human level, with position, verbosity and self-enhancement biases | abstract (checked 9 Sep) |
| Gallifant 2025, Nat Med 31:60-69 | abstract | Evals | TRIPOD-LLM reporting guideline: transparency, human oversight, task-specific performance reporting | abstract (checked 9 Sep) |
| Sumers 2023, arXiv 2309.02427 | abstract | Harness | a language agent as a model plus modular memories, an action space and a decision procedure | abstract (checked 10 Sep) |
| Patel 2024, ISCA, arXiv 2311.18677 | abstract | Prefill and decode | two phases per request, compute-intensive prompt computation and memory-intensive token generation, the second one token at a time from the cached context | abstract (checked 12 Sep) |

Not checked: the body of any abstract-grade paper beyond the two sections named above. A full-text pass over the 26 is about twenty-six fetches and one session; the abstracts support every claim as it is now worded, so the risk is nuance, not contradiction.

Dr Ganesh Sivasankara · MD · FRCA · FCARCSI · Consultant Anaesthetist
