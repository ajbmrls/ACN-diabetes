# Know Your Diabetes

Four-game diabetes quiz for World Diabetes Day (November 14), in REBEL branding.
One self-contained file: `index.html`. No build step, no dependencies. Fonts load from Google Fonts.

## Deploy on GitHub Pages

1. Create a repository and upload `index.html` to the root.
2. Go to Settings > Pages.
3. Under Build and deployment, choose "Deploy from a branch", pick `main` and `/ (root)`, then Save.
4. Wait a minute. The site appears at `https://<user>.github.io/<repo>/`.

## Saving results to Google Sheets (not connected yet)

`index.html` has a line near the bottom of the file:

    var CONFIG = { endpoint: "" };

While it is empty, the page runs in preview mode: nothing is sent, and the thank-you screen says so.
Paste a Google Apps Script web app URL there to start saving. The page sends two kinds of rows:

- `type: "result"`: sessionId, score, label, points, crowdGuess, insulinYearGuess, submittedAt. No name or email.
- `type: "raffle"`: name, email, submittedAt. No score or session id, so entries can't be matched to answers.

## Before launch

- GitHub Pages sites are public. Anyone with the link can open it, and the raffle form collects names and emails. Check your client's data policy first.
- Get a clinical review of the answers, especially the 1922 insulin date and the "honey-sweet" meaning of mellitus.
- The "Test your type 2 diabetes risk" link goes to worlddiabetesday.org. Swap in a direct test page if you have one.
- The purple accent color is a placeholder. Change `--accent` in the CSS to match final brand colors.
