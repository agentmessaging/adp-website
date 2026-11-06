# ADP website

Source for [agentdevices.org](https://agentdevices.org), the website of the Agent Device Protocol (ADP).

The site is one static page, `index.html` (Tailwind from its CDN, no build step, no analytics): what ADP is, the idea, the rules, roles, how a request works, capabilities, the spec documents, implementations, status and the protocol family. Next to it are `404.html`, `robots.txt`, `sitemap.xml`, `site.webmanifest`, `llms.txt`, `humans.txt` and `.well-known/security.txt`.

## Deployment

GitHub Pages serves the `main` branch from the repository root (Settings > Pages: deploy from a branch, `main`, `/`), the same setup as the sibling sites. `CNAME` holds the custom domain, `agentdevices.org` (DNS at Cloudflare). `.nojekyll` turns off Jekyll, which would otherwise drop `.well-known/`. Every push to `main` redeploys the site.

## Editing

Edit the files directly and open a pull request. To preview, serve the folder locally, for example `python3 -m http.server`, and open http://localhost:8000.

The page describes the protocol; it must match the specification. When the spec changes, update `index.html` and `llms.txt` together, and bump `<lastmod>` in `sitemap.xml`.

## Specification

The protocol specification, SDK, Linux bridge and reference controller live at [agentmessaging/agent-device-protocol](https://github.com/agentmessaging/agent-device-protocol) (v1, experimental).

## Related

- [AMP](https://agentmessaging.org): Agent Messaging Protocol
- [AID](https://agentids.org): Agent Identity Protocol
- [AAP](https://agentactions.org): Agent Actions Protocol
- [AFP](https://agentfiles.org): Agent Files Protocol
- [AI Maestro](https://aimaestro.sh): implementing the controller role

## License

MIT.
