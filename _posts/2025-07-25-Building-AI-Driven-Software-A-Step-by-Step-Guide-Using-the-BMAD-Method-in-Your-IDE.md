## Use the BMAD Method to Build AI-Driven Software in Your IDE

Create full-featured, production-ready software with AI agents using a structured agile workflow directly in your IDE.

---

## Prerequisites

- Basic familiarity with software development concepts (e.g., agile, epics, stories)
- Terminal access
- One of the following IDEs installed:  
  - Cursor  
  - Cloud Code  
  - Windsurf (optional)
- Node.js and `npx` installed
- An OpenAI-compatible AI (e.g., ChatGPT, Claude, Gemini)

---

## Estimated Time & Difficulty

- ⏳ **Time**: 30–60 minutes (initial setup); longer to build full apps  
- 🧠 **Difficulty**: Medium

---

## Step‑by‑Step Instructions

### 1. Install the BMAD Core System

1. Head to the BMAD GitHub repository: [github.com/bmadcode/bmad](https://github.com/bmadcode/bmad)
2. Copy the `npx` install command listed in the README.
3. Open your IDE (Cursor, Cloud Code, or Windsurf) and launch the terminal.
4. Paste the command and press Enter.

   *This sets up BMAD’s core workflow structure inside your project.*

5. When prompted:
   - Enter your full project path.
   - Choose **Install BMAD Agile Core System**.
   - Choose **Yes** to shard both PRD and Architecture files.
   - Select your IDE(s) from the list.
   - Choose **No** when asked about pre-built web bundles.

6. Restart your IDE if needed. You should see BMAD files installed in your project folder.

---

### 2. Generate Your PRD and Architecture Files

1. Download `teamfullstack.txt` from the BMAD repo (`/dist/teams/teamfullstack.txt`).
2. Upload the file to your AI (ChatGPT, Claude, or Gemini).
3. Prompt it using the **brainstorm** command to describe your app idea.

   *E.g., “I want to build a productivity app for iOS.”*

4. Let the AI guide brainstorming; confirm or reject suggestions.
5. When prompted, generate:
   - A **feature matrix** (MVP = Version 1, additional features = Version 2)
   - A **PRD** using the **pm create doc** command
   - An **architecture plan** using the **architect** agent in interactive mode

6. Save both the PRD and architecture file as `prd.md` and `architecture.md`.

---

### 3. Prepare the `docs` Folder

1. In your project directory, create a folder named `docs`.
2. Move `prd.md` and `architecture.md` into this folder.

   *BMAD agents rely on these files to kick off the workflow.*

---

### 4. Initialize Agents One-by-One

⚠️ Start each agent in a new chat session to avoid context confusion.

#### 4.1. Start the Product Owner (PO) Agent

1. In Cursor, type `PO` and select the Product Owner agent.  
   In Cloud Code, use `/PO`.
2. Run the **shard doc** command and provide paths to your PRD and architecture files.

   *This breaks your docs into manageable pieces, preparing them for task creation.*

---

#### 4.2. Start the Scrum Master Agent

1. Load the Scrum Master agent (`scrum.mdc` file).
2. Run the **draft** method.
3. If epics haven’t been created yet, run **create epic** (the agent will prompt you).
4. Confirm epic generation and review them.

   *Each epic contains multiple stories (e.g., 1.1, 1.2) for agile development.*

5. Manually change each story’s status from `draft` to `approved`.

---

#### 4.3. Start the Developer (Dev) Agent

1. In a new chat, open the Dev agent (`dev.mdc`).
2. Select a story to start with (e.g., 1.1).
3. Let the agent write and structure the code based on that story.
4. When the agent finishes, the status updates to `ready for review`.

---

#### 4.4. Start the Testing Agent

1. In a new chat, load the Tester agent (`tester.mdc`).
2. Use the **review** method.
3. Let the agent test the code:
   - It will check for implementation accuracy and make small refactors if needed.
   - If successful, it changes the story status to `done`.

---

### 5. Repeat for Each Story

1. Move to the next story marked as `approved`.
2. Use the Dev agent to build it.
3. Follow with the Testing agent.
4. Continue this loop until all stories in all epics are marked `done`.

---

### 6. Explore the Documentation with AI (Optional)

1. Take the GitHub repo URL and replace `github.com` with `git-ingest.com`  
   *(e.g., `https://git-ingest.com/bmadcode/bmad`)*
2. Open Claude (or equivalent) and paste the Git-Ingest URL.
3. Ask questions directly about the workflow.

   *Perfect for troubleshooting or exploring advanced commands.*

---

## Pro Tips & Common Pitfalls

- Always start agents in new chats — one agent per session to avoid memory conflicts.
- Manually approve stories after generation: change `draft` to `approved`.
- Don't skip brainstorming — it generates better PRDs and reduces confusion later.
- Use Gemini for long, cost-effective brainstorming sessions.
- Restart your IDE after installing for files to register.
- BMAD supports all mainstream IDEs; choose multiple for flexibility.
- Use the file `teamfullstack.txt` exactly as provided — it defines the full AI team structure.

---

## You’re Done When…

✅ All epics are broken into stories  
✅ Every story has been built by the Dev agent and marked `done` by the Tester  
✅ Your PRD and architecture files have been fully implemented in code  
✅ The automated agile workflow mimics a full software development life cycle within your IDE

---

Happy building!
## References:
 - https://www.youtube.com/watch?v=fD8NLPU0WYU&list=PLqSlRNst2NtmOrmU1RyEvJYIyb7eRa22s&index=41&t=304s