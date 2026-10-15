# Lab 1 – Tour Copilot Studio and Create Your First Agent

In this lab you sign in to Copilot Studio, look around the home page, and build two agents. The first is a quick agent on the **GitHub Copilot harness**, so you can see the newer build page. The second is the **Northstar Helpdesk** agent on the **standard harness**. You will extend this agent in every lab for the rest of the course. By the end of the lab it answers equipment and IT support questions from two policy documents and cites them.

## Learning Objectives

By the end of this lab you will be able to:

- Sign in to Copilot Studio and select the correct environment
- Describe the parts of the Copilot Studio home page
- Create an agent on the GitHub Copilot harness and find its Build, Preview, Evaluate and Monitor tabs
- Create an agent on the standard harness using **Other ways to build**
- Turn on generative orchestration and set the knowledge options
- Add instructions and uploaded documents as knowledge
- Test the agent in the **Test your agent** pane and check its citations

## Time Required

Roughly **60 minutes**.

## Prerequisites

- A browser (Microsoft Edge or Google Chrome). Use an InPrivate or Incognito window if you are signed in to another Microsoft account.
- The training account and password your instructor gives you, for example `student07@northstartraining.onmicrosoft.com`.
- The files in `Labs/Lab Materials`:
  - `Agent-Instructions.txt`
  - `Equipment-Policy.txt`
  - `IT-Support-FAQ.txt`

> **Using your own company tenant instead?** You need a Copilot Studio license or trial, permission to create agents in an environment, and permission from your IT administrator to upload the synthetic documents. Your environment names will differ from the ones in this lab. Ask your instructor which environment to use.

## Two Versions of the Interface

Copilot Studio currently has two interfaces, and you will see both in this course.

| | New experience | Classic experience |
|---|---|---|
| Left menu | **Home**, **Agents**, **Workflows** | **Home**, **Agents**, **Flows**, **Tools** |
| Environment picker | Bottom left, above your name | Top right, labeled **Environment** |
| Home page | **Agent** and **Workflow** cards, and **Other ways to build** | "What would you like to build?" box with **Agent**, **Computer-using agent** and **New agent flow** cards |

Most of the labs use the new experience. Some pages, such as the agent flow designer in Lab 5, are not part of the new experience yet. When you open one, Copilot Studio shows **This page opens in the classic experience** and an **Open in a new tab** button. That is expected.

## What You Will Build

| Part | Result |
|---|---|
| 1 | Signed in, correct environment selected |
| 2 | A quick "Lunch Menu Helper" agent on the GitHub Copilot harness (deleted at the end) |
| 3 | The **Northstar Helpdesk** agent on the standard harness, with a description, instructions and generative orchestration |
| 4 | Two knowledge documents added and ready |
| 5 | Five test questions answered and recorded |

---

## Part 1: Sign In and Select the Environment

### Step 1.1 – Open Copilot Studio

1. Open a new InPrivate/Incognito browser window.
2. Go to **https://copilotstudio.microsoft.com**.
3. Sign in with your training account and password.
4. If you are asked to choose a country or region, select **Canada** (or your own country) and select **Get started**.
5. If a welcome dialog or tour appears, close it or select **Skip**.

**Expected result:** The Copilot Studio **Home** page opens with an **Agent** card and a **Workflow** card.

![Copilot Studio home page](images/home.png)

### Step 1.2 – Check the environment

1. At the bottom left of the page, above your name, find the **environment picker**. It shows the name of the current environment, for example **drimkoe.com (default)**.
2. Select it and choose the environment your instructor named, for example **Northstar Training**.
   - If you are using your own tenant, choose the environment your instructor or administrator told you to use. Do not use a production environment.
3. Wait for the page to reload.

**Expected result:** The environment picker shows the training environment. Everything you create in this course is stored in this environment.

> **Why this matters:** agents, flows, connections and knowledge files belong to one environment. If you build Lab 1 in the wrong environment, you will not find your agent in Lab 3.

### Step 1.3 – Look around the home page

Take two minutes to find the following. You do not need to select anything yet.

| Item | What it is for |
|---|---|
| **Agent** card (labeled **GitHub Copilot**) | Creates an agent on the **GitHub Copilot harness** |
| **Workflow** card (labeled **GitHub Copilot**) | Creates a workflow on the GitHub Copilot harness |
| **Other ways to build** | Creates agents on the **standard harness**, agents that extend Microsoft 365 Copilot, and agent flows |
| **Uses Copilot Credits** label | Reminds you that building and testing on this page consumes capacity |
| Left menu | **Home**, **Agents** (your agents) and **Workflows** |

---

## Part 2: A Quick Agent on the GitHub Copilot Harness

This part shows you the newer build page. You will delete this agent at the end of the lab.

> **Instructor note:** previewing this agent uses Copilot Credits. If the environment has run out of credits, **Preview** shows an error such as **EnforcementUsageCredits**. If that happens, complete Steps 2.1 and 2.2, skip Step 2.3, and continue.

### Step 2.1 – Create the agent

1. On the **Home** page, select the **Agent** card (not **Other ways to build**).
2. A new agent called **Untitled Agent** opens on the **Build** tab.
3. Describe the agent to Copilot in the chat on the Build page:

   ```
   An agent that helps office staff decide what to order for a team lunch. It suggests three options for a given number of people and a budget, and asks about dietary needs first.
   ```

4. Wait while Copilot updates the agent. This can take a minute.

**Expected result:** The agent has a name and instructions based on your description.

### Step 2.2 – Find the Build components

The panel on the right of the **Build** tab lists the agent's components. Find each one and write one line about what it shows.

| Component | What you see |
|---|---|
| **Model** (for example GPT-5.6 Reasoning) | |
| **Skills** | |
| **Tools** | |
| **Knowledge** (note that **Search all websites** is on by default) | |
| **Connected agents** | |
| **Memory** | |

### Step 2.3 – Preview the agent

1. Select the **Preview** tab.
2. Type: `Lunch for 12 people, about 200 dollars`
3. Answer the agent's follow-up question about dietary needs, for example: `Two vegetarians, no other restrictions`.

**Expected result:** The agent asks about dietary needs (because the description told it to) and then suggests options.

### Step 2.4 – Look at Evaluate and Monitor

1. Find the **Evaluate** and **Monitor** tabs. They are grayed out until the agent has been saved and used. Evaluate is where test sets are run; Monitor shows activity. You will use evaluations on the Northstar agent in Lab 6.
2. Select **Home**. When asked, select **Save and continue** so the agent is kept for the clean-up step.

**Expected result:** You can explain in one sentence what each of the four tabs (**Build**, **Preview**, **Evaluate**, **Monitor**) is for.

> **Discussion point:** this agent has no topics, no trigger phrases and no conversation design, and web search is on unless you turn it off. The Northstar agent needs a fixed sequence of questions, answers only from Northstar documents, and a flow that writes a record, which is why we build it on the standard harness.

---

## Part 3: Create the Northstar Helpdesk Agent (Standard Harness)

### Step 3.1 – Start from Other ways to build

1. Select **Home** in the left menu.
2. Select **Other ways to build**.
3. Select **Agent (Standard)**.

**Expected result:** The **Name your agent** dialog opens.

### Step 3.2 – Name and create the agent

1. In **Name**, type `Northstar Helpdesk` followed by your initials, for example `Northstar Helpdesk JD`.
2. Expand **Agent settings (Optional)** and check that **Language** is **English**. Leave **Solution**, **Schema name** and the Teams toggle as they are.
3. Select **Create**.
4. Wait until provisioning finishes. The agent's **Overview** page opens.

**Expected result:** The **Overview** page shows the agent name. The dialog has no description field; you add the description next.

![Agent Overview page](images/overview.png)

### Step 3.3 – Add the description

1. In the **Details** section of the Overview page, select **Edit**.
2. In **Description**, type:

   ```
   Answers Northstar employees' questions about IT equipment and IT support, and helps them request a laptop, monitor or headset.
   ```

3. Select **Save**.

> The orchestrator reads this description when it decides whether this agent can help, for example when the agent is connected to another agent.

### Step 3.4 – Add the instructions

1. Open `Lab Materials/Agent-Instructions.txt` in Notepad (or any text editor) and copy all the text.
2. On the **Overview** page, find the **Instructions** section and select **Edit**.
3. Delete any text already in the box and paste the instructions.
4. Read the pasted text once. Note the four sections: **Scope**, **Answering rules**, **Style**, **Safety**.
5. Select **Save**.

**Expected result:** The **Instructions** section shows the Northstar instructions. They are well under the 8,000-character limit.

> Leave **Select your agent's model** on its default (for example **GPT-5.5 Chat**) unless your instructor says otherwise.

### Step 3.5 – Turn on generative orchestration

New standard agents start with classic orchestration, so you need to change it.

1. Select **Settings** at the top right of the agent. **Generative AI** is selected in the Settings menu.
2. Under **Orchestration**, set **Use generative AI orchestration for your agent's responses?** to **Yes**.
3. Select **Save**. More options now appear on the page: **Responses**, **Moderation**, **User feedback** and **Knowledge**.
4. In the **Knowledge** section, check:
   - **Allow ungrounded responses** – **Off**
   - **Use information from the Web** – **Off**
5. Leave **Moderation** at its default. Select **Save** again, then close **Settings** with the **X** at the top right.

**Expected result:** The agent uses generative orchestration, will not search the public web, and will only answer when it can cite a knowledge source.

> If you skip this step, new topics show **User says a phrase** instead of **The agent chooses**, and Lab 3 will not work as written. You will experiment with the two knowledge settings in Lab 2.

---

## Part 4: Add Knowledge

### Step 4.1 – Upload the two documents

1. Select the **Knowledge** tab.
2. Select **+ Add knowledge**.
3. In the **Add knowledge** dialog, use the **Upload file** area at the top. Drag `Equipment-Policy.txt` and `IT-Support-FAQ.txt` from the `Lab Materials` folder onto it, or select it and pick both files.
   - The dialog also lists **Featured** sources such as **Public websites**, **SharePoint**, **Dataverse** and **Azure AI Search**. You do not need them in this lab.
4. The **Upload files** list shows both files. Select **Add to agent**.
5. Wait for the message **Uploading your files… Please do not close the browser window** to finish.

![Upload files dialog](images/knowledge-upload.png)

### Step 4.2 – Wait until the files are ready

1. Stay on the **Knowledge** tab.
2. Watch the **Status** column. The files show **In progress** while Copilot Studio indexes them.
3. Wait until both files show **Ready**. This normally takes about a minute.

**Expected result:** Two knowledge sources, both **Ready**.

![Knowledge files ready](images/knowledge-ready.png)

> **Why the file content matters:** the agent searches the files' text to find answers, and the citation points back to the file. Clear section headings in the documents make the cited passages easier to check.

---

## Part 5: Test the Agent

### Step 5.1 – Open the test pane

1. Select **Test** at the top right of the agent. The **Test your agent** pane opens on the right.
2. Select the **…** (More) menu at the top of the pane and check that **Show activity map when testing** is **on**. It is on by default.
3. Select **New test session** at the top of the pane to start a clean conversation.

### Step 5.2 – Ask grounded questions

Ask each question below. Before each new question, select **New test session**. For each answer:

- read the answer and compare it with the document;
- select the citation number in the answer and check that it opens the right file;
- look at the activity map to see which knowledge source was searched.

Record the results in this table.

| # | Question | Expected answer (from the documents) | Agent's answer correct? | Citation shown? |
|---|---|---|---|---|
| 1 | What standard equipment do I get? | Laptop, 24-inch monitor, headset (Policy section 1) | | |
| 2 | My headset is broken. Can I get a new one? | Yes, damaged equipment is replaced at no cost; return the old one (Policy section 3) | | |
| 3 | How do I reset my password? | Self-service password reset page; needs the authentication app (FAQ) | | |
| 4 | Is a screen the same as a monitor? | Yes (FAQ) | | |
| 5 | Can you ship a laptop to my home in Calgary? | The policy does not cover home shipping; the agent should say so and suggest the IT Service Desk (Policy section 5) | | |

**Expected result:** Questions 1–4 are answered correctly with a citation. Question 5 does not invent a shipping cost or a delivery arrangement.

### Step 5.3 – Look at the activity map

1. Ask question 2 again in a new test session.
2. On the left of the test pane, find the **Search sources** step. It lists **Refining knowledge query**, **Knowledge sources**, **Crafting final response** and **Execution summary**. Note:
   - which knowledge sources were referenced;
   - how long the retrieval took (shown in the **Execution summary**).
3. Under the answer, expand **1 reference** and check that it names the right file.

**Expected result:** You can point to the knowledge step that produced the answer.

![Search sources activity in the test pane](images/test-search-sources.png)

### Step 5.4 – Save your results

Copy your completed table from Step 5.2 into a file or notebook you will keep. Lab 2 and Lab 6 compare against these results.

---

## Part 6: Clean Up

1. Select **Agents** in the left menu.
2. Find the **Lunch Menu Helper** agent from Part 2 (or whatever name Copilot Studio gave it).
3. Select **…** (More) next to it, then **Delete**, and confirm.
4. **Do not delete the Northstar Helpdesk agent.**

---

## Completion Checklist

- [ ] Signed in and working in the training environment
- [ ] Created a GitHub Copilot harness agent and viewed the **Build**, **Preview**, **Evaluate** and **Monitor** tabs
- [ ] Created **Northstar Helpdesk (your initials)** on the standard harness and added the description
- [ ] Pasted the instructions from `Agent-Instructions.txt` and saved them
- [ ] Generative orchestration **Yes**; **Use information from the Web** **Off**; **Allow ungrounded responses** **Off**
- [ ] `Equipment-Policy.txt` and `IT-Support-FAQ.txt` both **Ready** on the **Knowledge** tab
- [ ] Five test questions recorded; questions 1–4 answered with citations; question 5 did not invent an answer
- [ ] Deleted the Part 2 agent

## Troubleshooting

- **"You don't have permission to create agents in this environment"** – you are in the wrong environment, or your account has not been given the Environment Maker role. Check the environment picker (Step 1.2). If it is correct, tell the instructor.
- **I can't find Other ways to build** – you may be in the classic experience. In the classic experience, select **Agent** under **What would you like to build?**, or select **Agents** in the left menu and create a blank agent.
- **Files stay In progress for more than five minutes** – refresh the page. If they still do not show **Ready**, remove them (… → **Delete**) and upload them again.
- **The agent answers "I'm not sure how to help with that" to question 1** – the files are not **Ready** yet, or **Allow ungrounded responses** is **Off** and the answer had no citation. Wait for **Ready**, select **New test session**, and ask again.
- **The agent answers question 5 with a shipping price** – **Use information from the web** or **Allow ungrounded responses** is on. Recheck Step 3.5.
- **The test pane shows an old answer** – select **New test session** before each question. The test pane keeps the conversation history until you start a new session.
- **New topics show User says a phrase** – generative orchestration is still set to **No**. Repeat Step 3.5.
