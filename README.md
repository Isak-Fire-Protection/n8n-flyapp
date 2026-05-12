# n8n on fly.io for Isak Fire Protection
An n8n self-hosted instance hosted on fly.io made especially for Isak Fire Protection's tech team.

## fly.io Deployment
1. Create a Neon Postgres database.
2. `fly launch --copy-config --no-deploy --org isak-fire-protection`
3. `git restore fly.toml`
4. On .env repo: `fly secrets import --app n8n-isak-fp < .env`
5. `fly deploy --ha=false`

## Change server configuration
1. `fly deploy`

## .env contents
```
DB_POSTGRESDB_HOST=
DB_POSTGRESDB_PASSWORD=
N8N_ENCRYPTION_KEY=
N8N_USER_MANAGEMENT_JWT_SECRET=
```