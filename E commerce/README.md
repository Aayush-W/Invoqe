# ShopSphere

React + TypeScript/Vite storefront, with a TypeScript Express REST API and Prisma/PostgreSQL persistence model.

## Run locally

1. Copy `backend/.env.example` to `backend/.env` and set `DATABASE_URL` / `JWT_SECRET`.
2. `npm install`
3. `npm run prisma:generate -w backend && npm run prisma:migrate -w backend`
4. `npm run dev`

The UI runs at `http://localhost:5173` and API at `http://localhost:4000`. Seed product records through Prisma Studio or the admin product endpoint after creating an admin user.

The included storefront can be explored without a database; its catalog will show once the API has records and its bag is persisted in browser local storage. The API remains the server authority for authenticated carts, stock and order totals.
