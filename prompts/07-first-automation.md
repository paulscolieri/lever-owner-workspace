# 07. Build your first automation

Goal: take a mapped process and automate its mechanical steps. Do this after the process is mapped (prompt 04).

## Connect a tool

```
I want to connect [your CRM / calendar / accounting software] so you can read [jobs / customers / invoices].
1. Look up whether it has an API and what it can read and write.
2. Tell me exactly what key or login I need to create, and where to put it in .env.
3. Write a small read-only script in execution/ that pulls [the next 10 jobs] so we can confirm it works.
Read-only for now. Don't write or send anything to the system yet.
```

## Turn a mapped process into a workflow

```
Read knowledge/processes/[file].md, especially the Future state section.
Build the workflow:
- an SOP in directives/ using directives/_template.md
- scripts in execution/ for every step marked AUTO (reuse existing scripts first)
- AI DRAFT steps produce drafts for a person to approve. Nothing goes out to a customer or vendor automatically.
Show me the plan before you write code. Then run it on [3 real examples] and show me the output.
```

## Put it on a schedule

```
Run the [workflow name] workflow every [weekday at 7am] and send me a summary by [email / Slack]. Set it up, tell me how to check it's running, and how to turn it off.
```

## Example: tomorrow's jobs

```
Write a script that reads tomorrow's jobs from my calendar and lists, for each one: the time, the customer, the address, and what's being done. Then cross-check each job against knowledge/services/ and flag anything that needs a special material or a second person. Read-only.
```

Run it twice. Same output both times. That's the point of a script.
