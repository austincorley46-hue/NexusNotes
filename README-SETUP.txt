NEXUS NOTES — INTERACTIVE CHATGPT TUTOR

WHAT IS NEW
- A full conversational Tutor page in the existing premium Nexus Notes.
- Start new chats and return to previous chats, saved in THIS browser only.
- Subjects: math, science, English, history, coding, general.
- Tutor styles: step-by-step teaching, quizzes, hints, review.
- Optional notebook notes for context (ONLY sent when you choose one).
- Speak questions using browser microphone dictation (if browser supports it).
- Hear replies using built-in browser speech synthesis. This is NOT Siri or live call audio.
- Chat UI is complete, but LIVE AI RESPONSES require the following secure setup.

IMPORTANT: SECURITY AND COST
- DO NOT put an OpenAI API key into GitHub, index.html, or a browser field.
- ChatGPT subscription and OpenAI API are different products. API may incur charges.
- This is a personal demo, not production-grade authentication. Restrict access using
  a long unpredictable TUTOR_ACCESS_TOKEN. Use provider rate limiting and OpenAI spend caps.
- Chat history stays in browser storage. Selected notebook excerpts are sent to your
  Worker and OpenAI when you press Send. Avoid sensitive personal information.
- If you're under 18, ask a parent or guardian to help with any billed API account.

SET UP REAL AI ANSWERS
1. Keep your current Nexus Notes data safe: use Settings > Download backup (.json)
   before switching to another browser address or a new file.
2. Upload ONLY index.html to your GitHub NexusNotes repository, replacing the old
   index.html. Do not upload tutor-worker.js into a GitHub Pages public website.
3. Visit https://dash.cloudflare.com and open Workers & Pages.
4. Create a new Worker (or choose 'Start with Hello World'). Name it nexus-notes-tutor.
5. Open its code editor, replace its code with tutor-worker.js, and deploy.
6. In Worker Settings > Variables and Secrets, ADD TWO SECRET VARIABLES:
      OPENAI_API_KEY        = your OpenAI API key
      TUTOR_ACCESS_TOKEN   = a random secret string of 32+ characters
   Keep both secrets private; neither belongs in your website code.
   OpenAI API keys are managed at https://platform.openai.com/api-keys
7. Return to your Worker and copy its https://...workers.dev URL.
8. Open https://austincorley46-hue.github.io/NexusNotes/ in Chrome.
9. Open ChatGPT Tutor > AI CONNECTION. Paste the Worker URL and your private access
   code (NOT your API key), then click 'Save connection'.
10. Type a question and press Send. The AI should reply if secrets and API access
    are set correctly. The access code is kept in this browser tab/session only.

If you move Nexus Notes to a custom domain, update ALLOWED_ORIGINS in tutor-worker.js
with the new exact website origin, redeploy the Worker, then update its URL in the app.

VOICE
- Speak uses the browser microphone and speech recognition. Support varies.
- Voice on/off reads AI replies with an available system voice. This is not a live
  two-way voice call; it reads responses after they arrive.

BACKUP
The old notebooks, goals, tasks, and calendar localStorage keys remain unchanged.
New chats use nn_tutor_chats_v1 and are not included in the old backup exporter.
