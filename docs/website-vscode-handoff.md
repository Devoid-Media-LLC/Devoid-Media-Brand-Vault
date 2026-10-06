# Devoid Media website — VS Code handoff

Updated October 6, 2026.

## Authorized work

Continue the existing website using the current ChatGPT account. Create a separate private preview from existing local source, preserving the current design, photography, logos, fonts, and pending changes. Record this work in GitHub.

The owner requires all changes to be published to the private preview for review before any official release. Publishing to the official website requires explicit owner approval. See `website-preview-release-policy.md`.

## Working location

Repository: `/Users/earuich/Documents/GitHub/Devoid-Media-Brand-Vault-Master-Asset-Library`

Required repository branch: `Master-Asset-Library`, tracking `origin/Master-Asset-Library`. Website source: `website/`.

Synced ChatGPT project `sources/` files are read-only references.

## Account migration

The original private preview was under another account/workspace and the current connector returned project-not-found. The current account originally listed no editable Sites.

A new private Site was successfully registered under the current account:

- Project ID: `appgprj_6ac4d1e21b308191a9cd4d8abcc2e8f1`
- Expected preview URL: `https://devoid-media-studio-preview.emdevoid.chatgpt.site`
- Title: Devoid Media — Private Preview

Do not register another Site. Reuse this project ID from `website/.openai/hosting.json`.

The old manifest is preserved at `website/.openai/previous-account-hosting.json`. Official-site configuration at `website/.openai/production-hosting.json` was not edited.

## Current work state

The Sites source workflow opened the website directory and initialized dedicated source metadata at `website/.git`. Do not confuse this Sites source repository with the surrounding GitHub repository. Keep the GitHub Master-Asset-Library branch.

The publication workflow is building the site, then running `node --test tests/rendered-html.test.mjs`, saving source, and packaging an archive. At handoff, no successful deployment has been confirmed. Check the current chat's final update for any later completion.

Expected archive path: `/Users/earuich/.codex/visualizations/2026/09/30/01a0f291-bdc7-7d80-bb4d-c81481c56062/devoid-private-preview.tar.gz`.

Do not assume an archive exists or is valid. Reuse successful workflow results when available; otherwise use the Sites hosting workflow and obtain a fresh source credential for this same Site. Credentials were held only in session memory, never saved in files.

## Outstanding steps

1. Finish build and existing rendered-HTML checks; fix failures without redesigning the website.
2. Publish the new account's private Site and verify terminal deployment success.
3. Confirm the source and release-policy documents are committed and pushed to the GitHub Master-Asset-Library branch. Git status commands were slow in the current session; do not claim a successful push without verification.
4. Return a clickable private preview link.
5. Continue development after the owner chooses the next area; no new feature direction was selected yet.

## Existing local changes to preserve

Before migration, `.vscode/extensions.json`, `website/README.md`, `website/app/socials.css`, `website/app/socials/page.tsx`, and `website/tests/rendered-html.test.mjs` already had local modifications. Several untracked directories also existed. Do not discard these edits or indiscriminately stage unrelated files.

## Runtime

Bundled Node: `/Users/earuich/.cache/codex-runtimes/codex-primary-runtime/dependencies/node/bin/node`.

Sites plugin root: `/Users/earuich/.codex/plugins/cache/openai-curated-remote/sites/0.1.75`.

The existing pnpm dependencies were retained. Execution profile helper returned portable/configured=false, so existing scripts and configuration were preserved. Collaboration form delivery depends on hosted RESEND and Turnstile settings; previous-account secrets were not transferred.

## Final desktop handoff status

The build and GitHub recording attempts stalled on local file reads. The build was stopped before deployment, and the GitHub commit/push attempt was stopped without confirmed completion. No new private preview deployment was verified. The new Site registration and local documentation/configuration are saved. Inspect staged changes and Git history before retrying a commit or push. The official website was not published or edited.

Observed stalls included reads of supplied media during asset copying and an existing Git pack index during repository operations. This observation does not establish the cause; investigate local filesystem availability before retrying. Resume with the preserved source rather than registering another Site.
