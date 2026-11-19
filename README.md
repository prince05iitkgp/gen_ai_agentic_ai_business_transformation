# GenAI and Agentic AI for Business Transformation

A collection of 10 Python/Jupyter notebooks demonstrating prompting, retrieval-augmented generation (RAG), and multi-agent business workflows. The notebooks target Google Colab and include saved execution outputs. This is a collection of learning prototypes, rather than a deployed application.

## Notebook guide

| Notebook | Purpose |
| --- | --- |
| Chain of Thought Prompting (1) | Compare basic and structured reasoning prompts for an AI investment example. |
| Directional Stimulus Prompting (1) | Guide summarization using keywords and prompt examples. |
| REACT agent | Combine an OpenAI model with web search and an ROI calculator. |
| Traditional_RAG_System (1) | Load a PDF, split text, embed into Chroma, retrieve context, and answer questions with LangChain. |
| Agentic Rag | Coordinate routing, retrieval, relevance grading, grounding checks, and answer generation with CrewAI. |
| Automatic Email_generator | Research and draft email with CrewAI; provide a Gradio interface and Gmail sending through yagmail. |
| Automatic Balancesheet Analysis | Use five agents for planning, validation, liquidity, solvency, and financial narration. |
| Financial_Analysis Demo 4 (1) | Coordinate financial analysis, trading strategy, execution planning, and risk assessment. |
| Event_Planning_Automation (1) | Coordinate venue research, logistics, and marketing. |
| LangFuse_Event_Planning_Automation | Add Langfuse/OpenLIT observability to event planning. |

All notebook filenames retain their original spelling and spacing.

## Running the examples

1. Open a notebook in Google Colab and inspect its installation and execution cells.
2. Install the dependencies specified in that notebook. Libraries used across the collection include CrewAI, crewai-tools, OpenAI, LangChain, Chroma, pandas, Pydantic, Gradio, yagmail, DuckDuckGo search, Langfuse, and OpenLIT.
3. Add the required secrets through Colab Secrets and grant notebook access. Depending on the notebook, these include `OPENAI_API_KEY`, `SERPER_API_KEY`, `LANGSMITH_API_KEY`, `LANGFUSE_SECRET_KEY`, `LANGFUSE_PUBLIC_KEY`, and `GMAIL_APP_PASSWORD`.
4. Supply required inputs: the RAG examples reference `/content/attention-is-all-you-need-Paper.pdf`; balance-sheet analysis expects `ind_as_infra_style_dummy_balance_sheet.csv`. These files are not included.
5. Review example parameters and the email sender configuration before executing cells. The email notebook can send real email when its Send button is used.

There is no shared dependency lockfile or automated test suite. Notebook package installations are mostly unpinned; compatibility needs to be checked in the selected runtime.

## Inspection findings and limitations

- The agentic RAG helper references `setup_tools`, `create_agents`, and `create_tasks`, which are not defined in the notebook. Its PDF downloader also uses a different filename from the PDF tool configuration. A separately constructed crew is present.
- Several workflows depend on Colab-only imports, external APIs, local uploads, and human input.
- The email sender is hardcoded in the original notebook; configure your own sender and credentials before use.
- The ReAct loop has no explicit iteration limit and relies on parsing model-generated text.
- Existing outputs are historical examples, not evidence of a successful run with current dependencies. Agent descriptions and generated reports do not establish real venue bookings, marketing execution, or trades.
- Inspection checked notebook JSON, source cells, metadata, saved outputs, and Git history. No paid API calls, email sends, or end-to-end notebook runs were performed.
- A scan for common OpenAI, Google, and GitHub token patterns found no matches. This is a limited pattern scan, not a guarantee that every possible secret is absent.

## Ownership, attribution, and names

The destination repository is under the GitHub account `prince05iitkgp`. Repository hosting and Git commit authorship do not establish original notebook authorship or copyright ownership.

At inspection, the local history contained one commit, `309a81d` ("Add GenAI and Agentic AI notebooks"), authored by **Copilot** using a GitHub noreply address. The original files contain no explicit project-author declaration, project README, or project-level license. Colab authorship tags are opaque identifiers, not verified personal names. Original authorship and reuse permissions remain unverified; no new license is asserted here.

Names and contact references found in the material include:

- `anushreeiimlucknow@gmail.com`: the email notebook's configured sender. The address suggests the name Anushree but does not establish a verified identity or project authorship.
- **Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Łukasz Kaiser, and Illia Polosukhin**: credited authors of *Attention Is All You Need*, appearing in retrieved PDF text and metadata. These are paper authors, not established authors of this repository.
- **Lee Wan-koo, Park Geun-hye, and Sung Woan-jong**: people mentioned in an example news article used for prompting; not project contributors.
- `Somugowda87478@gmail.com` and `adamsbangalore@gmail.com`: contacts appearing in saved event-planning search/output content; not established project contributors.

Other names in outputs include organizations, vendors, venues, software providers, and agent role labels. These references are example content and do not establish ownership or endorsement.
