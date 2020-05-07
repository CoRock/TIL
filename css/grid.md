# Grid

## Grid Container Properties

그리드 컨테이너를 위한 속성들은 다음과 같습니다.

| 속성                    | 의미                               |
| ----------------------- | ---------------------------------- |
| `display`               | 그리드 컨테이너(Container) 를 정의 |
| `grid-template-rows`    | 명시적 행(Track) 의 크기를 정의    |
| `grid-template-columns` | 명시적 열(Track) 의 크기를 정의    |



## Grid Item Properties

그리드 아이템을 위한 속성들은 다음과 같습니다.

| 속성          | 의미                                              |
| ------------- | ------------------------------------------------- |
| `grid-row`    | `grid-row-xxx` 의 단축 속성(행 시작 / 끝 위치)    |
| `grid-column` | `grid-column-xxx` 의 단축 속성(열 시작 / 끝 위치) |
|               |                                                   |



## Grid Containers

### display

### grid-template-rows

```css
.container {
  display: grid;
  grid-template-rows: 1행크기 2행크기 ...;
  grid-template-rows: [선이름] 1행크기 [선이름] 2행크기 [선이름] ...;
}
```



### grid-template-columns

>   명시적 열(Track) 의 크기를 정의합니다.

동시에 라인(Line) 의 이름도 정의할 수 있습니다.

`fr` (fraction, 공간 비율) 단위를 사용할 수 있습니다.

`repeat()` 함수를 사용할 수 있습니다.
