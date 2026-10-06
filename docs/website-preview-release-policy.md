# Website preview and release policy

Confirmed by the owner on October 6, 2026.

## Account continuity

Continue Devoid Media website development using the current account. The previous private preview was created under a different ChatGPT account/workspace and is not accessible through the current Sites connection.

The existing website source, supplied photography, logo assets, fonts, and current edits are retained. This move creates a separate owner-private preview; it does not transfer ownership of the old Site or change the official website.

## Required release workflow

1. Build and validate changes from the Master Asset Library website source.
2. Publish changes to the separate private preview.
3. Have the owner review the preview.
4. Publish to the official website only after explicit owner approval of that release.

A request to develop or update the preview is not approval to publish to the official website. Do not automatically promote preview changes.

## Site configurations

- Current private preview: `.openai/hosting.json` inside `website/`.
- Previous account preview: `website/.openai/previous-account-hosting.json`, retained for historical reference.
- Official website: `website/.openai/production-hosting.json`, preserved separately.

The previous preview URL was <https://devoid-media-private-preview.em-devoid.chatgpt.site/>. The current account's preview is registered at <https://devoid-media-studio-preview.emdevoid.chatgpt.site/>; successful publication must be verified before treating it as live.

The official website is <https://devoidmediallc.com>.

## Repository record

Keep website source, preview configuration, release policy, and verified publication details in this GitHub repository. Do not commit credentials or local environment secrets.
