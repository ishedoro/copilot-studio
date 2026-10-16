# Microsoft Copilot Studio Labs

Hands-on lab exercises for the Microsoft Copilot Studio: Low-Code Copilot Development course (IN1945). Every lab has its own folder with a `README.md` that takes you through the lab one numbered step at a time. Each step ends with the result you should see. Every README also has a completion checklist and a troubleshooting section.

All six labs build the same agent, **Northstar Helpdesk**. Keep your agent and your test records from one lab to the next.

## Lab Index

| Lab | Day | Topic | What you build | Approx. time |
|-----|-----|-------|----------------|--------------|
| [Lab 1 – Tour Copilot Studio and Create Your First Agent](Lab%201%20-%20Tour%20Copilot%20Studio%20and%20Create%20Your%20First%20Agent/README.md) | 1 | Copilot Studio interface, harnesses, knowledge | A quick agent on the GitHub Copilot harness, then the Northstar Helpdesk agent with two policy documents as knowledge | 60 min |
| [Lab 2 – Grounding, Knowledge and Hallucination Control](Lab%202%20-%20Grounding%20and%20Hallucination%20Control/README.md) | 1 | Grounding, hallucinations, prompt injection | A test record comparing three knowledge settings, four adversarial tests and one instruction repair | 60 min |
| [Lab 3 – Build the Equipment Request Conversation](Lab%203%20-%20Build%20the%20Equipment%20Request%20Conversation/README.md) | 2 | Topics and nodes, testing, publishing | The Equipment request topic, published to Teams | 75 min |
| [Lab 4 – Variables, Entities and Authentication](Lab%204%20-%20Variables,%20Entities%20and%20Authentication/README.md) | 2 | Variables, entities, Power Fx, user context | An equipment entity with synonyms, a global office variable, and a greeting by name | 75 min |
| [Lab 5 – Extend the Agent with an Automated Workflow](Lab%205%20-%20Extend%20the%20Agent%20with%20an%20Automated%20Workflow/README.md) | 3 | Agent flows, connectors | An agent flow that creates a SharePoint item, emails the requester and returns the request ID | 90 min |
| [Lab 6 – Analyze, Evaluate and Improve the Agent](Lab%206%20-%20Analyze,%20Evaluate%20and%20Improve%20the%20Agent/README.md) | 3 | Analytics, transcripts, evaluations | An analytics review, an evaluation test set, one repair and a comparison run | 75 min |

## Lab Materials

`Lab Materials/` contains every file the labs use. All data is synthetic, and Northstar is a fictional company.

| File | Used in |
|------|---------|
| `Agent-Instructions.txt` | Lab 1 – instructions pasted into the agent |
| `Equipment-Policy.txt` | Lab 1 onwards – knowledge source |
| `IT-Support-FAQ.txt` | Lab 1 onwards – knowledge source |
| `Lab-2-Test-Record.md` | Lab 2 – test record (also reused in Lab 6) |
| `List-Schema.md` | Lab 5 – the columns of your own EquipmentRequests list (Part 0) |
| `Sample-Sessions.csv` | Lab 6 – 20 sample pilot sessions for the analytics calculations |
| `Test-Set.csv` | Lab 6 – 20 evaluation questions with expected responses |

## Prerequisites

- A browser (Microsoft Edge or Google Chrome)
- A training account in the course's Copilot Studio tenant, supplied by the instructor. You can use your own company tenant instead if you have a Copilot Studio license or trial and a non-production environment.
- No programming experience is needed.

## Getting Help

Start with the **Troubleshooting** section at the end of each lab README. Copilot Studio changes often, so a button may have a slightly different name in your tenant. The steps name the page and the setting so you can find it. If you are still stuck, ask the instructor.
