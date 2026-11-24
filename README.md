# Wordle Word Lists

## What is this?
This is an automatically updated repository containing two JSON word lists for the NYT Wordle:

- **`answer-pool.json`** — The curated list of possible daily Wordle answers.
- **`valid-guesses.json`** — The complete list of valid 5-letter words accepted as guesses.
- **`daily_YYYY-MM-DD.json`** - The daily word from NYT Wordle

## Usage
You can fetch the latest lists directly in your project using GitHub's raw file URLs:

```javascript
const answers = await fetch("https://cdn.jsdelivr.net/gh/JeremyKGalownia/Wordle-Word-List@main/answer-pool.json").then(res => res.json());
const guesses = await fetch("https://cdn.jsdelivr.net/gh/JeremyKGalownia/Wordle-Word-List@main/valid-guesses.json").then(res => res.json());
const daily = await fetch(`https://cdn.jsdelivr.net/gh/JeremyKGalownia/Wordle-Word-List@main/daily_${DATE}.json`).then(res => res.json());
```

## Updates
The lists are automatically checked and updated weekly via GitHub Actions.
The daily is automatically checked and updated daily via GitHub Actions.
