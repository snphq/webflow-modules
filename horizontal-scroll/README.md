## Description

Native js module for cellar ecommerce.

## Getting Started

**Install all of the dependencies:**

```bash
yarn
```

**Run dev server:**

```bash
yarn start
```

dev server host: localhost:5000

**Build and deploy:**

staging build:

```bash
yarn build:staging
```

staging deploy:

```bash
bundle exec cap testing deploy
```

production build:

```bash
yarn build
```

production deploy:

```bash
bundle exec cap production deploy
```

## Structure

**src / ...**

src/api - api

src/components - js components

src/constants - all config or common variables

src/html - html templates for development

src/utils - helper functions

src/cellarEcom.js - entry script

/webpack - webpack config

**public / ...**

```cellarEcom.min.js``` - module script.
