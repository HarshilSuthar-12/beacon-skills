---
name: offboarding
description: Use for leavers, terminations, contract end and "off board" tickets — disabling accounts, converting and delegating mailboxes, reclaiming licences and devices, and removing group membership.
---

# Offboarding

The highest-risk category in the queue. Getting it wrong leaves an active
account for someone who has left, or destroys data the business still needs.
Both failures are expensive, and they pull in opposite directions — which is
why the standard is *disable and retain*, never delete.

## The standard sequence

1. **Confirm the departure is real and dated.** Source it from the HR record,
   not from a chat message. Note whether it is a standard resignation, a
   contract expiry, or an involuntary termination — the third is time-critical
   and usually coordinated with HR for a precise cut-off time.
2. **Disable, do not delete.** Disable the directory account and revoke active
   sessions and tokens. Deletion destroys the audit trail and any data still
   attached to the identity.
3. **Revoke sessions explicitly.** A disabled account can keep working until
   issued tokens expire. Sign the user out everywhere rather than assuming the
   disable took effect immediately.
4. **Handle the mailbox.** Convert to a shared mailbox and grant the manager or
   named successor delegate access. This is the single most requested follow-up
   on leaver tickets — doing it up front prevents a second ticket in a week.
5. **Remove group memberships and entitlements**, including anything that costs
   per seat.
6. **Reclaim licences** so the seats return to the pool.
7. **Reclaim the workspace** — decommission the virtual desktop, recover the
   physical device.
8. **Confirm back to the manager** with what was disabled, what was retained
   and where the retained data now lives.

## Timing is the whole game

For involuntary terminations, the account must be disabled at the time HR
specifies — not before (the person may still be in the meeting) and not after
(they still have access). Confirm the exact cut-off and treat it as the
deadline.

For contract expiry, the expiry date set at onboarding should do this
automatically. A contractor ticket arriving manually usually means the expiry
was never set — worth flagging as a gap, not just resolving.

## What must never be done without explicit sign-off

- deleting an account, mailbox or home directory
- removing data that is not demonstrably duplicated elsewhere
- disabling an account before the HR-specified time

Retention has a policy period. Propose disable-and-retain, and let the deletion
happen on the policy clock rather than on ticket close.

## Traps

- **Shared and service accounts.** A leaver is often the owner or the only
  credential holder for a shared mailbox, service account or integration.
  Disabling without transferring ownership breaks a system nobody notices until
  it fails. Check what the identity owns before disabling it.
- **Delegated access the leaver granted.** Access they gave others may be
  attached to their identity and disappear with it.
- **Mail flow.** Decide forwarding or auto-reply deliberately — external
  correspondents will keep writing to the address for months.
- **Partial leavers.** Internal transfers arrive worded like departures. A
  transfer is a group change, not a disable.

## Propose, do not act

Every step is destructive or near-destructive. Propose the sequence with the
cut-off time stated, and make the retention decision explicit in the proposal
so approval covers it.
