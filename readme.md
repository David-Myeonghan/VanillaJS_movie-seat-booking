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

- Save in local storage

- Spread syntax `'...'`:
  Allows an iterable such as an array expression or string to be expanded in places where 0 or more arguments are expected. It's passing in the value of an array, not passing in the actual array. Can use it with objects.

```
const arr = [1,2,3];
const arr2 = [...arr,4,5];

console.log(arr2); // Array[1,2,3,4,5]
```

- High Order Array method

- forEach():
  doesn't return anything. Just loops through.

- map():
  will return an array

```
arr.forEach(function(item) {
    console.log(item)
})

const arr3 = arr2.map(function(item) {
    return item * 2;
});

console.log(arr3) // Array[2,4,6,8,10]
```

- indexOf():

```
const arr = [1,2,3,4,5];
console.log(arr.indexOf(5)) // 4
console.log(arr.indexOf(100)) // -1
```

- localStorage: don't need to import anything.

```
localStorage.setItem('name', 'David');
```

- select event 발생하지 않더라도 첫번째 영화를 로컬 스토리지에 담아두는 방법...
  (select에서 첫번째 영화 볼 거라서 영화는 선택안하고, 좌석 선택 바로 할 때는 로컬스토리지에 담기지 않는다.)

  - 즉시실행 함수로 초기화하기 - Unnecessary flow -> Not Scalable.
  - 좌석선택시(이벤트 발생시) default select value 같이 저장해두기 -> Reasonable!
  - 굳이 이 페이지에선 할 필요 없다 실제라면 다음 화면 넘어갈 때 저장해두면 된다 -> Best!
    updateSelectedCount()에서 개선 필요 - seats만 관여하는 것이 타당한가

  ```
  movieSelect.selectedIndex;
  movieSelect.value; // 이용해서 저장
  ```
