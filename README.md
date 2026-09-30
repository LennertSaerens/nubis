# KBC Nubis

KBC Nubis is a dependency-free proof of concept for the Tectonic Hackathon KBC challenge. It imagines an evolving banking companion that remembers what matters, recognizes meaningful life moments, and starts a useful conversation at the right time.

## Run it

The POC is a static site—no package install, API key, account, or real KBC connection is required.

```bash
python3 -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000). The root `index.html` opens `banking-grows-with-you.html`, exactly as a GitHub Pages deployment would. The three transparent companion assets are committed under `assets/` and are loaded with relative paths, so the 16, 26, and 55 life stages work in a fresh clone.

The prototype stores only fictional demo memories in browser `localStorage` under a namespaced key. Use **Reset demo** to clear them.

## Three-minute demo

1. Start at **16 · First salary**. Notice that the home shows one simple everyday balance and only lightweight tracking/transfer tools. Tap the **Talk with Nubis** microphone to play Theo’s “Make tonight work” conversation about drinks and the ski goal.
2. Select **26 · A home**. The home has evolved to show everyday and investment balances, a budget surface, mortgage-readiness education, and the supplied 26-year-old Nubis portrait. Tap the microphone to play “Prepare before the decision,” where Nubis connects freedom and home costs without telling Theo whether to buy.
3. Select **55 · Retirement**. The home retains the two-balance model and adds a pension overview, education about how pension funds work, and a dedicated wealth overview with an illustrative five-year investment journey—not a forecast or recommendation. Tap the microphone to play the retirement conversation about trips, security, and leaving something meaningful for the children.
4. Open either card’s educational next step or prepare a fictional handoff. The prototype confirms that nothing is booked or shared.

The stage buttons support a clearly labelled **guided preview** for jumping directly to a later scene. Preview memories are explicitly marked as fictional seeded context; the main story should be shown linearly.

The adaptive banking tools also open lightweight fictional panels: a weekly-spend breakdown and transfer review at 16; budget and home-readiness views at 26; and pension overview/fund education at 55. They demonstrate the UI only—no money is moved, no product is recommended, and no appointment is booked.

## What is demonstrated

- **Understand:** controlled fictional signals and the customer’s current answer.
- **Adapt:** stage-specific scenes, supplied transparent Nubis portraits, scripted conversations, remembered values, and banking surfaces: simple money tools at 16, home-readiness education at 26, and a wealth overview plus pension-fund education at 55.
- **Scale:** one controlled conversation shape across first salary, home, and retirement moments.
- **Safety:** no product recommendation, credit decision, transaction, booking, data sharing, or unbounded AI output.

The five intended surfaces are represented by the timeline, adaptive banking home, Nubis conversation player, Life Tree, Conversation Cards, and confirmed KBC handoff. The player is intentionally local and deterministic: it reveals the supplied Theo/Nubis script as paced speech bubbles and needs no network connection.

## Out of scope

This hackathon POC does not use real KBC data, authenticated users, transactions, product applications, mortgage/pension/investment recommendations, real appointment booking, calendar integration, or a backend. Any future LLM integration should return a validated fixed JSON shape and use the existing scripted fallback when validation fails.

Before submission, keep the repository public, run the required Aikido audit, resolve findings, and include the audit screenshots with the short demo video.
