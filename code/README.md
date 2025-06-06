## `Develop 👨‍💻`

Both the public website and admin panel are statically generated. Powered by [SvelteKit](https://kit.svelte.dev/).\
The admin panel is using a REST API that runs as a node server. Powered by [Directus](https://directus.io/).

### Backend: <small>`/backend`</small>

#### 1. Directus: <small>`/backend/directus`</small>

Directus turns an SQL database into a REST API.

`npm run start`

#### 2. Heimdall: <small>`/backend/heimdall`</small>

Heimdall is a custom server that performs actions based on the information from the admin panel.

`npm run dev`

### Frontend: <small>`/frontend`</small>

`npm run dev`

<br/>

## `Deploy 🏃`

Setup [nginx](https://nginx.org/).\
Consider running everything with [pm2](https://github.com/Unitech/pm2).

Serve SvelteKit on port **80**.\
Serve Directus on port **8055**.\
Serve Heimdall on port **999**.

#### Backend: <small>`/backend`</small>

1. Run Directus (<small>`npm run start`</small>)
2. Run Heimdall (<small>`npm run start`</small>)

#### Frontend: <small>`/frontend`</small>

Build (<small>`npm run build`</small>) and run the node server (<small>`node ./build`</small>).
