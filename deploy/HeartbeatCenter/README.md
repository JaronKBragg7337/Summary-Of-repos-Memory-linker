# Deploy /HeartbeatCenter/ to heartbeatobservatory.com

Copy `index.html` from this folder to `HeartbeatCenter/index.html` on the `main`
branch of JaronKBragg7337/heartbeat-observatory. Vercel auto-deploys; the page
then lives at https://www.heartbeatobservatory.com/HeartbeatCenter/

The page is fully self-contained for that site: it reuses the three.js vendor
files already shipped at /3DPrinterAsset/vendor/ and fetches its repo manifest
at runtime from this repo's repos.json — so it always matches the GitHub data.

One-liner (from any machine with git):

    git clone --depth 1 https://github.com/JaronKBragg7337/heartbeat-observatory
    mkdir -p heartbeat-observatory/HeartbeatCenter
    curl -o heartbeat-observatory/HeartbeatCenter/index.html \
      https://raw.githubusercontent.com/JaronKBragg7337/Summary-Of-repos-Memory-linker/main/deploy/HeartbeatCenter/index.html
    cd heartbeat-observatory && git add . && git commit -m "Add /HeartbeatCenter/" && git push
