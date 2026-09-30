# Privacy Policy for AI Health Coach

**Effective date:** September 30, 2026

AI Health Coach is a personal, educational application that demonstrates how a user can connect a WHOOP account and view a small wellness snapshot. This policy explains what information the application accesses and how it is handled.

## Information the application accesses

After you choose to connect your WHOOP account and approve the requested permissions, the application may read:

- Basic WHOOP profile information used to identify the authorized account.
- Recovery information, including recovery score, resting heart rate, heart-rate variability, blood oxygen percentage, and skin temperature when available.
- Physiological cycle information, including strain and heart-rate summaries.
- Sleep information, including sleep performance, consistency, efficiency, and respiratory rate when available.
- OAuth access and refresh tokens required to make authorized requests to WHOOP.

The application requests the `read:profile`, `read:recovery`, `read:cycles`, `read:sleep`, and `offline` scopes. It does not request permission to modify WHOOP data.

## How the information is used

WHOOP information is used only to retrieve and display the connected user's latest recovery, cycle, and sleep snapshot inside AI Health Coach.

WHOOP information is not currently included in prompts sent to Gemini or any other generative AI provider. It is not used for advertising, sold, or shared with data brokers.

## Storage and retention

The current application does not use a database for WHOOP information. OAuth tokens are held in the Spring Boot application's process memory so the application can make authorized WHOOP requests and refresh expired access tokens. Restarting the backend clears this in-memory state.

The displayed wellness snapshot is held only in the current API response and the browser application's memory. The application does not intentionally write the snapshot to persistent storage or logs.

## Services involved

The application communicates with WHOOP's OAuth and Developer APIs to complete authorization and retrieve the information described above. WHOOP handles information according to its own privacy policies and terms.

The AI Health Coach nutrition feature separately communicates with Gemini, but the WHOOP snapshot is not sent to Gemini in the current version.

## Your choices

Connecting WHOOP is optional. You can revoke the application's access through your WHOOP account's connected-app or integration settings. You can also stop and restart the local AI Health Coach backend to clear its in-memory token state. After WHOOP access is revoked, the application can no longer retrieve new WHOOP information unless you authorize it again.

## Security

The WHOOP client secret is used only by the Spring Boot backend. OAuth tokens and client credentials are not intentionally exposed to the Angular frontend or committed to source control.

## Medical disclaimer

AI Health Coach is an educational project. It does not provide medical advice, diagnosis, or treatment. Consult a qualified healthcare professional for medical questions.

## Changes to this policy

This policy may be updated when the application's data collection, storage, sharing, or functionality changes. The effective date above will be updated when material changes are made.

## Contact

For privacy questions, open an issue in the [AI Health Coach Privacy repository](https://github.com/amulyakurapati2-sys/ai-health-coach-privacy/issues).
