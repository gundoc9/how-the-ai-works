# How the AI you use works

A dictionary of the machine behind the chat box, written for clinicians. Twenty-four terms, one per card. Each card carries a picture that responds to a control, one analogy from theatre life, and the papers it rests on, with a note on how far each paper was checked.

Live at: https://gundoc9.github.io/how-the-ai-works/

## What the pictures are

- **Computed live**: the page trains a small language model in your browser when it opens, a byte-pair tokeniser and a count-based next-token model built from the text of the cards themselves. The token, next-token, temperature, sampling, context-window, embedding, hallucination and calibration pictures are drawn from it. The arithmetic is the real arithmetic, at toy scale.
- **Published formula**: the Parameters card draws equation 1.1 of Kaplan et al. (2020) with its published constants.
- **Simulation**: the Reinforcement learning and Sycophancy cards run a gradient-bandit learning rule on rewards the page sets. The learning is real; the rewards are invented to show it.
- **Diagram**: a drawn picture of a mechanism. Nothing in it is measured.

## Privacy

One page and one icon, nothing else fetched. Nothing you type leaves your phone. The only links are the arXiv pages of the sources, and they open only if tapped.

## Sources

See `SOURCES.md` for every paper, what each card claims from it, and how far it was checked. The same list is on the page under All sources.

## Corrections

If a card is wrong, open an issue naming the card and the claim. Corrections are made in the open and the version stamp on the About page changes.

## Building

The page is assembled from `engine.js`, `cards.js`, `app.js` and `styles.css` with fonts embedded, then checked at three phone widths for contrast, tap targets, overflow, text collisions and navigation inside a sandboxed frame. The build and the checks live with the author; the shipped files are `index.html`, `ai-icon-180.png` (home-screen icon and favicon) and `how-the-ai-works-card.png` (the link preview).

Dr Ganesh Sivasankara · MD · FRCA · FCARCSI · Consultant Anaesthetist
