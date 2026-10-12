# Privacy

*Trimm Studio, by 24HourLifestyle LLC. Last updated: October 2026.*

Trimm Studio is built so your footage stays on your computer. This page lists what stays, what can leave, and who
receives it when it does.

## In short

* **No account, no tracking.** Trimm has no sign-up, no analytics, no advertising and no crash reporting. It does not
  send usage data to us.
* **Your videos are processed on your computer.** Importing, analysis, editing and rendering all happen locally.
* **Data leaves only when you choose a service that needs it**, and only to that service. Each case is listed below.
* **Your API keys are kept in the Windows credential store** and are never written to settings, logs or exports.

## What stays on your computer

* Your videos, clips, exports, transcripts, projects and settings.
* Your API keys and connected-account tokens (in the operating system's credential store).
* Logs and diagnostics. Logs hide keys and tokens automatically and are never sent anywhere. A diagnostics file is
  created only if you export one, and you decide whether to share it.

Trimm stores its data in a folder on your computer. **Settings, then Storage** shows where it is. In portable mode
everything lives in the `ClipForgeData` folder next to the app.

## When data can leave your computer

| You do this | What is sent | Who gets it |
|---|---|---|
| Paste a link to import a video | The link, and a normal request for the video | The site that hosts it (for example YouTube or Twitch), like any browser or download tool |
| Use an AI model you added for highlights, hooks, titles or descriptions | Transcript text and your instructions | The AI provider you chose |
| Use AI to write a voice-over script | A few still frames from the clip, and the clip's transcript | The vision model provider you chose |
| Use a cloud voice | The narration text | The provider you chose |
| Use a model on your own computer (such as Ollama or LM Studio) | Nothing leaves your computer | No one |
| Install offline transcription or a local voice | A download request | Python's package index (PyPI) and Hugging Face, which host those files |
| Transcribe offline for the first time | A one-time download of the speech model (about 145 MB) | Hugging Face |
| Publish to YouTube, TikTok or Instagram | The clip and its title, description and tags, after you confirm | The platform you connected |
| Open the Browse window | Normal web requests, as in any browser | The sites you visit |
| Press "Check for updates" | A request to an update address, but only if one is configured in your copy | That address |

**Local-only mode** (Settings, then Privacy) blocks cloud AI providers and cloud voices, add-on and voice downloads,
channel checks and update checks. Two things still reach the internet because that is their purpose: importing a link
contacts the site that hosts the video, and publishing contacts the platform you chose. The speech model for offline
transcription downloads once on first use, so run a first transcription before you rely on it fully offline.

## AI providers have their own policies

When you use a provider, its privacy policy and terms apply to what you send it, including how long it keeps it and
whether it uses it to train models. We do not control that. Read your provider's policy, and use a local model if you
need the content to stay private.

## Browser data

The Browse window is a normal web view. Websites you open there can set cookies and store data, and they stay in
Trimm's own profile folder, separate from your other browsers. Clear them by deleting that folder.

## Deleting your data

Uninstalling Trimm removes the program. Your projects and settings are in the data folder, which you can delete
yourself. API keys can be removed in AI & Models before you uninstall, or in the Windows credential store.

## Children

Trimm Studio is not directed at children under 13 and does not knowingly collect information from them. It collects
no personal information at all.

## Contact and changes

Use this repository's **Issues** page for privacy questions. Do not post keys, passwords or private videos there. We
may update this page. The date at the top shows the latest version.
