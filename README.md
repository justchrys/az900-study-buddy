# AZ-900 Study Buddy (Unofficial)

> A free, no-login study companion for Microsoft Azure Fundamentals (AZ-900): plain-language explanations with everyday local analogies, original practice questions that explain every answer, and a readiness tracker by exam domain.

**Unofficial.** This project is not affiliated with, endorsed by, or sponsored by Microsoft. It uses no Microsoft logos and no real exam questions. Content follows the public [AZ-900 skills outline](https://learn.microsoft.com/credentials/certifications/resources/study-guides/az-900) and should always be verified on Microsoft Learn.

Built for the **#1MillionDevs AZ-900 Vibe Coding Hackathon** (20 to 23 October 2026) by Chrystabel Young, solo.

**Live demo:** https://justchrys.github.io/az900-study-buddy/

![Study Buddy](docs/screenshot-buddy.png)

## The problem

I kept failing the same elasticity vs. scalability questions because every definition sounded identical: “the ability to handle changing demand.” What fixed it was a boda boda rider in Nairobi. Scalability is buying a second bike because your regular customers doubled over the year. Elasticity is calling in three riders for one chaotic Friday when a nearby office empties out at 5pm. The other thing that nearly broke me was practice tests that said “Incorrect” with no explanation. I started writing one sentence on why I chose each wrong answer, and those notes did more for me than the tests themselves. This app is the tool I wished I’d had.

## What it does

| Tab | Hackathon track | What it does |
|---|---|---|
| Study Buddy | Study Buddy | 16 short concept explanations, each with a plain-language definition, an everyday local analogy and an exam tip. Tap a topic or type a keyword. |
| Quiz | Smart Quiz Builder | 22 original questions across the three exam domains. Answer order is shuffled every time. Every answer gets an explanation, and wrong answers get a note on the specific misconception. |
| Readiness | Readiness Tracker | Accuracy per domain, an overall estimate weighted by the exam’s domain weights, and your five weakest subtopics. “Target my weakest area” sends you back to them. |

## Design decisions

- **Misconception-first feedback.** Every distractor has its own explanation of why it is wrong. This is the habit that worked for me when I studied.
- **Analogies that stick.** Concepts that sound alike (scalability vs elasticity, Policy vs locks, VPN vs ExpressRoute) are explained with side-by-side everyday examples.
- **Honest readiness.** The overall estimate is only meant as a guide once you have answered at least 5 questions in every domain. It is a study aid, not a prediction of your exam result.
- **No accounts, no servers, no AI at runtime.** It runs entirely in the browser and works offline. Progress is saved in `localStorage`.

## How the content was made

The content was drafted with AI assistance (Claude) from the public skills outline and then checked against Microsoft Learn. Questions are original and are not copied from any exam or practice test.I reviewed every question against the Microsoft Learn pages for its subtopic.

## Readiness calculation

Accuracy per domain, weighted by approximate exam weights (Cloud Concepts 27.5%, Architecture and Services 37.5%, Management and Governance 35%, the midpoints of the published ranges).

## Tech

- Single-file HTML, CSS and JavaScript (`index.html`), no build step and no dependencies
- Hosted on GitHub Pages
- Built with AI-assisted tools (Claude.ai) and VS Code

## Run it

Open the live demo link, or download `index.html` and open it in a browser.

## Limitations

- A small content set (22 questions, 16 explanations), English only. It is not a full practice exam.
- AI-assisted content can contain mistakes. Check against Microsoft Learn.
- Progress lives in one browser and does not sync between devices.

## Roadmap

- More questions per subtopic, including the Azure IoT, AI and serverless categories
- Flashcards from missed questions and a mistake-notes box (“why did I pick this?”)
- Study planner from exam date and weak areas
- Local-language versions, reviewed by native speakers
- Other certifications (AZ-104, AI-900, AWS Cloud Practitioner)

## Repo layout

```
index.html   # the whole app
README.md
docs/        # screenshots
```
