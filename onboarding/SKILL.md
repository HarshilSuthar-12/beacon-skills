---
name: onboarding
description: Use for new employee and new contractor setup — account creation, day-one access, device and virtual desktop provisioning, start-date changes, and "new hire" tickets raised from the HR system.
---

# Onboarding

Onboarding tickets are mostly generated from the HR system rather than typed by
a person, so they arrive in a predictable shape and resolve as a checklist. The
judgment is in the exceptions: contractors, early start dates, and non-standard
role access.

## The standard sequence

1. **Confirm the start date and the record.** The HR feed is the source of
   truth for start date, legal name, job title, manager and employment type.
   Where the ticket text and the HR record disagree, the record wins.
2. **Create the directory account** in the correct domain and the correct
   organisational unit. Employees and contractors do not share an OU, and the
   OU drives what the user inherits.
3. **Set the initial credential** with forced change at first logon. Never
   leave a static initial password in a ticket comment the requester can read
   later — send it through whatever channel policy specifies, to the manager.
4. **Apply role-based groups.** Standard groups for the department and role,
   then any extras the ticket names. Extras beyond the role default need the
   manager's approval like any other access request.
5. **Provision the workspace** — virtual desktop or physical device, endpoint
   security agent, and the productivity suite.
6. **Mail and collaboration** — mailbox, department distribution lists, team
   sites.
7. **Confirm to the manager** before the start date, listing what exists and
   anything still outstanding.

## Contractors differ

Contractors go in a separate organisational unit and carry an **expiry date**.
That expiry is the control that makes offboarding automatic; a contractor
account created without one becomes an orphan.

Contractors typically get a narrower default group set than employees. Do not
copy an employee template onto a contractor.

## Timing

These tickets are deadline-driven in a way most are not: the work is worthless
if it lands after the person's first morning. Treat start date as a hard due
date, and flag anything that cannot be completed before it rather than
discovering it on the day.

Start dates move frequently. A changed start date on an existing onboarding is
an update to the existing ticket, not a new build.

## Traps

- **Duplicate accounts.** Re-hires and name changes produce a second account
  for an existing person. Search the directory for the person before creating.
- **Name mismatch.** Preferred name, legal name and the name on the HR record
  often differ. The directory account follows the convention policy sets; the
  display name follows the preferred name.
- **Day-one access that needs approval.** If the role needs an entitlement that
  requires sign-off, start that approval immediately — it is the step most
  likely to miss the start date.
- **Silent licence failure.** Productivity and collaboration licences fail
  quietly when the pool is exhausted, leaving an account that looks complete
  but cannot send mail.

## Propose, do not act

Account creation, group membership and licence assignment are all write
actions. Propose the full set as one package so the reviewer approves a
coherent day-one state, not six disconnected changes.
