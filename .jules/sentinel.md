## 2025-06-12 - Inline JS XSS and Syntax Error Prevention
**Vulnerability:** XSS and JS syntax errors from injecting HTML-escaped strings directly into inline `onclick` handlers (e.g., `onclick="storeBuyTheme('${escapeHTML(name)}')"`).
**Learning:** Browsers decode HTML entities *before* parsing inline JavaScript. Thus, an HTML-escaped apostrophe (`&#39;`) reverts to an apostrophe, breaking the JS string and opening up XSS or syntax errors.
**Prevention:** Always use `data-*` attributes to pass dynamically escaped string data to inline JS handlers (e.g., `data-name="${escapeHTML(name)}" onclick="storeBuyTheme(this.dataset.name)"`).
