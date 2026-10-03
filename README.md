# Montclair CBT — Montclair Group of Schools

**Shared backend + frontend** so when a student or staff registers on any phone, the Admin sees them.

## Admin (only ONE account — nobody else can be admin)

- Email: `montclaircollege001@gmail.com`
- Password: `Montclair College 1234@$$$`

## School code for Staff / Students / Parents

`MONT2026`

## Why you need the server

Without the server, each phone keeps its own data (local only).  
With the server, **all devices share one database**.

## Run locally (connected)

```bash
cd server
npm install
npm start
```

Open http://localhost:3001

## Deploy on Render (recommended for shared use)

1. Create a **Web Service** on [render.com](https://render.com) (free tier works)
2. Connect this repo OR upload the project
3. **Root directory:** leave as project root, or set to folder containing `server`
4. **Build:** `cd server && npm install`
5. **Start:** `cd server && node index.js`
6. Add disk or note: data is stored in `server/data/db.json` (on free tier it may reset unless you attach a disk)

Open the Render URL on admin phone and student phones — same data.

## Excel bulk questions

Headers (first row):

```
question,optionA,optionB,optionC,optionD,correct,marks
```

- `correct` can be the full answer text **or** letter A/B/C/D  
- Sample file: `assets/questions-template.csv`

## Features

- Student / Staff / Parent signup with passport, class, DOB, etc.
- Admin approval (visible from any device when server is running)
- CBT, CA marks, attendance, report sheets, gallery
- Only one admin
