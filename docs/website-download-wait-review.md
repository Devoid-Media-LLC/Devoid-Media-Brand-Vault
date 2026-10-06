# Website review during download recovery

Reviewed October 6, 2026.

## Scope and evidence

Source review of GitHub baseline commit `7a38888aa6378b3665b5eedeaf30332208c82f5a`, covering the homepage, Socials directory, collaboration forms, and inquiry handler. The existing local Socials and test edits are not covered by this baseline review. Current Sites runtime settings for private project `appgprj_6ac4d1e21b308191a9cd4d8abcc2e8f1` were read: no environment entries, revision zero.

This is a source and configuration review, not a rendered visual review or a successful build, deployment, submission test, or external-profile verification.

## Confirmed findings

### Collaboration settings need migration

The new preview has no hosted environment entries. The inquiry handler requires `RESEND_API_KEY`, `TURNSTILE_SITE_KEY`, and `TURNSTILE_SECRET_KEY`. Without these, the configuration/submission endpoints return service-unavailable responses. Preserve the existing provider setup; do not invent credentials or create replacement services merely because the account changed.

The sending address in the source is `forms@info.devoidmediallc.com`. Confirm its existing sending-domain verification when restoring mail delivery. The Turnstile widget must permit the new preview hostname. Never commit secret values or ask for plaintext credentials in a public issue.

### Professional inquiry routing needs confirmation

Creator submissions go to `collabs@devoidmediallc.com`. All professional form submissions, including press inquiries, go to `info@devoidmediallc.com`. The visible page separately lists `partnerships@devoidmediallc.com` for business and `press@devoidmediallc.com` for press. These may be intentional; confirm the intended routing before changing it.

### Unavailable-verification experience can be clearer

If form configuration is absent, the page tells the visitor to refresh and retry, while the verification component can continue showing a loading message. Refreshing cannot repair missing hosted settings. A scoped follow-up can make the unavailable state explicit and direct visitors to the page's existing email links. Keep the two inquiry paths and existing visual design.

### Keyboard interactions need rendered testing

The homepage entrance uses a modal role, but the reviewed source does not implement focus containment or make the background inert. The mobile navigation buttons expand a menu, but the reviewed source does not implement Escape dismissal. The collaboration inquiry controls use tab roles without the usual tab keyboard handling. Verify actual browser behavior before declaring accessibility complete; preserve the current appearance when making corrections.

## Existing content to preserve

- Approved logo structure, custom font hierarchy, and supplied photography.
- The homepage's established headline and philosophy.
- Both creator and professional collaboration paths.
- Existing Socials destinations and friend links until the owner requests changes.
- Separate private preview and official-site configuration.

Social URLs were inventoried from source only. No active-profile ownership, availability, or live link behavior was verified.

## Next sequence

1. Finish local file downloads and reconcile the remote migration record with local staged changes without discarding work.
2. Complete the build and existing rendered-HTML checks, then deploy the separate private preview.
3. Restore the existing email and Turnstile settings securely and confirm the preview hostname is permitted.
4. Verify both inquiry paths and the unavailable-service states. Use an explicitly authorized test before sending any email.
5. Review Socials at desktop, tablet, and narrow-mobile widths using the preserved local edits.
6. Address keyboard behavior and clear form status messages through scoped changes.
7. Obtain explicit owner approval before publishing an official release.
