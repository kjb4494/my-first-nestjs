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

## Memo

- 개발 환경 버전

  - node v20.11.0
  - npm 10.2.4
  - yarn 1.22.21
  - typescript 5.3.3

- vscode settings

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

- eslintrc.js에 추가한 설정

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

- `nest g resource [name]` 명령어로 만들고자 하는 리소스의 CRUD 보일러플레이트 코드를 한 번에 생성할 수 있다.
