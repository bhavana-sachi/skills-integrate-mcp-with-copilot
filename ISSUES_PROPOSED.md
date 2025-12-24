# Proposed GitHub Issues — Extracurricular Features

This file contains proposed issues to add features from `pennlabs/penn-clubs` to this project.

---

## 1. Add persistent database and ORM
**Description:** Replace in-memory `activities` store with a persistent database (SQLite for dev; PostgreSQL as production option) and an ORM (SQLModel or SQLAlchemy). Migrate current activity fields to a model.
**Acceptance criteria:** Activities persist across restarts; CRUD operations work via API; migration scripts or models included.
**Priority:** High

## 2. Implement authentication (SSO/OAuth)
**Description:** Add user authentication so actions can be gated (signup, management). Support campus SSO or OAuth-compatible flows; fallback to basic accounts for testing.
**Acceptance criteria:** Login flow works; protected endpoints require auth; frontend shows login prompts.
**Priority:** High

## 3. Club ownership requests & approval workflow
**Description:** Allow users to request ownership of an activity/club and let admins or current owners accept/reject; send email notifications.
**Acceptance criteria:** Ownership request endpoint, admin approval UI or API, email template present, ownership stored in DB.
**Priority:** High

## 4. Full CRUD for activities, events, and resources
**Description:** Add endpoints and frontend forms to create/update/delete activities, events, and attached resources (links, files).
**Acceptance criteria:** Endpoints and frontend pages for create/edit/delete exist and enforce auth and permissions.
**Priority:** High

## 5. Search, filtering, and pagination for activities
**Description:** Implement search and filters (by tag, schedule, availability) and API pagination.
**Acceptance criteria:** Frontend search/filter UI; API supports query params and pagination.
**Priority:** Medium

## 6. Admin/moderation UI and role-based access control
**Description:** Add admin panel and roles (admin, owner, member) with server-side enforcement.
**Acceptance criteria:** Roles stored, role checks implemented, admin endpoints or UI available.
**Priority:** Medium

## 7. Email notifications and templates
**Description:** Integrate an email service (SMTP or transactional provider) and add templates for ownership acceptance, signup confirmations, and reminders.
**Acceptance criteria:** Emails can be sent locally (console) and template files included.
**Priority:** Medium

## 8. Frontend improvements: React/SPA components and auth-aware UI
**Description:** Modularize the frontend into reusable components, add auth-aware prompts (login required for actions), and improve the participants UI.
**Acceptance criteria:** New components added; UI shows auth prompts and updates dynamically.
**Priority:** Medium

## 9. Add fairs / static markdown pages support
**Description:** Support markdown-based static pages (FAQ, fair pages) rendered in frontend.
**Acceptance criteria:** Markdown pages render and are editable in repo.
**Priority:** Low

## 10. Add devcontainer, CI, and developer README
**Description:** Add a `.devcontainer`, CI workflow for tests, and expand `README` with local setup instructions.
**Acceptance criteria:** Devcontainer present; CI runs basic tests; README updated.
**Priority:** Low

## 11. API hardening: validation, pagination, rate-limiting
**Description:** Add input validation, error handling improvements, pagination defaults, and optional rate-limiting.
**Acceptance criteria:** Validation for endpoints; sensible error messages; pagination for large lists.
**Priority:** Low

---

If you'd like, I can open individual GitHub issues for each of these (requires repository issue-creation permission), or I can open a pull request that adds this file and then create issues from it. Which do you prefer?