# TypeScript Node Server Deployed to Vercel

## Demo Link

- Home Page: https://node-ts-server-in-vercel.andy770921.vercel.app/

- About Page: https://node-ts-server-in-vercel.andy770921.vercel.app/about

- API: https://node-ts-server-in-vercel.andy770921.vercel.app/api

## TypeScript Node Server Example

```ts
import express from 'express';

const app = express();

app.get('/', (req, res) => res.send('Home Page Route'));

app.get('/about', (req, res) => res.send('About Page Route'));

app.get('/api', (req, res) => res.status(200).json({ data: 'api' }));

const port = process.env.PORT || 3000;

app.listen(port, () => console.log(`Server running on ${port}, http://localhost:${port}`));
```

## Install and Development

1. `npm install`

2. `npm run start`: compile TypeScript to JavaScript and start running local server

3. `npm run lint`: check lint manually

## Build and Deployment

1. `npm run build`: compile `src/app.ts` to `dist/app.js`

2. Deploy to Vercel: [Vercel](https://vercel.com/) takes `src/app.ts` and compiles TypeScript to JavaScript automatically for deployment. Detail settings are in the file `vercel.json`.

## Reference Tutorial

- [Deploying Apollo Server with TypeScript Path Aliases to Vercel](https://dev.to/ozanbolel/deploying-apollo-server-with-typescript-path-aliases-to-vercel-4k5l)

- [How to set up an Express.js API using Webpack and TypeScript](https://medium.com/the-andela-way/how-to-set-up-an-express-api-using-webpack-and-typescript-69d18c8c4f52)

- [nodemon-webpack-plugin](https://www.npmjs.com/package/nodemon-webpack-plugin)

