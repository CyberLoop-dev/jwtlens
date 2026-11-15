<p align="center">
  <img src="assets/banner.svg" alt="jwtlens banner" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML-single%20file-fb923c?style=for-the-badge" alt="single file">
  <img src="https://img.shields.io/badge/dependencies-zero-ef4444?style=for-the-badge" alt="zero deps">
  <img src="https://img.shields.io/badge/100%25-local-22c55e?style=for-the-badge" alt="local">
  <img src="https://img.shields.io/badge/license-MIT-3b82f6?style=for-the-badge" alt="MIT">
</p>

**jwtlens** decodes JSON Web Tokens right in your browser. Paste a token, get a pretty header and payload, readable dates and a live expiry countdown. No server, no uploads, no tracking.

## 💡 Why local matters

Tokens are credentials. Pasting them into random websites is a bad habit. jwtlens is one HTML file that never makes a network request, so you can read it, audit it and run it offline.

## 📌 Use it

1. Open `index.html` in your browser.
2. Paste a token (a leading `Bearer ` is fine).
3. Read the result.

## 📌 What you see

- Pretty-printed **header** and **payload**
- `iat`, `nbf` and `exp` as local time and ISO 8601
- A **live countdown** that turns yellow under 5 minutes and red when expired
- Warnings for:
  - `alg: none` (unsigned token)
  - missing signature
  - no `exp` claim
  - `nbf` in the future
- Proper UTF-8 handling, so non-English claims decode correctly

## 📌 Important

jwtlens **decodes only**. It does not verify signatures, because that needs your secret or public key. A token that decodes is not a token you can trust.

## 📄 License

MIT
