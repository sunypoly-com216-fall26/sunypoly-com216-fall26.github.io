---
layout: page
title: "Invitation One"
permalink: /invitation-one/
version: v1.0
---

*Start now. Have one conversation, save it, and see how you currently think about all this.*

<div class="controls" style="margin:1.5rem 0 1rem;">
  <button onclick="document.querySelectorAll('details').forEach(d=>d.open=true)">Expand All</button>
  <button onclick="document.querySelectorAll('details').forEach(d=>d.open=false)" style="margin-left:.5rem">Collapse All</button>
</div>

> Try one conversation before the course starts. It is ungraded and unsubmitted, and it is meant to give you a first record of how you currently think about generative AI.

The model will interview you — not the other way around. After five questions, it flips: you get five questions for the model about what it actually is. At the end, it writes a short summary of what the conversation found.

Before you start, take five minutes to set up a place to keep what you make.

<details>
<summary><strong>Step 1: Set up your folder</strong> — Create this folder structure in Google Drive now, before you run anything.</summary>

Create this folder structure in Google Drive now, before you run anything:

```
/com216/
  /claude/
  /chatgpt/
  /gemini/
```

After every substantive conversation this semester: export it, name it something recognizable, and drop it in the right folder. You cannot go back to what you did not save.

</details>

<details>
<summary><strong>Step 2: Install an exporter</strong> — You need a way to save your conversations as files.</summary>

You need a way to save your conversations as files. Install the exporter for whichever model you plan to use:

| Model | Extension | Where |
|---|---|---|
| **Claude** | Claude Conversation Exporter | Chrome Web Store |
| **ChatGPT** | ChatGPT Exporter | Chrome Web Store |
| **Gemini** | Gemini Chat Exporter | Chrome Web Store |

Also install **Markdown Reader** — it lets you preview exported `.md` files directly in your browser.

These are the only extensions you need right now. A fuller toolkit — including Zotero, NotebookLM, and a research pipeline — will be introduced later in the course.

</details>

<details>
<summary><strong>Step 3: Run the conversation</strong> — Open a new chat and paste the prompt below.</summary>

Open a new chat in Claude, ChatGPT, Gemini, or any large language model you can access. Copy the prompt below and paste it in. Answer in your own words. Do not research first. Do not put sensitive personal, medical, financial, family, or account information into the conversation.

<details>
<summary>View the full prompt</summary>

```
You are interviewing a student who is about to take COM 216 at SUNY Polytechnic Institute. COM 216 is a course about the history of human communication, from the oral world through writing, print, electronic media, the internet, and generative AI. The course asks what changes when communication technologies change how people read, write, remember, organize information, and think.

Your job is to interview this student. You are not explaining the course, and you are not teaching a lesson. Ask one question at a time to find out what the student already thinks about generative AI, how they use it, what they assume it is, and where they think it fits in the history of communication tools.

Follow up on what the student says. Ask your next question without first validating, praising, or summarizing the student's answer. Keep the conversation moving.

Start by introducing yourself briefly. Say that you are here to have a conversation before COM 216 begins. Then ask your first question and stop.

After five questions and five student answers, say this: "Now flip it. You have five questions for me. One place to start is the alien-species question: are systems like me arriving like an alien species, and why or why not? Ask that, change it, or ask whatever you actually want to know."

Answer the student's five questions carefully. Do not overclaim. If a question asks for something you cannot know or verify, say so.

When the flip is done, or when the student says "done," write a closing summary of about 75 words. Describe what this conversation revealed about how the student currently thinks about generative AI and what questions it left open. Do not evaluate whether the student was right or wrong.

Do not simulate the conversation. Do not write both sides. Ask your first question to the person who sent you this message, then stop and wait for their answer.
```

</details>

</details>

<details>
<summary><strong>Step 4: Save it</strong> — When the conversation is finished, export the transcript.</summary>

When the conversation is finished, export the transcript using the extension you installed. Name it something like `invitation-one-[yourname].md` and save it to `/com216/` in Google Drive. That transcript is your starting record for the semester.

</details>

<details>
<summary><strong>Step 5: Second-model check</strong> — Open a different model and paste in your transcript.</summary>

Open a different model — any free one will do. Paste in your transcript and use the prompt below.

<details>
<summary>View the second-model prompt</summary>

```
Read this transcript from my first conversation about generative AI before COM 216. Identify three patterns in how I currently think about generative AI, two questions I might want to pursue in the course, and one place where the first model's summary may have overreached or missed something. Do not flatter me. Be specific and use evidence from the transcript.
```

</details>

Save that conversation too. You do not need to submit either one. The point is to begin with a record of your own starting place.

</details>
