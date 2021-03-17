## CSS

- `'box-sizing: content-box'` (by default):
  CSS의 width, height는 border 값을 뺀 컨텐트 자체 값만을 계산하기 때문에, 같은 크기라도 보더가 다르면 크기가 다르게 보인다.

- `'border-box'`라고 지정하게 되면, 컨테이너의 border 값이 같아지게 되고 같은 width 값으로 컨테이너의 길이를 똑같게 맞출 수 있다.

- 사이징을 맞추기 쉬워지기 때문에, 전체 지정으로 해놓는 경우가 많다.

```

* {
  box-sizing: border-box;
  }

```

## JS

- querySelectorAll(CSSSelector) puts all selected elements into the 'Nodelist' which is very similar to an array.

- `'+'` is equal to `'parseInt()'` which makes the value a number
