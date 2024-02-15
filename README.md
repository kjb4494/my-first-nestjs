# my-first-nestjs

## Installation

```bash
$ yarn install
```

## Running the app

```bash
# development
$ yarn run start

# watch mode
$ yarn run start:dev

# production mode
$ yarn run start:prod
```

## Test

```bash
# unit tests
$ yarn run test

# e2e tests
$ yarn run test:e2e

# test coverage
$ yarn run test:cov
```

---

## Env

- Versions

  - node v20.11.0
  - npm 10.2.4
  - yarn 1.22.21
  - typescript 5.3.3

- VSCode Settings

  ```json
  {
    "workbench.colorTheme": "Default Dark+",
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
      "source.fixAll": "explicit"
    },
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
  ```

- Added eslintrc.js Settings

  ```js
  rules: {
  	<!-- [lf -> auto] Delete `␍` eslint (prettier/prettier) -->
  	'prettier/prettier': [
  		'error',
  		{
  			endOfLine: 'auto',
  		},
  	],
  	<!-- [error -> warn] 'A' is declared but its value is never read. ts(6133) -->
  	'@typescript-eslint/no-unused-vars': 'warn'
  }
  ```

- Added Modules

  1. **uuid**: `yarn add uuid`
  1. **@types/uuid**: `yarn add @types/uuid`
  1. **[_class-validator_](https://github.com/typestack/class-validator?tab=readme-ov-file#validation-decorators)**: `yarn add class-validator`
  1. **class-transformer**: `yarn add class-transformer`
  1. **typeorm + postgres**: `yarn add pg typeorm @nestjs/typeorm`

- postgres docker

  ```shell
  docker run --name postgres -p 5432:5432 -e POSTGRES_PASSWORD=P@ssw0rd -d postgres:latest
  ```

  ```posgres
  CREATE DATABASE "board-db";
  ```

## Memo

- `nest g resource [name]` 명령어로 만들고자 하는 리소스의 CRUD 보일러플레이트 코드를 한 번에 생성할 수 있다.
