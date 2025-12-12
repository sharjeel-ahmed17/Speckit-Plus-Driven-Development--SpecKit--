# Hackathon Overview

This document compiles information from the provided Google Docs links related to upcoming or planned hackathons. Note: Direct extraction of content from these Google Docs was limited due to access restrictions (likely requiring viewer/editor permissions). The titles suggest a series of hackathons focused on AI-native development themes. For full details, please ensure the documents are publicly shared or grant access.

If you're participating or organizing, consider integrating **SpecKit+ Driven Development** (from the previous guide) to structure your hackathon projects efficiently—e.g., using `/sp.specify` for idea validation and `/sp.implement` for rapid prototyping.

## Hackathon I: Physical AI & Humanoid Robotics Textbook

- **Link**: [View Document](https://docs.google.com/document/d/1nw6D37JmTfhPLHo0IfTeCcKajX3Lw9PidDmBjMG1G5o/edit?tab=t.0)
- **Theme**: Physical AI and Humanoid Robotics (potentially building a collaborative textbook or resource guide).
- **Status**: Planned/In Development.
- **Key Focus Areas** (Inferred from Title):
  - Exploring AI applications in physical robotics.
  - Humanoid robot design, simulation, and real-world integration.
  - Collaborative knowledge-sharing via a textbook format.
- **Suggested SpecKit+ Integration**:
  - `/sp.constitution`: Define rigor for technical accuracy in robotics content.
  - `/sp.specify`: Outline chapters on kinematics, AI control systems, etc.
  - Use MCP servers for GitHub collaboration and agent skills for code generation.

> **Action Item**: Request share access or export the doc as PDF/Markdown for team review.

## Hackathon II: Todo Spec-Driven Development

- **Link**: [View Document](https://docs.google.com/document/d/1KHxeDNnqG9uew-rEabQc5H8u3VmEN3OaJ_A1ZVVr9vY/edit?usp=sharing)
- **Theme**: Todo App built with Spec-Driven Development (aligns perfectly with SpecifyPlus workflows).
- **Status**: Planned/In Development.
- **Key Focus Areas** (Inferred from Title):
  - Implementing a task management ("Todo") application using specification-first methodologies.
  - Emphasis on AI-assisted planning, task breakdown, and implementation phases.
  - Potential for sub-agents handling features like reminders, prioritization, or integrations.
- **Suggested SpecKit+ Integration**:
  - Start with `specifyplus init todo-hackathon`.
  - `/sp.specify`: Core features (add/edit tasks, due dates, AI suggestions).
  - `/sp.plan`: Architecture for frontend/backend with MCP for context.
  - `/sp.implement phase ui`: Rapid prototyping with Claude via free CCR setups.

> **Action Item**: Use the workflow from the [SpecKit+ Guide](#) to kick off this hackathon. Export the doc for detailed rules/schedule.

## General Hackathon Guidelines (Recommendations)

Since direct content access was limited, here's a template based on standard hackathon best practices, tailored to these themes:

### Rules
- Teams: 2–5 members.
- Duration: 24–48 hours.
- Tech Stack: Open-source preferred; integrate AI tools like Gemini CLI or Bonsai.
- No pre-existing code; all work during the event.

### Schedule (Example)
| Phase          | Time Slot              | Activities |
|----------------|------------------------|------------|
| Kickoff        | Day 1, 9:00 AM         | Theme reveal, team formation, `/sp.constitution` setup. |
| Ideation       | Day 1, 10:00 AM – 12:00 PM | `/sp.specify` and `/sp.clarify` sessions. |
| Building       | Day 1, 12:00 PM – Day 2, 9:00 AM | `/sp.plan`, `/sp.tasks`, `/sp.implement` cycles. |
| Demos          | Day 2, 10:00 AM – 12:00 PM | Presentations with live demos. |
| Judging        | Day 2, 1:00 PM         | Criteria: Innovation, Feasibility, Spec Adherence. |

### Prizes (Suggested)
- **1st Place**: $1,000 + xAI API credits.
- **Best Use of SpecKit+**: Free SuperGrok subscription.
- **Most Creative AI Integration**: Robotics hardware kit.

### Submission
- Repo: GitHub with AGENTS.md.
- Demo Video: 3-min Loom recording.
- Spec Artifacts: Include `/sp.*` outputs in README.

## Next Steps
1. **Access Docs**: Make the Google Docs publicly viewable or share links with edit access.
2. **Start Project**: Run `specifyplus init <hackathon-name>` and select Claude backend.
3. **Team Up**: Use sub-agents for division of labor (e.g., one for research, one for coding).

For real-time updates or questions, reply with more details. Let's build something awesome! 🚀