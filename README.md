# Nike Member Community: prototype

Single-page, no-dependency HTML prototype of a brand community on a self-service help site. All Nike content is illustrative. Not an official Nike site, policy or support answers.

## Run it
The help site embeds the community in an iframe, so serve the folder over HTTP:

```bash
python3 -m http.server 8765
```

Open http://localhost:8765/nike-help-site.html

## Files
- `nike-help-site.html`: two tabs. Use case 1 arrives from ChatGPT, use case 2 arrives from the website help article.
- `nike-community.html`: the community. Works standalone, or embedded with `?embed=1&src=chatgpt|website`.
- `nike-community-demo-script.md`: walkthrough, what is simulated, and how to embed it in a customer's branding.

State is stored in the browser (localStorage). Use "Restart both" to reset.
