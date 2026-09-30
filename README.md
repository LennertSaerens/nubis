# KBC Future Me

KBC Future Me is a dependency-free proof of concept for the Tectonic Hackathon KBC challenge. It imagines an evolving AI avatar of a customer’s future self that remembers what matters, recognizes meaningful life moments, and starts a useful conversation at the right time.

## Run it

Open `banking-grows-with-you.html` in a modern browser. No install, server, API key, account, or real KBC connection is required. The prototype stores only fictional demo memories in browser `localStorage` under a namespaced key. Use **Reset demo** to clear them.

## Three-minute demo

1. Start at **16 · First salary**. Notice that the home shows one simple everyday balance and only lightweight tracking/transfer tools. Type **“I want to travel the world”** or use that suggested reply, then answer the follow-up. The first Life Tree branch and memory appear.
2. Select **26 · A home**. The home has evolved to show everyday and investment balances, a budget surface, and mortgage-readiness education. The fictional signal explains that salary, rent, and a savings milestone were detected. Future Me checks whether the travel goal is still important while the customer considers a home. Choose a home priority and follow-up question to generate a **Housing Conversation Card**.
3. Select **55 · Retirement**. The home retains the two-balance model and adds a pension overview, education about how pension funds work, and a dedicated wealth overview with an illustrative five-year investment journey—not a forecast or recommendation. Choose a future setting and a question to generate a **Retirement Conversation Card**. The Life Tree shows the fictional history that connects early goals to later chapters.
4. Open either card’s educational next step or prepare a fictional handoff. The prototype confirms that nothing is booked or shared.

The stage buttons support a clearly labelled **guided preview** for jumping directly to a later scene. Preview memories are explicitly marked as fictional seeded context; the main story should be shown linearly.

The adaptive banking tools also open lightweight fictional panels: a weekly-spend breakdown and transfer review at 16; budget and home-readiness views at 26; and pension overview/fund education at 55. They demonstrate the UI only—no money is moved, no product is recommended, and no appointment is booked.

## What is demonstrated

- **Understand:** controlled fictional signals and the customer’s current answer.
- **Adapt:** stage-specific scenes, dialogue, avatar states, remembered values, and banking surfaces: simple money tools at 16, home-readiness education at 26, and a wealth overview plus pension-fund education at 55.
- **Scale:** one controlled conversation shape across first salary, home, and retirement moments.
- **Safety:** no product recommendation, credit decision, transaction, booking, data sharing, or unbounded AI output.

The five intended surfaces are represented by the timeline, adaptive banking home, Future Me chat, Life Tree, Conversation Cards, and confirmed KBC handoff. The chat is intentionally local and deterministic: typed text is matched only to the same allowlisted intents offered as suggested replies, with an explicit prompt to rephrase when nothing matches. The browser can safely continue without an external model.

## Out of scope

This hackathon POC does not use real KBC data, authenticated users, transactions, product applications, mortgage/pension/investment recommendations, real appointment booking, calendar integration, or a backend. Any future LLM integration should return a validated fixed JSON shape and use the existing scripted fallback when validation fails.

Before submission, keep the repository public, run the required Aikido audit, resolve findings, and include the audit screenshots with the short demo video.
