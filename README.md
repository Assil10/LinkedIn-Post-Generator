# LinkedIn Post Generator (Make.com / JSON Template) 🚀

This mini project is a Make.com automation template that generates a complete LinkedIn post using Gemini and publishes it to your LinkedIn feed. It reads a topic from Google Sheets, prompts Gemini to write a post (≤ 2,999 chars, with relevant emojis, no bold), and then posts to LinkedIn. ✍️🤖➡️🔗

## Demo 🎥
[Watch the demo (MP4)](assets/Demo.mp4)


https://github.com/user-attachments/assets/33b4d0ac-f358-47d2-a1c5-8e8f1e4fbbcb



<!-- GitHub sometimes sanitizes HTML; the raw URL helps inline playback. -->
<video src="https://raw.githubusercontent.com/Assil10/LinkedIn-Post-Generator/main/assets/Demo.mp4" controls width="720"></video>

## What’s included 📦
- `linkdin post generator (Assil).json` — the Make.com scenario JSON containing four steps:
  1) Function increment (run/execution/scenario counter) 🔢
  2) Google Sheets: filter one row matching the current counter 📄
  3) Gemini: generate the LinkedIn post from the sheet topic 🧠
  4) LinkedIn: publish the generated post 📣

## Prerequisites ✅
- Google account with access to the target Google Sheet
- LinkedIn account with API/app access (via Make.com LinkedIn connector)
- Gemini API access/connection (via Make.com)
- Make.com account with permission to import JSON scenarios

## Setup 🔧
1) Import the JSON scenario into Make.com.
2) Replace the placeholder connections in the scenario:
   - `GOOGLE_CONNECTION_PLACEHOLDER`
   - `GEMINI_API_PLACEHOLDER`
   - `LINKEDIN_CONNECTION_PLACEHOLDER`
3) Configure the Google Sheets module:
   - `spreadsheetId`: set to your Spreadsheet ID
   - `sheetId`: set to your sheet/tab name or ID
   - `tableFirstRow`: ensure header range covers your columns
   - The scenario expects the topic in column `B` (index `1` in the JSON mapper).
4) Verify the Gemini model (currently `gemini-2.0-flash`) and prompt settings.
5) Ensure the LinkedIn module targets the correct profile/org and visibility.

## Usage ▶️
- Add or maintain a topics list in your Google Sheet.
- Each run increments the counter and fetches the matching row.
- The generated post (from Gemini) is published directly to LinkedIn.

## Notes 📝
- Max post length is capped at 2,999 characters per LinkedIn’s limits.
- Update visibility, feed distribution, and reshare flags as needed.
- For a dry run, disable the LinkedIn step and log the generated content first.

## License 📄
MIT
