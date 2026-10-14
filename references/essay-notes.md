# Notes on the essay

Felix Rieseberg, "How to be more ambitious: a tutorial for humans with models", 13 October 2026.
https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/

Felix leads engineering for Claude.ai, Cowork and Claude Code Desktop at Anthropic. He wrote the essay because "we're not ambitious enough" had become a slogan without instructions. His running example is a quarterly business review (QBR) deck at an imagined company called Acme.

## Altitude
- **The question to ask:** what do you want to happen next, and what is the goal beyond the goal? Felix moved from asking Claude to fix single crashes to asking it to keep the apps free of crashes.
- **QBR rungs, from least to most ambitious:**
  1. Instead of updating the template numbers, give the model as much data as possible and ask what changed this quarter, why, and what to do about it.
  2. Ask it to work out the three most urgent decisions and start on options with arguments for and against.
  3. Say the review exists so leadership catches problems early and moves money and people to the right places. Ask it to design a better way to do that than a quarterly deck, show from the company's own history that it would have caught problems sooner, and run it beside the current deck for a quarter.
- **When altitude fits:** when you are after an outcome. Felix says a good sign is that you'll hold meetings about the work. It fits less well for creative work, and simply telling Claude to make money doesn't work for most businesses in 2026.
- **Wiring:** altitude is where durable workflows come from, which take the human out of the loop. Felix had to change his own setup first. Claude needed to fetch crash reports, map app versions to commits, and use Windows, macOS and Linux machines to reproduce and verify fixes.

## Depth
- **Same instruments as the best:** models told to act like a professional often change their words without changing their methods. Insist on the actual tools, e.g. databases and statistical models instead of markdown tables. You don't need to know the tools yourself, because the model usually does.
- **Unreasonable goals, called reasonable:** if you need a page to load in 5 seconds instead of 10, ask for 200 milliseconds. When the model says something seems impossible, say it's solvable and that it should keep going.
- **Challenge what you know:** give the model the raw data and ask it to check a belief adversarially. Felix's example is a company that believes its churn comes from onboarding, and he asks the model to try to reproduce that belief from the raw data.
- **Produce new knowledge:** once the model is deep in the data, ask it to find a blind spot. Felix's example is to simulate the last year of customers from the logs, find an early sign of churn nobody knows about yet, and show that the sign predicts churn on data the model hasn't seen.
- **Outside judge:** don't ask the model to judge itself. In October 2026 Felix insists on outside validation, ideally a tool the model can run for immediate feedback.
- **Felix's depth prompt, paraphrased:** ask for a deeper version of the task rather than a bigger one. Before rewriting the task, the model says what a top professional would do that wasn't asked for, names the rawest material they would start from, names the methods and tools they would use, and names something other than the model or the person that would show the result is right. Then the model rewrites the prompt to ask for exactly that.

## Range
- **Nouns to verbs:** a trick from "The Art of Innovation" by Tom Kelley and Jonathan Littman. A QBR is not a deck. It is getting busy people to believe a story about cause and effect, and to decide under uncertainty, in 30 minutes.
- **Assemble the crew:** Felix imagines the deck must be excellent or the world ends, and asks who humanity would send. For production quality he picks an analyst, a journalist and an editor. If it's presented, he adds a motion and audio designer. To attack it, he adds a short seller and a forensic accountant.
- **Avoid role play:** use the crew to find fields and techniques. Don't ask the model to write as a short seller. Ask it to do what a short seller does to research a position.
- **Example of range:** Felix had never thought of using Claude to build 3D scenes for his homepage until a colleague, Alex Albert, used Blender to render interior designs.

## Why it works
Felix calls the underlying problem self-efficacy, which means how far people believe in their own abilities. People who believe more achieve more. He cites these examples:
- **Hard goals:** Locke and Latham reviewed 35 years of research and found that people given specific hard goals do better than people told to do their best.
- **Believing it's possible:** in 1939 George Dantzig solved two unsolved statistics problems because he thought they were homework.
- **Seeing someone else do it:** after Roger Bannister ran a mile in under 4 minutes in 1954, others followed within weeks. In April 2026 two runners finished the London Marathon in under 2 hours in the same race.
- **Permission to fail:** "The Inner Game of Tennis" argues you play worse when you try too hard, and Linux was first announced as a hobby project.

He ends by noting that model abilities jump every few weeks, so people need ways to attempt things they didn't believe possible.

## Requirements
All of the methods need the model to have a computer that can install software, and access to the relevant data through connectors or other means.
