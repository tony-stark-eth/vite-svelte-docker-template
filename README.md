# Vite Svelte Docker Template

This template offers the following things, ready to use, in a dockerized environment:

- [Vite](https://vitejs.dev/)
- [Svelte 4](https://svelte.dev/) (TS)
- [ESLint](https://www.npmjs.com/package/eslint)
- [Prettier](https://prettier.io/)
- [Svelte-Check](https://www.npmjs.com/package/svelte-check)
- Testing Svelte with [Vitest](https://vitest.dev/) & [Testing Library](https://www.npmjs.com/package/@testing-library/svelte)

## Create with it!

```sh
npx degit bavragor/vite-svelte-docker-template app-name
```

## Requirements

- Docker
- make

## Installation

```sh
make setup
make up
make install
```

## Development

```sh
docker compose exec app pnpm run dev
```

## Build

```sh
docker compose exec app pnpm run build
```

## Preview

```sh
docker compose exec app pnpm run preview
```

## Test

```sh
docker compose exec app pnpm run test
```

Or with coverage in build directory

```sh
docker compose exec app pnpm run test:coverage
```

## OS specific settings

### Windows + WSL2 + Symlinks + PNPM

In case your running a setup like me,
WSL2 with Ubuntu and have your IDE running on Windows,
your IDE may not be able to use symlinks created by pnpm.
For this scenario you can do the following

```
cp .npmrc.dist .npmrc
make build
make up
make install
```

This will run pnpm without symlinks.
