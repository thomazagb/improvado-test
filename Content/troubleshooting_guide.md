# 🛠️ Troubleshooting Guide

This guide covers common issues encountered when working with the GitHub API, especially during token-based authentication and pagination.

---

## ✅ 1. 401 Unauthorized Error

Occurs when authentication with the API fails.

### 🔎 Possible Causes & Solutions:

| Cause | Description | Solution |
|-------|-------------|----------|
| ❌ Missing or incorrect token | The token is missing or has a typo | Check the `GITHUB_TOKEN` variable or Postman env var |
| ❌ Expired or revoked token | Tokens can be disabled or expire | Generate a new token in GitHub Developer Settings |
| ❌ Insufficient token permissions | Token doesn't have access to the resource | Ensure token has `repo`, `read:org`, etc. |
| ❌ Malformed header | Improper formatting of the `Authorization` header | Use `"Authorization": "Bearer <TOKEN>"` |

---

## ✅ 2. Rate Limits (403 Forbidden)

GitHub has hourly request limits:

- Authenticated: **5,000 requests/hour**
- Unauthenticated: **60 requests/hour**

### 🔄 Handling Rate Limits:

- Check usage:
```python
rate_url = "https://api.github.com/rate_limit"
rate_data = make_request(rate_url, "Check Rate Limits")
print(rate_data["rate"]["remaining"])
```

- Use `time.sleep()` between requests
- Authenticate with a token for higher limits

---

## ✅ 3. 404 Not Found

### 🔍 Common Causes:

- Typo in endpoint URL
- Repository or file doesn't exist
- Trying to access private content with a public token

### 🧰 Fix:

- Confirm URL structure
- Test the endpoint manually
- Make sure the file (e.g., `README.md`) actually exists in the repo

---

## ✅ 4. Best Practices: Colab vs. Postman

| Feature | Colab | Postman |
|---------|-------|---------|
| 🔐 Token Storage | Set as Python variable at top | Use environment variable `Authorization` |
| 🔁 Pagination | Use `for`/`while` with `page` param | Set `{{page}}` and loop in requests |
| ⏱️ Rate Limit Handling | Check `/rate_limit` and use delays | Use `Tests` + control flows if needed |
| 💾 Save Responses | `json.dump()` to file | Manually export responses |

---

Always monitor headers and responses carefully when building robust API extraction workflows.
