# "Creating Custom Mobile App UIs with Claude AI and Cloud Code Sub-Agents"

## Build a Custom Mobile App UI with Cloud Code Sub‑Agents

Easily generate high‑quality mobile app layouts, apply custom themes, and convert them to SwiftUI apps using AI agents.

---

## Prerequisites / Materials

- Access to **Claude AI** with Cloud Code support  
- Sample app requirements (a simple product description or use case)  
- Basic knowledge of **HTML/CSS/JavaScript**  
- Optional: familiarity with **SwiftUI** for iOS app conversion  
- [Cloud Code sub‑agents](https://www.anthropic.com) configuration files (shared in video description)  

---

## Estimated Time & Difficulty

- ⏱ **Time**: 30–60 minutes  
- 🎯 **Difficulty**: Medium  

---

## Step‑by‑Step Instructions

### 1. Define Your App’s Purpose

Write a simple requirements prompt describing the app (e.g., a university app for checking grades and schedules).  
*Think of it as a PRD—avoid technical specs and just focus on user actions and goals.*

---

### 2. Activate the “Mobile UX Engineer” Agent

Use Claude Cloud Code to run the Mobile UX Engineer agent with your prompt.  
- Ensure the agent is configured to produce **HTML with no color styling**  
- It will generate the raw app structure and user flow based on your description

*Separating layout from design ensures better user experience decisions.*

---

### 3. Review and Save the Generated HTML

Inspect the HTML output for usability and logical flow.  
Save the file for use in the next stage.

---

### 4. Activate the “Mobile UI Implementer” Agent

Request the UI Implementer to apply design styling to your saved HTML.  
- Provide a **color scheme** and set the **design field** (e.g., minimal, 3D, Notion-inspired)  
- Optionally, upload image links for color sampling

*Styling is separated from layout to maintain clarity and control.*

---

### 5. Generate Multiple UI Variations (Optional)

For different looks:
- Use a prompt like: `Can you fire up two UI agents with the same structure but different color schemes?`  
- Specify each color scheme or style per agent

*Explicitly stating the number of agents prevents default single-agent responses.*

---

### 6. Choose Your Best Design

Review the UI versions. Pick the one that aligns best with your app's purpose.  
Minor layout overlaps or design quirks can be fixed manually or adjusted via prompt.

---

### 7. Split HTML, CSS, and JavaScript

Ask Claude to separate your files for cleaner structure.  
This makes editing easier and reduces complexity.

---

### 8. Convert HTML to iOS SwiftUI App

Use Claude with the **HTML Converter Agent** to transform your HTML/CSS/JS into SwiftUI code.  
- Provide a representative HTML snippet  
- Ask for conversion + SwiftUI documentation using `context 7 mcp`  
- Prompt 2–3 improvement rounds to refine output  

*Context 7 MCP ensures fast and accurate documentation retrieval.*

---

### 9. Finalize and Test in iOS Simulator

Load the converted SwiftUI app into Xcode and run it in the iOS Simulator.  
Check usability, icon placement, and visual polish.

---

## Pro Tips & Common Pitfalls

- 🔹 Use **emojis for icons** during HTML prototyping—replace them later in SwiftUI  
- 🔹 Always name agents explicitly and define how many to spawn   
- 🔹 Keep HTML output clean by splitting into CSS/JavaScript files early  
- 🔹 Stick to HTML for easy edits before converting into platform-specific code  
- ⚠️ Avoid abstract prompts; clearly define styles and agents to avoid random results  
- ⚠️ Layout bugs (like overlapping) are usually fixed by adjusting design parameters or redrawing UI agents  

---

## You’re Done When…

- ✅ Your app has a clear, responsive layout generated in HTML  
- ✅ At least one styled variation with applied color themes looks polished  
- ✅ You have SwiftUI files running successfully in the Xcode simulator  
- ✅ HTML is cleanly separated into HTML, CSS, JS  
- ✅ Design choices reflect both usability and visual consistency

---

You're now ready to iterate and build richer UI designs using this workflow with Claude AI’s Cloud Code system.
## References:
 - [Wait... 80% of UI Workflows Are Pointless Now With This Claude Code Setup](https://www.youtube.com/watch?v=uayt-IVbh8E)