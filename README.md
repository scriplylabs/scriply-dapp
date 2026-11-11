# scriply-dapp

Scriply's hosted build of the receivables pool app. The app itself, a static site that lists every pool on chain and lets anyone lend, borrow, repay and keep, is open source in [scriply-programs](https://github.com/scriplylabs/scriply-programs/tree/main/app); this repo holds no app code, only which version is hosted and what it talks to.

Live at <https://scriplylabs.github.io/scriply-dapp/>, on Solana devnet.

## Deploying

`.github/workflows/deploy.yml` builds `app/` from scriply-programs at `PROGRAMS_REF`, runs its tests, and publishes `dist/` to GitHub Pages on every push to `main`.

- **A newer app:** set `PROGRAMS_REF` to a scriply-programs commit on `main`, in a PR.
- **Other settings:** `VITE_NETWORK`, `VITE_RPC_URL` and `VITE_SNAPSHOT_API_URL` are in the workflow's `env` (what each means is in the app's README). None is secret.
