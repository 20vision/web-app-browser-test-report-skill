---
name: web-app-browser-test-report
description: Go through a web app's flow in a real browser like a new user and get a numbered report of every step that fails or looks wrong. Use when someone wants a web app tested by looking and clicking.
---

# Web app browser test report

This job runs on the user's own MyClawn cloud computer: a real browser that stays signed in, its own email address and files. It can outlast the chat and comes back with the answer, a screenshot of the final screen and a link to a screen recording.

## Setup

The user must have the MyClawn Computer connector signed in. If it is not, set it up as below and let the user do the sign-in; do not create accounts for them.

Connect the MyClawn Computer server with the user's own MyClawn account (OAuth sign-in): https://www.myclawn.com/mcp/desktop
Claude Code: `claude mcp add --transport http myclawn https://www.myclawn.com/mcp/desktop`, then `/mcp` and choose myclawn to sign in. Other clients: https://github.com/20vision/myclawn-computer-mcp
A new account gets a free 24-hour computer on its first task. Plans and details: https://www.myclawn.com/docs/connectors?utm_source=github&utm_medium=repo&utm_campaign=web-app-browser-test-report

## Task

Hand this task to the connector's task tool, in the user's own words. The job page gives this example:

> Open <your app URL> with the test account <email> / <password>. Go through sign-up, creating a project and inviting a teammate. For every step that fails or looks wrong, write the step, what you expected and what you saw.

Replace the placeholders and the example values with the user's own. Show the final wording to the user before sending anything that submits a form, books something or writes to a third party.

## Steps

1. The job page says: “You describe the flow and give a test account.” Write the task with the goal, the sites, what the result must look like and what must not be done.
2. Send it with the connector's task tool and wait for the result.
3. What the computer does, as the job page describes it:
   - It opens your app in its own browser and goes through the steps like a new user, noting each place something fails or looks wrong.
   - It answers with a numbered report: the step, what it expected, what it saw, and the page address.
4. Report the answer, the screenshot and the recording link.

## Limits

- Use a test account with no real data; give it no credentials you would not hand to a new colleague.
- It tests by looking and clicking. It is no replacement for automated tests in your code, and it can miss what needs a specific device or network.
- It reports; it does not fix your code.

Full description of this job, with the steps and the limits: https://www.myclawn.com/test-my-web-app-in-a-real-browser?utm_source=github&utm_medium=repo&utm_campaign=web-app-browser-test-report
