# Flowboard

Collaborative project management app with React, Express, SQLite and Socket.IO.

## Run

```bash
npm install
npm run dev
```

Open `http://localhost:5173`. Register an account, create a project, invite a teammate by their email, and create tasks. The database is stored at `server/flowboard.db`.

## API overview

All non-auth routes require `Authorization: Bearer <token>`.

- `POST /api/auth/register`, `POST /api/auth/login`, `GET /api/auth/me`
- `GET/POST /api/projects`, `GET/PATCH/DELETE /api/projects/:id`
- `POST /api/projects/:id/members`, `PATCH/DELETE /api/projects/:id/members/:userId`
- `GET/POST /api/projects/:id/boards`, `PATCH/DELETE /api/boards/:id`
- `GET/POST /api/boards/:id/tasks`, `PATCH/DELETE /api/tasks/:id`, `POST /api/tasks/:id/move`
- `GET/POST /api/tasks/:id/comments`, `DELETE /api/comments/:id`
- `GET /api/projects/:id/activity`, `GET /api/projects/:id/notifications`

Roles: owners administer projects and members; admins edit boards/tasks; members create and update tasks; viewers read and comment.
