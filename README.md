# Word of the Day — n8n Workflow

This n8n automation fetches a *Word of the Day* from a free dictionary API, enriches it with definitions and examples, and logs it in a Google Sheet.
## Features

- Retrieves a new word each day
- Gets the definition, part of speech, and an example sentence
- Logs everything to a Google Sheet for easy review
- Built without any email or third-party notification services (fully API + Google Sheets based)

## Tools Used

- [n8n](https://n8n.io/)
- [Free Dictionary API](https://dictionaryapi.dev/)
- Google Sheets (via Google Sheets node)

## Use Case

Ideal for:
- Language learners
- Teachers/tutors creating daily vocabulary exercises
- Teams building demo automations with useful, real-world APIs

## Google Sheet Setup

Before importing the workflow:

1. Create a Google Sheet with the following columns:
   - `Date`
   - `Word`
   - `PartOfSpeech`
   - `Definition`
   - `Example`

2. Name the sheet (e.g. `WordLog`) and connect it to n8n using Google Sheets credentials.

## Workflow Overview

1. **Cron Node** – Triggers the flow once a day.
2. **HTTP Request** – Fetches the Word of the Day from the Dictionary API.
3. **Code Node** – Extracts and formats relevant data.
4. **Google Sheets Node** – Appends a new row with the word and its definition.

## How to Use

1. Clone or download this repository.
2. Import `word-of-the-day-n8n-workflow.json` into your n8n instance.
3. Set up your Google Sheets credentials.
4. Adjust the Cron schedule to your preference.
5. Run it manually or let it run daily!

## Example Output

| Date       | Word     | PartOfSpeech | Definition                            | Example                        |
|------------|----------|---------------|----------------------------------------|--------------------------------|
| 2025-06-01 | ephemeral| adjective     | Lasting for a very short time          | Life is as ephemeral as a dew. |


