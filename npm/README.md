# NPM

## C

- [x] core-js



## N

- [x] npm-run-all
> 병렬 또는 순차적으로 여러 npm 스크립트를 실행하는 CLI 도구



### 스크립트 병렬 실행

`npm run script` 명령으로는 여러 개의 `npm script` 를 실행할 수 없다.

```bash
npm run build && npm run start
```

위와 같은 형식으로 npm script 나열



### -parallel
`npm-run-all` 을 사용하면 일반적 나열로 스크립트 실행 가능

```bash
npm-run-all -p build start
```

`-p` 는 병렬 옵션이며, `-parallel` 이다.

-max-parallel 로 최대 병렬 개수 지정 가능



## U

- [x] underscore
