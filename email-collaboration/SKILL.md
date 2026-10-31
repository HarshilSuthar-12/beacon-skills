---
name: email-collaboration
description: Use for mail and collaboration tickets — distribution list changes, shared mailbox access, mail not arriving, quarantined messages, Teams and team-site membership, calendar and delegate permissions.
---

# Mail and collaboration

Two different jobs arrive under the same heading: **membership changes**, which
are access requests with a resource owner, and **mail flow faults**, which are
diagnosis. Decide which one you are looking at before doing anything.

## Membership changes

Distribution lists, shared mailboxes, team sites and Teams channels all have an
**owner**, and the owner approves — not the requester's manager, unless they
are the same person.

1. Identify the list or resource precisely. Display names collide; resolve to
   the unique address or identifier before changing anything.
2. Find the owner. If the resource has no owner, that is the finding — propose
   assigning one rather than quietly making the change.
3. Get the owner's approval on the ticket.
4. Make the membership change at the group, not in anyone's client.
5. Say when it will take effect. Mail group changes propagate on a delay.

Removals deserve the same care as additions. Removing someone from a list they
need silently breaks their visibility into something.

## Mail flow faults

Work from the evidence, not the complaint. "I didn't get the email" has several
distinct causes and they need different fixes:

- **Quarantined.** The message was filtered. Check quarantine before anything
  else — this is the most common cause and resolving it is release-and-explain.
  If the sender is legitimate and recurring, propose a policy change rather
  than releasing the same message weekly.
- **Not sent.** Confirm it actually left the sender. A missing message often
  never existed.
- **Group membership.** Mail to a list reaches only current members. Check
  whether the complainant was a member at the time it was sent.
- **Rules and forwarding.** Client-side rules file messages invisibly.
- **Delivery failure.** A bounce has a reason code; read it rather than
  guessing.

Before declaring delivery lost, establish that the message exists, who it was
addressed to, and when.

## Shared mailboxes and delegates

Shared mailbox access requests are common after someone leaves. Grant at the
mailbox, specify the permission level deliberately — read, send-as and
send-on-behalf are different grants with different audit implications — and
state which was given.

Send-as is impersonation. It needs a clear reason and the owner's approval.

## Traps

- **Quarantine release as a habit.** Releasing the same sender repeatedly
  means the filter policy is wrong. Fix the policy.
- **Ambiguous list names.** Near-identical names mean a change can land on the
  wrong list. Confirm the address, not the display name.
- **External recipients.** Adding externals to an internal list leaks internal
  traffic outside. Treat it as a security decision.
- **Calendar permissions.** Often requested as "access to the mailbox" when the
  need is calendar visibility only. Grant the narrower one.

## Propose, do not act

Membership changes and permission grants are write actions. Name the exact
resource, the permission level and the approving owner in the proposal.
