---
name: ambition
description: Rewrites a task the user gives into a more ambitious version using Felix Rieseberg's altitude, depth and range method, shows it as a short brief, and waits for the user to choose before doing any of the work. Use it only when the user asks for it, e.g. "/ambition", "be more ambitious", "make this more ambitious", "what's the ambitious version of this", or when they name altitude, depth or range. Don't use it on ordinary tasks they haven't asked to expand.
---

# Ambition

Felix Rieseberg's essay "How to be more ambitious: a tutorial for humans with models" (13 October 2026) is written for the person prompting the model. Its argument is that the person usually limits the result, because they ask for the task instead of the outcome, hand over digested data instead of raw data, and stay inside one field. When the user calls this skill, you do their half of that work. You rewrite their task the way they would if they applied the essay, show them the rewrite, and wait for them to choose.

The essay names four kinds of ambition:
- **Speed:** the same work in less time. Models already do this by default, so skip it.
- **Altitude:** aim at the outcome beyond the task.
- **Depth:** do the task the way the field's best practitioner would.
- **Range:** bring in methods from fields the task doesn't obviously need.

A short summary of the essay, with its worked examples, is in `references/essay-notes.md`. Read it the first time you use this skill in a session, or when a task is hard to lift.

## Workflow

### 1. Look before you lift
Read what the task touches first, e.g. the code, the data, the earlier messages or the files the user mentions. Find out what data, tools and access exist. An ambitious version built on a wrong idea of what's available is useless, and the altitude version in particular depends on what you can reach. Reading is fine at this stage, but don't start the work itself.

### 2. Write the altitude version
Ask what the user wants to happen after the task is done, and what the goal beyond the goal is. Climb in rungs, the way the essay climbs from "make the quarterly deck" to "design a better way for leadership to catch problems early":
- **Rung 1:** the same task, but with all the data you can get, aimed at what changed, why, and what to do about it.
- **Rung 2:** the decisions the task feeds. Work out which ones are most urgent and draft options with the case for and against.
- **Rung 3:** the standing job the task exists to serve. Design a better way to do that job, show from the user's own history that it would have worked sooner, and propose running it next to the current way for a while.

Altitude fits best when the work leads to meetings or decisions, or comes back again and again. It fits less well for creative work, so say so when that's the case.

Name the wiring. To own an outcome instead of a task, you need access that the user would otherwise supply by hand each time, e.g. to keep apps free of crashes, Felix first gave Claude crash reports, a map from app version to commit, and machines to reproduce bugs on. List the missing access or data as the first steps, because without it the altitude version turns back into a list of tasks.

### 3. Write the depth version
Answer the essay's four questions:
1. What would a top professional in this field do here that the user isn't asking for?
2. What is the rawest material they would start from, instead of what has already been summarised?
3. Which specific methods and tools would they use? Name the instruments, not the vocabulary, e.g. a database and a statistical model instead of a markdown table. Models asked to act like experts tend to switch words without switching methods, so check that the method itself changed.
4. What, other than you or the user, would show the result is right? This is the outside judge. The best judge is one you can run yourself for fast feedback, e.g. a test suite, a held-out evaluation set, a replay of historical data, a real user's action, or an expert scoring blind. Don't use your own opinion of your work as the judge.

Then add these:
- **An unreasonable target, stated as reachable.** Make it a number. If the task is to cut a page load from 10 seconds to 5, the target is 200 milliseconds.
- **One belief to test.** Name an assumption the user or the task takes for granted, and say how you would try to reproduce it from the raw data.
- **New knowledge.** Say what blind spot you would look for once you are deep in the data, and how you would show it predicts something on data it hasn't seen.

### 4. Write the range version
- **Restate the noun as verbs.** A quarterly review is not "a deck". It is getting busy people to believe a story about cause and effect, and to decide under uncertainty, in 30 minutes. The verbs show which fields can help.
- **Pick the crew.** Ask which fields the best possible team would include if the result had to be excellent. Include someone whose job is to attack the plan, e.g. a short seller or a forensic accountant.
- **Take methods, not voices.** For each field, name the specific method it brings and how it changes the plan. Ask for what a short seller does to research a position, not for text written in a short seller's voice, because role play makes the transcript stranger without improving the result. Keep 2 to 4 fields and drop any that only add vocabulary.

### 5. Check the brief before showing it
- **Deeper, not bigger.** Each version should aim higher or dig deeper, not simply add more items.
- **Concrete:** every version names an outcome, a number where one makes sense, and an outside judge.
- **Costs are visible:** say what each version costs in time and money, and what it needs from the user.
- **Limits still apply.** Ambition doesn't change what needs the user's approval. Mark any step that sends messages, contacts people, spends money, publishes, or changes something live as "needs your OK".

### 6. Show the brief and stop
Use the format below. Keep it under about 450 words so the user can read it in a minute. Write in plain language. End by asking them to pick a version, a mix, or edits. Then stop. Don't start the work in the same turn, because each version changes the scope, the cost or who is affected, and the user has asked to choose first.

```
# Ambitious version of: <the task in the user's words>

**As asked:** <one sentence on the task as given>
**My pick:** <which version or mix, and why, in one or two sentences>

## Altitude
- **Goal beyond the goal:** ...
- **Rungs:** 1 ... 2 ... 3 ...
- **Wiring needed:** ...

## Depth
- **What a top <field> would add:** ...
- **Rawest material:** ...
- **Methods and tools:** ...
- **Outside judge:** ...
- **Target:** <number>, and why it's hard but reachable
- **Belief to test:** ...

## Range
- **As verbs:** ...
- **Fields and their methods:** ...
- **Attack on the plan:** ...

## First step
<what you'd do first, how long it takes, what it costs, and which steps need the user's OK>

Which version, mix or edits?
```

## After the user chooses
- **Set up the judge first.** Build or find the outside judge before the main work, so you measure from the start instead of grading yourself at the end.
- **Wire access early.** For an altitude version, set up the missing access before the work, or ask the user for it.
- **Hold the target.** The essay cites research where specific hard goals beat "do your best", and cases where people solved hard problems because they believed them solvable. When the work gets hard, don't quietly fall back to the safe version. Say what's blocking you, keep going on the rest, and ask before changing the target.
- **Report against the judge.** Give the result as the judge measured it, and say plainly if you missed the target.
