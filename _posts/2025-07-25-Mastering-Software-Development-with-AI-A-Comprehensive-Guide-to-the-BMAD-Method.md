# "Mastering Software Development with AI: A Comprehensive Guide to the BMAD Method"

## Build Software with AI Using the BMAD Method  
A step-by-step guide to using AI agents as your development team inside your IDE.

---

### Prerequisites / Materials

- A GitHub account
- One of the following IDEs:
  - Cursor (*recommended*)
  - Cloud Code
  - Windsurf
- A terminal inside your IDE
- Access to an AI assistant (ChatGPT, Claude, or Gemini)
- Basic familiarity with Agile principles (*optional but helpful*)

---

### Estimated Time & Difficulty

- ⏱ **45–90 min** (initial setup + first story)
- 🧠 **Difficulty:** Medium

---

## Step‑by‑Step Instructions

### 1. Install the BMAD Developer Framework

1. Open the [BMAD GitHub repository](https://github.com/bmadcode/bmad).
2. Copy the `npx` installation command provided there.
3. Open your terminal in your IDE and paste the command.
4. When prompted:
   - Enter the full path to your project directory.
   - Choose: **Install BMAD Agile Core System**.
   - Select **Yes** to sharding the PRD and architecture documentation.
   - Choose your IDE(s): Cursor, Windsurf, or Cloud Code.
   - Select **No** for pre-built web bundles (if following this guide exactly).

*This creates all required files and folders inside your project, keeping it clean and self-contained.*

---

### 2. Prepare the Two Key Documents: PRD & Architecture

1. Navigate to `dist/teams/teamfullstack.txt` in the GitHub repo.
2. Upload this file to your preferred AI assistant (e.g., ChatGPT).
3. Include this instruction:  
   > “Act as per the attached system instructions. Do not break character.”
4. Run the `*brainstorm` command to begin ideating your software idea.
5. Answer the AI’s questions and refine the features.
6. Generate a **feature matrix** and finalize the brainstorming session.
7. Use the `*PM` command → then `*create doc`.
   - Follow all five PRD drafting stages with guided choices.
   - Save the final `prd.md` file.
8. When prompted, switch to **Architect** mode to design your app's architecture.
   - Save the final `architecture.md` file.

*Both documents are essential inputs for the AI team to build your app.*

---

### 3. Place Documentation in the Correct Folder

1. Create a folder inside your project named `docs`.
2. Move `prd.md` and `architecture.md` into this folder.

---

### 4. Initialize the AI Development Team in Your IDE

1. Start a new chat session.
2. Type `PO` to start the **Product Owner** agent.
3. Run the `*shard doc` command and provide paths to both markdown files.

*Sharding breaks each doc into chunks for easier task management in Agile workflow.*

---

### 5. Run the Scrum Master and Generate Epics/Stories

1. Open a new chat, activate the **Scrum Master** agent.
2. Run the `*draft` command.
3. If your PRD has no epics, the agent will detect it and offer to generate them.
4. Choose the **createEpic** option to divide your PRD into major EPICs.
5. The agent will:
   - Create epics (e.g. Epic 1, Epic 2…)
   - Generate user stories inside each (e.g. 1.1, 1.2…)
6. Manually set the status of stories you want to build to `approved`.

---

### 6. Assign Development with the Dev Agent

1. Open a fresh chat and start the **Dev** agent.
2. Choose a story (e.g., 1.1) to begin development.
3. Wait as the agent breaks it into code subtasks and builds component by component.
4. The story status will change to `ready for review`.

---

### 7. Test the Story with the QA Agent

1. Open a new chat and start the **Testing** agent.
2. Run the `*review` command for the completed story.
3. The agent:
   - Scans implementation for completion and bugs.
   - Auto-fixes repetitive code if necessary.
   - Changes the story status to `done`.

---

### 8. Repeat for the Next Story

1. Return to the Scrum Master to find the next `approved` story.
2. Assign it to the Dev agent in a new chat.
3. Continue loop: Develop → Review → Approve → Done.

---

## Pro Tips & Common Pitfalls

- ✅ Always start each agent in a **new chat** to avoid context length issues.
- 🟢 Approved stories only: Dev agents skip anything not explicitly marked `approved`.
- ⚠ Don’t skip epics: The workflow depends on proper PRD decomposition.
- 🛑 Avoid using voice commands in early brainstorming—can introduce bugs.
- ⏱ Initial setup may take time, but pays off in speed and consistency later.
- 🤖 Claude, ChatGPT, or Gemini all work — Gemini is most cost-effective.

---

## You’re Done When…

- Your project folder contains:
  - A `.bmad` core directory
  - A `docs` folder with `prd.md` and `architecture.md`
  - Epics with user stories, marked as `done` after testing
- Your AI team (Product Owner, Scrum Master, Dev, QA) has built and shipped at least one user story
- You can rerun the loop for each remaining story to complete your software incrementally

---
## References:
 - [Agile Coding Is HERE… 90% AI Coding Is Already Done With This](https://www.youtube.com/watch?v=fD8NLPU0WYU&list=PLqSlRNst2NtmOrmU1RyEvJYIyb7eRa22s&index=41&t=304s)