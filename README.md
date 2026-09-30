# Nubis

> **The bank that is on your side—because it is you.**

Nubis is an AI version of the customer's future self: a companion that grows with them, remembers what matters, and helps them prepare for financial choices. Instead of meeting customers only when they already need a product, Nubis starts a useful conversation while they are deciding what kind of future they want to build.

| Life stage | Customer question | Nubis role |
|---|---|---|
| **16** | “Can I spend EUR30 tonight and still go skiing?” | Makes a small trade-off understandable and suggests a realistic recovery plan. |
| **26** | “Should I make an offer on this apartment?” | Recalls the customer's priorities and prepares a better first-home conversation. |
| **55** | “Can I retire at 67 and leave something for my children?” | Helps balance retirement freedom, family legacy, and the need for professional advice. |

Nubis is not a product-selling chatbot. It is a customer-controlled financial companion that helps people see trade-offs, prepare for what is ahead, and connect with a KBC professional when tailored advice is needed.

## Why Nubis?

People trust banks with their money, but not always with their interests. In Test-Aankoop's 2025 bank-satisfaction survey, 21% of respondents reported that their savings earned less than expected, while 12% objected to new customers receiving better rates than loyal ones.

Many customers remain with the same bank for decades. As switching becomes easier, inertia is not a loyalty strategy. Nubis creates a relationship worth keeping by supporting people during meaningful life moments, using priorities they have explicitly chosen to share.

```text
Life moment + customer-approved memory
                 |
                 v
        A useful Nubis conversation
                 |
                 v
  Clearer choice, plan, or expert conversation
```

## Built on future-self research

Nubis uses a behavioural insight: people often experience their future self as distant, almost like another person. Strengthening that connection can support longer-term decisions, including saving behaviour.

- Research by Hal Hershfield and colleagues examined how future-self continuity relates to saving; later work found that age-progressed future-self experiences can increase saving behaviour.
- MIT Media Lab's **Future You** project found in a preregistered study that interacting with a personalised AI-generated future self increased reported future-self continuity and improved wellbeing measures.

Nubis applies this idea to everyday banking: make the future feel personal enough to care about, without making the experience cold, preachy, or sales-driven.

## What the prototype shows

This repository contains a browser-based hackathon proof of concept. Its core claim is simple:

> The same bank should not talk to a customer in the same way at 16, 26, and 55.

### The personalisation thread

Nubis does not “know everything.” It only remembers customer-approved goals and preferences.

```text
16 -> “I want to go skiing with my friends.”
26 -> “I want my own place, but I do not want to lose my freedom.”
55 -> “I want to enjoy retirement and still help my children.”
```

Across decades, freedom evolves:

- **At 16:** joining friends without giving up on a goal.
- **At 26:** owning a home without losing room for everyday life.
- **At 55:** staying independent while creating options for family.

That is the Nubis difference: it remembers the customer's values, not just their transactions.

## Features

### Included in this prototype

- Responsive, browser-based banking-style interface.
- Nubis companion portraits and life-stage storytelling.
- Curated microphone-driven conversations for the 16, 26, and 55 scenarios.
- Synthetic customer profile, signals, goals, and financial information.
- “Why this moment?” explainability layer.
- Illustrative investment-history visualisation for the later-life scenario.
- Clear responsible-advice boundaries.

### Future product direction

| Future feature | Customer value |
|---|---|
| Voice AI agent | Customers can talk naturally to Nubis instead of typing through every life conversation. |
| Money Calendar | Predictable annual costs—tax, insurance, holidays, and renewals—become visible before they create stress. |
| Conversation-to-appointment | Nubis creates a customer-editable summary and helps book time with a KBC professional. |
| Forecasting | Customers can explore transparent future scenarios and uncertainty ranges, not just today's balance. |
| Personal avatar and voice | With explicit consent, Nubis can look and sound more like the customer's future self. |

## Quick start

The prototype is self-contained. It has no backend, package installation, API keys, or KBC account connection.

### Option 1: Open directly

```bash
git clone https://github.com/LennertSaerens/nubis.git
cd nubis
open index.html
```

On Windows:

```bash
start index.html
```

### Option 2: Run a local server

Use this option if your browser restricts local browser features:

```bash
python3 -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000). The root entry point opens the main prototype at `banking-grows-with-you.html`.

## How to use the demo

1. Open the landing experience and introduce Nubis as a future-self companion.
2. Read the **Why this moment?** card, which explains why Nubis is surfacing a conversation.
3. Explore the age-16 moment: a night out, a ski goal, and a manageable recovery plan.
4. Move to age 26: a first-home conversation driven by the customer's stated priority of freedom.
5. Move to age 55: an illustrative retirement journey and the balance between future comfort and family support.
6. End with the trust boundary: Nubis helps customers reflect and prepare; qualified KBC professionals give tailored advice.

### Suggested presentation line

> “At 16, Nubis helps you make tonight work. At 26, it helps you prepare before a major decision. At 55, it helps you make room for both your future and your family's. The person changes, so the conversation changes—but the relationship remains.”

### Example conversation

**Theo:** Nubis, I feel like going for drinks tonight. Is that okay for my ski trip?

**Nubis:** Of course. You are still aiming for EUR650 by February, and a night out does not cancel that.

**Nubis:** If you spend around EUR30 tonight, we can get back on track by putting EUR6 less toward food for the next five days. Or we can set a EUR15 budget tonight and leave the ski plan exactly as it is.

**Theo:** Let’s do the EUR30. I can skip take-away food this week.

**Nubis:** Done. Tonight is covered, and your ski goal stays alive. I’ll check in next week—not every day.

## Trust and safety

Nubis is designed for financial literacy, reflection, preparation, and a safe handoff to human expertise.

### Nubis can

- Help customers articulate goals and priorities.
- Explain simple trade-offs in plain language.
- Create goals, checklists, and customer-editable conversation summaries.
- Explain why it surfaced a moment.
- Help prepare a conversation with a KBC professional.

### Nubis cannot

- Approve, reject, or score credit.
- Give a personalised investment or insurance recommendation.
- Promise a return, retirement outcome, or affordability result.
- Execute a payment or transfer through conversation.
- Share customer context without review and approval.
- Infer sensitive life events or impose a life path.

### Demo boundaries

- This is a hackathon prototype.
- All customer personas, balances, transactions, goals, and investment figures are synthetic.
- Investment information is illustrative history only; it is not a forecast, recommendation, or guarantee.
- No KBC system, account, payment flow, or appointment system is connected.
- No personal data is collected, booked, transferred, or shared.
- Dialogue is curated to demonstrate the product's personalisation model safely and consistently.

## Project structure

```text
.
├── README.md
├── index.html                      # Static root entry point
├── banking-grows-with-you.html     # Main Nubis prototype
└── assets/
    ├── nubis-16.png                # Transparent age-16 companion
    ├── nubis-26.png                # Transparent age-26 companion
    └── nubis-55.png                # Transparent age-55 companion
```

## Contributing

Nubis was created as a hackathon prototype. Contributions are welcome, especially around accessible design, responsible AI, financial literacy, and privacy-first interaction patterns.

Please keep these principles intact:

- Use fictional or approved data only.
- Preserve consent, explainability, and customer control.
- Never introduce unguarded financial recommendations or autonomous transactions.
- Keep Nubis warm, concise, practical, and non-judgmental.

## License

This project is available under the MIT License.

```text
MIT License © 2026 KBC Nubis Hackathon Team
```

## Contact

Built by the KBC Nubis Hackathon Team.

> Nubis does not decide a customer's future. It helps them see it, name what matters, and take the next step with confidence.
