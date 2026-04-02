# CredoConnect (HTML Demo)

`credoconnect.html` is a single-file, front-end demo of an influencer marketing marketplace. It includes a landing page, sign-in/sign-up, a role-based dashboard (brand/influencer/admin), an AI matching view, a wallet/payments view, and a “smart contracts” flow.

## How to run

1. Double-click `credoconnect.html` (or open it in your browser).
2. Use one of the built-in demo accounts to sign in:
   - Brand: `brand@novatech.com` / `password123`
   - Influencer: `influencer@example.com` / `password123`
   - Admin: `admin@credoconnect.com` / `admin123`
3. Explore sections from the left sidebar after login.

No build step, server, or dependencies are required (everything runs from inside the HTML file).

## Important: MetaMask / “on-chain” behavior is simulated

This is a UI/demo. It does **not** actually connect to MetaMask or deploy real smart contracts.

What’s mocked in `credoconnect.html`:

- `connectMetaMask()` just simulates “connecting” by setting a fixed demo wallet address and an in-memory balance.
- Campaign “deploy” creates a **random** `contractAddr` string and updates in-memory campaign state.
- “Approve deliverable & release payment” updates in-memory balances/transactions and marks the campaign completed.
- Refreshing the page resets all demo state (no persistence).

## Demo wallet and token numbers

- Demo wallet address: `0x4f3cA8b2D1e0c7F5a9bE3d8c2F1a4e6b7d0C9E1`
- Demo CREDO balance starts at: `2450`
- Conversion rate shown in the redeem modal: `1 CREDO = $0.10`
- Redemption fee shown: `2.5%`
- Campaign platform fee shown: `5%` (payout shown as `95%`)

## Dashboard sections

After login, you’ll see a role-based dashboard with these sections:

- `Overview`: campaign metrics, active/pending campaigns, and AI recommendations.
- `Campaigns`: list + actions per campaign status (match/invite/sign/deploy).
- `Influencer marketplace`: browse influencers and invite them to campaigns.
- `AI Matching`: run a recommendation model and rank top influencers based on engagement, niche match, tier preference, and success rate.
- `Payments`: view demo transaction history; deposit and redeem update in-memory balances.
- `Smart contracts`: view contract/campaign lifecycle; approve deliverables to release payment (simulated).
- `Analytics`: charts + ROI table and an “Export CSV” button (static demo CSV).
- `Your profile`: edit profile fields (demo); shows the demo wallet address.
- `Admin panel`: approve/reject pending influencer applications (demo) and adjust platform settings (demo).

## Security note

Login is fully client-side and uses demo credentials stored in the HTML file, so do not treat this as a real authentication system.

