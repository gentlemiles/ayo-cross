## 2023-10-27 - Cross-Site Scripting (XSS) in innerHTML Rendering
**Vulnerability:** Unsanitized user inputs (Leaderboard names/avatars) and API responses (Game Level Clues) were directly injected into the DOM using `innerHTML` in `ayocross.html`.
**Learning:** Vanilla JavaScript applications that rely heavily on string concatenation and `innerHTML` for rendering are highly susceptible to XSS.
**Prevention:** Always use a helper function like `escapeHTML` to sanitize any dynamic data before using `innerHTML`, or prefer using `textContent` for text-only updates.
