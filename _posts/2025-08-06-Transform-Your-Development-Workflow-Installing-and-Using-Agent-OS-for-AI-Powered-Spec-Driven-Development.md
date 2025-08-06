# Transform Your Development Workflow: Installing and Using Agent OS for AI-Powered Spec-Driven Development

```markdown
## Install and Use Agent OS for AI-Powered Spec-Driven Development  
Transform your AI coding agent into a reliable teammate by installing Agent OS and adopting a spec-first workflow.

---

## Prerequisites / Materials  
- A working knowledge of basic software development  
- Familiarity with terminal commands  
- An AI coding tool such as **Claude (Cloud Code)** or **Cursor**  
- Git installed and configured  
- macOS or Linux (default instructions shown for macOS)  
- Optional: Knowledge of **Ruby on Rails** if using the sample project

---

## Estimated Time & Difficulty  
- ⏱ **30–60 minutes** for initial setup  
- 🔧 **Difficulty**: *Medium*

---

## Step-by-Step Instructions  

### 1. Install the Base Agent OS System  
1. Navigate to your home directory in the terminal.  
2. Run the installer script from [buildermethods.com/agentos](https://buildermethods.com/agentos) or directly:  
   ```bash
   curl -s https://buildermethods.com/install-agentos.sh | bash
   ```  
3. Confirm that a new `agentos` folder appears in your home directory.

*This establishes a centralized system storing your coding standards and instructions.*

---

### 2. Customize Your Coding Standards  
1. Open the newly created `~/agentos/standards` folder.  
2. Edit the following files to reflect your preferences:  
   - `techstack.md`: Define common tech stack (language, framework, deployments, etc.)  
   - `codestyle.md`: Outline naming conventions, indentation, code comments, etc.  
   - `bestpractices.md`: Describe strategic coding principles and philosophies

*Customizing these files is essential—AI agents use them to think and build like you.*

---

### 3. Link Agent OS to Cloud Code (Claude)  
1. Run the Cloud Code setup script:  
   ```bash
   curl -s https://buildermethods.com/setup-cloudcode.sh | bash
   ```  
2. Verify that the `~/.claude/claude.md` file references your Agent OS standards and instructions using `&`-prefixed paths (e.g., `&~/agentos/standards/techstack.md`).  
3. Ensure the following commands appear in `~/.claude/commands/`:  
   - `analyze product`  
   - `plan product`  
   - `create spec`  
   - `execute tasks`

---

### 4. Link Agent OS to Cursor  
1. Open the codebase directory of your project.  
2. Run the Cursor setup script from within the project folder:  
   ```bash
   curl -s https://buildermethods.com/setup-cursor.sh | bash
   ```  
3. Check for a `.cursor/rules/` folder containing the same four command files as Cloud Code, all referencing `~/agentos/instructions`.

---

### 5. Plan a New Product  
1. Navigate into your project folder in terminal or open it in Cursor/Cloud Code.  
2. Run the `plan product` command:  
   - In Cloud Code, type `/plan product`  
   - Respond to prompts about your product idea, target user, feature ideas, and tech stack

*If you’re working on an existing codebase, use `/analyze product` instead.*  
*This documents the “why” behind what you’re building—essential context for agents.*

---

### 6. Review the Product Plan  
Check the generated files under `agentos/product/`:  
- `mission.md`: Elevator pitch, problem/solution, user types, differentiators  
- `roadmap.md`: Phased feature breakdown with priorities and dependencies  
- `textstack.md`: Tech stack per project (based on your defaults + adjustments)  
- `decisions.md`: Log of decisions made, their rationale, and consequences

*Review and edit to ensure alignment with your vision before building features.*

---

### 7. Create a Feature Specification  
1. Run `/create spec` to begin planning the next roadmap item  
   - Or ask: “What’s next?” to let the agent guide the selection  
2. Review the resulting spec folder:
   - `spec.md`: Overview, user stories, deliverables, in/out of scope
   - `subspects/`: Includes files like `api.md`, `schema.md`, `tech.md`
   - `tasks.md`: Auto-generated checklist to build and test feature

*You only need to review and approve—no need to write the spec manually.*

---

### 8. Execute Feature Development  
1. Once approved, respond with `yes` or specify which tasks (`1, 2, 3`) to execute.  
2. Monitor progress in your codebase and terminal:
   - Code and tests will be generated
   - Task status is updated live in `tasks.md`  
3. Launch your app and validate visually and functionally  
   - For Rails: run `rails server` and navigate to your app in the browser  
   - Confirm tests pass by running test suite (`rails test` or equivalent)

---

## Pro Tips & Common Pitfalls  
- ⚙️ Customize the `standards` folder before generating specifications for best results  
- 📂 Keep Agent OS files in your home directory for centralized referencing  
- 💡 Use `/analyze product` for existing apps to create a plan based on current progress  
- 🧪 Tests are generated automatically using test-driven development principles  
- ✅ By default, only one task is executed at a time—specify more if needed  
- 🧠 Instructions are structured in markdown + XML and can be tailored, but defaults are production-ready  
- 🔁 Create rules once and reuse them across Cloud Code, Cursor, and other AI tools

---

## You’re Done When…  
✅ The following are in place:  
- Agent OS folder exists in both your system and individual project(s)  
- Your standards (tech stack, code style, best practices) are customized  
- Product plan is completed with clear mission, roadmap, and decisions log  
- Specs for at least one feature are generated and reviewed  
- Tasks are executed and validated with passing tests and working UI

Your AI agent now works with your architecture, patterns, and development workflow—like a trained teammate.

---
```
## References:
 - [The Missing SYSTEM Your Coding Agents Need](https://www.youtube.com/watch?v=CTMyzeKKb0o)