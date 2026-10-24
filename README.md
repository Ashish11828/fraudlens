<div align="center">

# FraudLens

### PAUSE. CHECK. VERIFY.

An accessibility-first scam-prevention experience designed for a **600 × 600 Meta Ray-Ban Display preview**.

[Try the live app](https://scamfruadlens.netlify.app/) · [Watch the demo](https://drive.google.com/file/d/1mxk_QB9SAB7yR2BMgr0MdIzllzrnREJZ/view) · [Project gallery](https://www.krazyykrunal.com/buildtheinvisible/project-gallery/preview.html?project=fraudlens)

</div>

---

## Why FraudLens exists

Suspicious messages often create urgency, fear, or confusion. FraudLens gives people a moment to pause and work through simple questions before making a payment, clicking a link, or sharing information.

The experience is designed with older adults, people with low digital literacy, and people with cognitive or processing accessibility needs in mind. Short prompts, large controls, and calm screens keep the interaction easy to follow.

## Demo video

**[▶ Watch the FraudLens project demo](https://drive.google.com/file/d/1mxk_QB9SAB7yR2BMgr0MdIzllzrnREJZ/view)**

The demo above is the original video linked in the Build The Invisible project gallery. A copy is also included in this repository: **[Download the demo video](docs/fraudlens-demo.mp4)** (approximately 55 MiB).

## What you can do

| Feature | Experience |
| --- | --- |
| Guided check | Answer four Yes / No questions about money, urgency, links, and sensitive information. |
| Risk guidance | Receive a rule-based result based on the number of warning signs selected. |
| Scam simulator | Practice with three built-in examples and review feedback. |
| Pressure cards | Recognize urgency, fear, authority, reward, and secrecy tactics. |
| Accessibility settings | Adjust text size, high contrast, an alternative font, and reduced motion. |
| Read aloud | Hear screen content through the browser's speech synthesis support. |
| Saved preferences | Keep accessibility preferences in browser local storage. |

## How it works

1. Open **Check Something** from the home screen.
2. Answer the four short questions about the situation.
3. Review the warning level and suggested next steps.
4. Use **Learn** to practice or **Pressure Cards** to recognize common manipulation patterns.

The current app uses fixed questions and local rules. It does not scan incoming messages or use an AI model to verify whether a message is genuine. Simulator labels are illustrative and should not be treated as real-world verification.

## Run locally

Requirements: Node.js and npm, plus a modern web browser.

```sh
git clone https://github.com/Ashish11828/fraudlens.git
cd fraudlens
npx serve -s .
```

Open the local address printed in the terminal. The repository is private, so cloning requires access to it. No build step or API key is needed.

Use a web server rather than opening `index.html` directly, so client-side routes work correctly.

## Controls

| Screen | Key | Action |
| --- | --- | --- |
| Home | Enter | Start a guided check |
| Guided check | Left or Enter | Yes |
| Guided check | Right or Down | No |
| Simulator | Left or Enter | Choose Safe |
| Simulator | Right or Down | Choose Scam |
| Any screen | Escape | Return home |

On-screen buttons also support mouse and touch interaction. Read-aloud availability depends on the browser and installed voices.

## Technology

- **HTML, CSS, and vanilla JavaScript** in a single app file.
- **History API** for browser navigation.
- **Local Storage** for accessibility preferences.
- **Web Speech API** for read-aloud support.
- **Netlify redirects** for direct navigation to app routes.

## Project structure

```text
fraudlens/
├── index.html       # App UI, styles, scenarios, and interaction logic
├── _redirects       # Netlify fallback for client-side routes
├── README.md        # Project overview and setup
└── docs/            # Demo media and documentation
```

## Deploy on Netlify

Deploy the repository root as a static site:

| Setting | Value |
| --- | --- |
| Build command | Leave empty |
| Publish directory | `.` |

The included `_redirects` file sends routes such as `/check`, `/simulator`, and `/pressure` to `index.html`.

## Team

**Team Invisible Creator**

- [Ashish Kumar](https://github.com/Ashish11828)
- Manav Rajpurohit

Team credits follow the original project gallery. The gallery lists ChatGPT and Claude as development and ideation assistants.

## About this repository

This working version was recovered from the deployed FraudLens app on **24 October 2026**, at the project owner's request. It preserves the deployed HTML, CSS, and JavaScript. Original development files and earlier Git history were unavailable.
