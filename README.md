# ERR_DIFFERENT_STORAGE_BACKEND when using a DO from remote worker with new vite plugin

This repo shows an issue with local dev when using a DO from a remote worker with the new vite plugin.

To see the error run:

```sh
pnpm install
pnpm run dev
```

This repo is copied from [this playground example](https://github.com/cloudflare/workers-sdk/tree/main/packages/vite-plugin-cloudflare/playground/external-durable-objects) from the official repo.

That example works, but in that example the Durable Object isn't properly declared as part of the external worker.

In this repo, I've moved the binding and migrations to `worker-b`.
This breaks the example.