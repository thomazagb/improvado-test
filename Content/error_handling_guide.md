# Error Handling Guide

Common error codes:
- 401 Unauthorized: Token missing or invalid
- 403 Forbidden: Rate limit exceeded or access denied
- 404 Not Found: Resource does not exist

Best practices:
- Always check `response.status_code`
- Use `try/except` blocks for connection errors
