# 01 — Your First AI Agent in n8n

📺 **Video:** [Build Your First AI Agent with n8n (No Code)](https://www.youtube.com/@AutomateWithHassan)

A beginner-friendly AI agent you can chat with. It has:

- 🧠 **Brain:** OpenAI Chat Model (`gpt-4o-mini`)
- 💾 **Memory:** Simple Memory (last 10 messages)
- 🔧 **Tools:** Calculator + Wikipedia. The agent decides on its own when to use them.

```
When chat message received ──► AI Agent
                                 ├── Chat Model: OpenAI (gpt-4o-mini)
                                 ├── Memory: Simple Memory
                                 └── Tools: Calculator, Wikipedia
```

## Setup (2 minutes)

1. Import `workflow.json` into n8n (⋯ menu → **Import from File**).
2. Open the **OpenAI Chat Model** node → **Credential** → **Create new** → paste your OpenAI API key (from platform.openai.com).
3. Save the workflow and click **Open chat** at the bottom of the canvas.

## Try these questions

1. `Who founded n8n, and in what year?` → uses **Wikipedia**
2. `If I invest $500 a month for 3 years, how much is that in total?` → uses **Calculator** ($18,000)
3. `What was my first question?` → uses **Memory**

## System message used

```
You are a friendly assistant for beginners.
Use the Calculator tool for any math.
Use the Wikipedia tool to look up facts. Never guess.
Keep answers short and clear.
```

## Troubleshooting

- **"Credentials not found":** select your OpenAI credential in the OpenAI Chat Model node.
- **"Insufficient quota" / 429 error:** add a small amount of credit to your OpenAI account.
- **Import fails or a node shows as unknown:** update n8n to the latest version.
