# critique


- The Model being "stateless" is true at the API level but the Harness manages continuity for the user. The concern from not emphasizing this is confusion; since obviously the agentic AI as a whole maintains continuous comprehension over a session.


- The transition from case studies to agentic AI narrative is abrupt.  The reader is left wondering: How would the Noble lab or the Math AI Lab actually use agentic AI differently? One or two sentences per case study connecting them to the efficiency/learning rules would close this gap.


- Part 2 opens with "Here we will articulate strategies and examples" but the framework section (Harness/Connector/Model) reads more like background than strategy. Consider placing the framework earlier — perhaps at the end of Part 1 as a "How it works" bridge — so Part 2 can open directly with actionable material (Rules 3–7).


- "Stateless" appears in both Part 1 (Rule 2, about stupidity) and Part 2 (the framework). In Rule 2, statelessness supports the social argument ("it forgets, so it can't judge you"). In the framework it's a technical fact about payload construction. These are different uses of the same concept and could confuse a non-technical reader who encounters the term first in a social context and later in an architectural one. A brief forward-reference in Rule 2 ("we will explain why in Part 2") would help.*


- The "accountability deficit" in Rule 1 is well-defined, but the assertion that it "can accumulate rapidly and even imperceptibly" is stated without elaboration. An example — say, chaining multiple AI outputs where each depends on the last — would make the accumulation mechanism concrete rather than abstract.


- The case studies are strong but uniform in structure (description → blockquote). Revisit the interspersed punchline remarks, thematically: "What agentic AI is doing or could be doing here" as part of the impedence matching.


- Rule 5 ("Meta-vate") is the most compelling section because it shows real prompts. Consider promoting it or at least cross-referencing it earlier — readers who skim will benefit from seeing concrete examples before abstract rules.


- Document voice shifts between casual and formal:  Pick one register (suggest casual) and maintain it. 


- Brief glossary defining: LLM, API, context window, LoRA, OCR, and other acronyms that appear without expansion for non-specialist readers. Some are defined inline (OCR) but others (LoRA, YOLO, CLIP) are not.



Here is a 6-AUG-2026 Critique to factor in: 


### Omissions


The Part 1 conclusion is still a visible TODO: "To do: Conclude Part 1 by reconnecting the case studies with what we have so far in terms of efficiency and learning." This is the most conspicuous missing piece. The case studies are orphans without a paragraph that ties them back to accountability deficit and stupidity freedom.


Rule 6 is still a placeholder with a visible "To do: section is light." tag. If you're not ready to write it, consider collapsing it into a brief statement or deferring it to a future revision rather than leaving the scaffolding exposed.


No mention of cost in a literal/financial sense. You mention a learning curve cost and accountability cost, but token-based billing is a real factor for researchers on grant budgets. The framework section mentions billing in passing (under Harness) but it never surfaces as a practical concern. A sentence or two somewhere — maybe under Rule 1 — would ground it.


No mention of data sensitivity / privacy. Researchers working with IRB-governed data, HIPAA data, or export-controlled data have a real question: What happens to my prompt content? Does it leave my machine? Does it get stored? This matters particularly for the Michaelsen (clinical) and Noble (genomic) case studies. Even a brief caveat would serve your audience.


The Activities section mentions MCP servers but the framework section already explained MCP as "plumbing you don't need to worry about." These two messages conflict slightly. If an activity asks people to investigate MCP, you should set that expectation somewhere in the framework discussion.


### Inaccuracies / Questionable claims


"$data \to analysis$" uses LaTeX math notation, which won't render in standard GitHub-flavored markdown. It'll display as literal $data \to analysis$. Use an arrow character (→) or rephrase.


"The current term of art context engineering has replaced the earlier term prompt engineering." — This is debatable. Both terms are in active use. "Context engineering" emphasizes the broader payload (system prompts, tool results, steering), while "prompt engineering" emphasizes the user-facing input. Saying one "replaced" the other overstates the situation. More accurate: "Context engineering is emerging as a broader framing that subsumes prompt engineering."


The Harness description says "possibly running in a data center far away." This is accurate for the Model, but the Harness itself runs locally (it is your IDE). The sentence is correctly placed under the Harness section describing the connection to the Model, but a hasty reader might misparse it as saying the Harness is remote.


### Sections that read AI-generated (the ground loop problem)


The entire Framework section (items 1–5) is the most obviously AI-written material. The tells:


Perfectly parallel structure across all five items
Explanatory parentheticals that define obvious terms for the reader ("this is what makes the system 'agentic'")
The closing aphorism "Tools are verbs. Steering is grammar. Skills are recipes." — catchy but feels manufactured
No first-person voice, no anecdotes, no "I discovered this when..."
This section would benefit from some of your voice injected into it — a brief anecdote about discovering one of these concepts, or a "here's where I got confused" moment.


Rule 4's bullet list (except the rat-holing anecdote and the Slop entry). The definitions are clean, parallel, one-sentence-with-a-dash constructions. They're accurate but generic — the kind of list you'd find in any "LLM pitfalls" blog post. The rat-holing sub-bullet with your personal print-statement anecdote is immediately distinguishable as human-written. More entries like that would break the pattern.


The MCP parenthetical at the end of the framework: "think of it as a 'USB standard for AI tools'" is a common AI-generated analogy that appears in dozens of MCP explainers. If you want to keep it, own it with something like "I've seen this compared to USB for AI tools, which is close enough."


Rule 3's guideline labels (Jujitsu, Anthropology, Tactics, Insight, Reboot, Persist) — The naming convention is clearly yours (creative, non-obvious metaphors). But the explanatory text following some of them reverts to AI tone: smooth, parenthetical, slightly over-explaining. Compare "Jujitsu" (which reads like you explaining a concept you've lived) with "Persist" (which reads like a tooltip definition).


### Minor / formatting


"help ensure we are on the same page" — fixed from "insure" in one instance but check if it appears elsewhere.


"For more on context see sections 4 and 5 on the agentic AI framework above." — The framework doesn't use "section 4" and "section 5" labels; it uses "4. Context & Steering" and "5. Skills." This reference is slightly confusing.


The Rule 3 intro paragraph has a missing word: "Prompts and established context together guide the process of work..."


Biggest wins: writing the Part 1 conclusion (connecting case studies to rules), injecting personal voice into the framework section, and addressing the data privacy omission.
