## slice vs splice
- slice()와 splice()는 배열을 다룰 때 자주 사용하는 함수이다.
- 두 함수는 언뜻 보기에 비슷한 기능을 하는 것처럼 보이지만 큰 차이점이 있다.
<br>

### slice
- slice() 메소드는 begin부터 end 전까지의 복사본을 새로운 배열 객체로 반환한다. 즉, 원본 배열은 수정되지 않는다.
- **slice(시작점, 끝점)**
<br>

- 시작점
1. 시작점이 undefined인 경우: 0부터 slice
2. 음수를 지정한 경우: 배열의 끝에서부터의 길이를 나타낸다. slice(-2)를 하면 배열의 마지막 2개의 요소를 추출한다.
3. 배열의 길이와 같거나 큰 수를 지정한 경우: 빈 배열을 반환
<br>

- 끝점
1. 끝점이 undefined인 경우: 배열의 끝까지 slice
2. 음수를 지정한 경우: 배열의 끝에서부터의 길이를 나타낸다. slice(2, -1)를 하면 세 번째부터 끝에서 두 번째 요소까지 추출한다.
3. 배열의 길이와 같거나 큰 수를 지정한 경우: 배열의 끝까지 추출
<br>

### splice
- splice() 메소드는 배열의 기존 요소를 삭제 또는 교체하거나 새 요소를 추가하여 배열의 내용을 변경한다. 이 메소드는 원본 배열 자체를 수정한다.
- **splice(시작점, 제거할 요소 수, 추가할 요소1, 추가할 요소2, ...)**
- splice()는 아무 값도 제거하지 않았으면 빈 배열을 반환한다.
<br>

## sort
- sort()는 아스키 코드로 비교하여 정렬하는 함수이기 때문에 숫자일 때 그냥 사용하면 값이 의도한대로 나오지 않을 수 있다.
- 완주하지 못한 선수 때는 문자열을 정렬하는 것이라 상관 없었다.
### 오름차순
- sort((a,b) => {return a-b})

### 내림차순
- sort((b,a) => {return b-a})
<br>

![k번째 수](https://user-images.githubusercontent.com/68318945/105835600-59111600-600f-11eb-8e13-3d1b2d98f092.png)
<br>

### k번째 수 문제를 풀고 배운 점
```
자르고 정렬하는 알고리즘은 떠올랐지만 따로 자르고 정렬해야하는 줄 알았다.
slice와 sort를 한번에 할 수 있다는 것을 알고 적용해보니 훨씬 깔끔한 코드가 완성된 것 같다. 
```
