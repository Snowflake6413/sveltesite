# Personal website

### Info
Personal website, written in Svelte.

>[!IMPORTANT]
> Yes, I know I used a clanker for this project but it was fixing 3 little bugs I swear :(

### Quickstart
You must have:
* Bun

#### Steps
1. Clone this repo
```bash
   git clone https://github.com/Snowflake6413/sveltesite
```

2. Enter directory
```bash
cd sveltesite
```

3. Install dependencies
```bash
bun install
```
4. Run the server
```bash
bun run dev
```
5. Profit

### Deployment on Coolify

This project uses `@sveltejs/adapter-node` for Node.js-compatible deployments.

#### Coolify Configuration
Configure the following settings in your Coolify project:

- **Build Command**: `npm run build` or `bun run build`
- **Start Command**: `npm run start` or `node build/index.js`
- **Port**: `3000` (default for adapter-node)

The adapter will create a standalone Node.js server in the `build` directory that's ready to deploy.
