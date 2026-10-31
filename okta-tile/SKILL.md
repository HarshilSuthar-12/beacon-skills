---
name: okta-tile
description: Use when a ticket is about an application tile on the single sign-on dashboard — a tile that is missing, a tile that should be removed, or an app the user expects to launch from SSO but cannot see.
---

# SSO dashboard tiles

Tiles look like a user-interface problem and are almost never one. **A tile is
a view of group membership.** The tile is missing because the user is not in
the group that assigns the application. Fix the membership and the tile
appears; nothing is ever fixed by editing the dashboard.

## The resolution

1. Identify the application precisely. Users name tiles by what they call the
   product, which often differs from the application's name in the identity
   provider.
2. Find the group that assigns that application. Directory group membership
   usually drives identity-provider group membership, which drives app
   assignment — so the change is normally made in the directory, upstream of
   where the symptom shows.
3. Confirm the user should have the application. This is an access request
   wearing different clothes: role-default access needs no new approval, and
   anything else needs the manager or the app owner.
4. Add the user to the backing group.
5. Tell the user to sign out and back in, and give the sync delay. The tile
   does not appear instantly, and a refresh will not force it.

## Removals

Tile removal requests usually mean one of three things:

- the user left the role that justified the access — treat as an entitlement
  removal and check whether other access from the same role should also go
- the tile is for a decommissioned product — the fix is the app assignment, not
  one user's view
- clutter — the user wants it hidden, not revoked. Hiding is a user preference;
  revoking removes real access. Confirm which they mean before proposing.

## Traps

- **Fixing it in the wrong system.** Assigning the app directly in the identity
  provider, bypassing the directory group, drifts from source and is reverted
  at the next sync. Make the change where the membership originates.
- **The app is assigned but the licence is not.** The tile appears, the launch
  fails. If the product needs a seat, check the seat.
- **Wrong environment.** Products with separate production and non-production
  instances have separate tiles and separate groups. Confirm which the user
  needs — the request rarely says.
- **Stale cache.** A user who has not signed out since the change will report
  failure. Confirm they have re-authenticated before investigating further.
- **Expecting SSO where there is none.** Not every application is behind SSO.
  If it is not integrated, no group membership will produce a tile, and the
  answer is the direct URL and its own credential path.

## Propose, do not act

Group membership is a write action and carries real access. Name the group, the
application it assigns, and the basis for entitlement in the proposal.
