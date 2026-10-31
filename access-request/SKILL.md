---
name: access-request
description: Use when a ticket asks for access to an application, security group, site, licence or shared resource — including "I need access to X", "add me to Y", "licence request", and app tiles that are missing because of group membership.
---

# Access requests

The largest single class of tickets. Almost all of them resolve the same way:
**access is granted by group membership, not by touching the application.**
Find the group that backs the entitlement, confirm the requester is allowed to
have it, add them, confirm propagation.

## What the resolution almost always is

1. Identify the entitlement actually being asked for. The ticket names an app;
   what grants it is a directory security group or an identity-provider group.
2. Check whether the requester already has it. A surprising share of these are
   already-granted entitlements that failed to propagate, or the user looking
   in the wrong place.
3. Confirm authorisation. For anything beyond default-for-role access, the
   line manager or the resource owner approves — not the requester.
4. Add the user to the backing group.
5. Tell the requester where the access appears and how long propagation takes.
   Sync is not instant; most "it still doesn't work" follow-ups are impatience,
   not failure.

## Deciding whether it needs approval

Ask for approval when any of these is true:

- the entitlement is not standard for the requester's role or department
- it grants write, admin or financial capability
- it is a paid licence with a per-seat cost
- the resource has a named owner (distribution lists, team sites, shared drives)

Default-for-role access that the requester's peers already have does not need
a fresh approval; cite what makes it default when you propose it.

The approver is the **line manager** for role-based access and the **resource
owner** for owned resources. Do not accept the requester's own assertion that
they are approved — the approval has to be visible on the ticket.

## Propose, do not act

Granting access is a write action. Put the proposal in front of a human with:

- the exact group to add the user to
- the evidence that they should have it (role, manager approval, peer precedent)
- what the access lets them do
- the cost, if it is a paid licence

## Traps

- **The app is not the entitlement.** Adding someone directly in the
  application drifts from the directory and gets reverted at the next sync.
  Always go through the backing group.
- **Licence exhaustion.** Paid-seat products fail silently when the pool is
  empty. Check available seats before promising access.
- **Leavers.** Cross-check that the requester is still active before granting.
  An access request that arrives near someone's departure date is a red flag.
- **Access for someone else.** When the requester asks on behalf of a third
  party, the approval must come from that person's manager, not the requester's.
- **Over-granting.** Tickets often ask for a broad role when a narrow group
  does the job. Propose the narrowest entitlement that satisfies the request.

## Closing

Say which group was added, where the access shows up, and the expected
propagation delay. If the request was partially granted, say explicitly what
was not granted and why.
