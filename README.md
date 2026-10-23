# codehands-web

**This repo is empty on purpose. It has no role in the current Code Hands AI design and no owner.**

Part of [Code Hands AI](https://github.com/devweekends/codehands-docs).

## Why it exists

The first plan had a phone web app here: a Next.js app on Vercel where you could sign in, watch a session live, start a task and approve it from your phone, while the laptop did the work. Commands went from the phone to a cloud API and down to the laptop over its open connection.

## Why it is parked

The design moved to **local-first** ([docs README](https://github.com/devweekends/codehands-docs#design)):

- Everything a task needs runs on the desktop: the [desktop app](https://github.com/devweekends/codehands-desktop), a local database, the daemon and the [runner](https://github.com/devweekends/codehands-agent).
- The cloud [only stores state](https://github.com/devweekends/codehands-backend), so signing in on another machine brings your sessions, memory and preferences with you. It runs nothing and passes no commands.

With no commands going through the cloud, a phone has nothing to drive, so the web app was dropped from the current design.

## What would bring it back

A web or phone view returns only through a new decision in [codehands-docs/decisions](https://github.com/devweekends/codehands-docs/tree/main/decisions). The plan's later phases are the likely reasons:

| When | What a web client would do |
| --- | --- |
| Month 5 | Watch a task and approve it from a phone while the laptop lid is closed and the task finishes in the cloud |
| Month 6 | A web view for self-hosted installs |

If that happens, this README gets replaced with the real one: owner, the contracts it uses (at least C3 and C5 from [codehands-contracts](https://github.com/devweekends/codehands-contracts)), stack, and how to run it.

Until then, please do not add code here.
