# Web app browser test report (Claude skill)

Go through a web app's flow in a real browser like a new user and get a numbered report of every step that fails or looks wrong. The skill hands the job to your own MyClawn cloud computer: a real browser that stays signed in, its own email address and files. It comes back with the answer, a screenshot of the final screen and a link to a screen recording.

## Example request

> Open <your app URL> with the test account <email> / <password>. Go through sign-up, creating a project and inviting a teammate. For every step that fails or looks wrong, write the step, what you expected and what you saw.

## What you get

- It answers with a numbered report: the step, what it expected, what it saw, and the page address.
- A screenshot of the final screen and a link to a screen recording.

## What it does not do

- Use a test account with no real data; give it no credentials you would not hand to a new colleague.
- It tests by looking and clicking. It is no replacement for automated tests in your code, and it can miss what needs a specific device or network.
- It reports; it does not fix your code.

## Install

Claude Code, as a personal skill:

```sh
mkdir -p ~/.claude/skills/web-app-browser-test-report && curl -fsSL https://raw.githubusercontent.com/20vision/web-app-browser-test-report-skill/main/SKILL.md -o ~/.claude/skills/web-app-browser-test-report/SKILL.md
```

With the skills tool (installs into the current project):

```sh
npx skills add 20vision/web-app-browser-test-report-skill
```

## Needs

The MyClawn Computer connector, signed in with your own MyClawn account. Setup and details: https://www.myclawn.com/docs/connectors?utm_source=github&utm_medium=repo&utm_campaign=web-app-browser-test-report

Full description of this job, with the steps and the limits: https://www.myclawn.com/test-my-web-app-in-a-real-browser?utm_source=github&utm_medium=repo&utm_campaign=web-app-browser-test-report

## Also listed

- https://www.skillsdirectory.com/skills/20vision-web-app-browser-test-report
- https://www.agensi.io/skills/web-app-browser-test-report
- All skills: https://github.com/20vision/skills

Made by 20Vision, the company behind MyClawn.
