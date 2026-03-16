## Plan: Add backend FastAPI tests

**TL;DR:**
- Add a new `tests/` directory with pytest tests for the FastAPI backend.
- Use FastAPI `TestClient` to validate `/activities`, signup, duplicate signup, and unregister behavior.
- Ensure tests are isolated by resetting the in-memory `activities` store between tests.

**Next Steps:**
1. Create `tests/test_app.py` with a pytest fixture resetting `activities`.
2. Add tests for:
   - retrieving activities (`GET /activities`)
   - signing up (`POST /activities/{activity}/signup`)
   - preventing duplicate signups (400 response)
   - unregistering participants (`DELETE /activities/{activity}/unregister`)

**Verification:**
- Run `pytest` and confirm all tests pass.
