# Bright Futures Funding Workspace (showcase)

Public showcase for a private project. The source code is not published here.

This is a small fundraising ERP, built as a class prototype for a local nonprofit that supports women creatives. It covers the donor lifecycle in one place instead of spreadsheets and scattered email.

## The problem

A small nonprofit team tracks donors, grants, events and thank-yous in separate tools. Donors get missed, thank-yous go out late, and the board gets no regular view of the pipeline.

## How it works

| Stage | What the app does |
| --- | --- |
| Identification | Potential donors enter a pipeline |
| Qualification | Each donor is scored for capacity and for affinity with the mission |
| Cultivation | Relationship log per donor, a calendar of events and campaigns, "needs a touch" reminders |
| Solicitation | Pipeline board, grant finder and grant tracking, weekly board report |
| Stewardship | Automatic thank-you emails, personalized newsletters, and a donor-facing impact report with a private page per donor |

A daily scheduled job sends newsletters whose date has arrived and, on Mondays, emails the grant report to the board.

## Design notes

- Money is stored as integer cents.
- Emails are recorded in an outbox in demo mode and only delivered when an email provider is configured.
- The grant finder is mocked: it returns sample opportunities behind a single function, so a model with web search can replace it without changing the flow.
- All seeded data is fictional. A bundled demo database lets it run without setup.
- There is no login yet. That is stated openly: authentication has to be added before any real donor data goes in.

## Architecture

Next.js App Router with server actions, Drizzle ORM on SQLite/libSQL, a cron route for scheduled work, an email module, and a metrics module that feeds the dashboard and charts.

## Stack

Next.js 16, React 19, TypeScript, Tailwind CSS 4, Drizzle ORM, SQLite/libSQL, Resend, Vercel.

## Status

Prototype built in October 2026 (four commits over a few days) as part of a class project with a team at the University of Notre Dame. It is a demo with fictional data, not a production system.

## What is shown and what is kept private

Only this README is public. The source is private because the app is built for a real organization and is not meant to be reused or deployed with real donor data without authentication and review.
