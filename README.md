# Redwood

> **WARNING:** RedwoodJS software has not reached a stable version 1.0 and should not be considered suitable for production use. In the "make it work; make it right; make it fast" paradigm, Redwood is in the later stages of the "make it work" phase.

## Getting Started
- [Tutorial](https://redwoodjs.com/tutorial/welcome-to-redwood): getting started and complete overview guide.
- [Docs](https://redwoodjs.com/docs/introduction): using the Redwood Router, handling assets and files, list of command-line tools, and more.
- [Redwood Community](https://community.redwoodjs.com): get help, share tips and tricks, and collaborate on everything about RedwoodJS.

### First-time Setup

1. To install dependencies, just do this in the root directory:

```terminal
yarn install
```

2. Create a `.env` file:

```
cp .env.example .env
```

3. Set up an [Infura account](https://infura.io/). Create a new project. Copy the project secret to the `INFURA_ID` environment variable in your `.env` file.

4. Generate a jwt secret and set it to ETHEREUM_JWT_SECRET in your `.env` file:

```
echo "ETHEREUM_JWT_SECRET=$(openssl rand -base64 32)" >> .env
```

5. Set up the database:

```
yarn rw prisma migrate dev
```

### Fire it up


```terminal
yarn redwood dev
```

Your browser should open automatically to `http://localhost:8910` to see the web app. Lambda functions run on `http://localhost:8911` and are also proxied to `http://localhost:8910/.redwood/functions/*`.
