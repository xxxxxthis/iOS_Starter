# Today I Learned  Day6 - 문법 심화

---

## 배열  이해하기

---

필요한 이유: 배열은 동일한 데이터 타입을 여러 개 저장할 때 필요합니다.

개념: 배열은 같은 데이터 타입의 여러 값을 순차적으로 저장하는 자료형입니다.

---

## 배열의 심화: 요소 추가, 삭제, 필터링, 정렬

---

배열에 요소 추가하는 방법 알아보기!

---

```swift
1. append()

var numbers = [1, 2, 3, 4]
numbers.append(5) // 배열의 마지막에 요소 추가
print(numbers) // [1, 2, 3, 4, 5]
```

```swift
2. insert()

var numbers = [1, 2, 3]
numbers.insert(4, at: 3) // 배열의 특정 위치에 요소 추가
print(numbers) // [1, 2, 3, 4]
```

```swift
3. += 연산자

var numbers = [1, 2, 3]
numbers += [4, 5, 6] // 배열에 하나 이상의 요소를 추가할 때 사용
print(numbers) // [1, 2, 3, 4, 5, 6]
```

---

배열에서 요소 삭제하는 방법 알아보기!

---

```swift
1. remove()

var numbers = [1, 2, 3]
numbers.remove(at: 2) // 배열에서 특정 요소 제거
print(numbers) // [1, 2]
```

```swift
2. removeFirst() , removeLast()

var numbers = [1, 2, 3]
numbers.removeFirst() // 첫번째 요소 제거
print(numbers) // [2, 3]

numbers.removeLast() // 마지막 요소 제거
print(numbers) // [2]
```

```swift
3. removeAll()

var numbers = [1, 2, 3, 4]
numbers.removeAll() // 모든 요소 제거
print(numbers)  // []
```

---

배열 필터링하는 방법 알아보기!

---

```swift
1. filter()

let numbers = [1, 2, 3, 4, 5, 6]
let evenNumbers = numbers.filter { $0 % 2 == 0 } // 조건을 만족하는 요소만 남긴 새로운 배열 생성
print(evenNumbers)  // [2, 4, 6]
```

---

배열 정렬하는 방법 알아보기!

---

```swift
1. sorted()

let numbers = [4, 10, 99, 3, 1, 6, 5]
let sortedNumbers = numbers.sorted() // 베열을 정렬한 새로운 배열 반환
print(sortedNumbers)  // [1, 3, 4, 5, 6, 10, 99]
```

```swift
2. sort()

var numbers = [3, 1, 2, 0, 10, 3]
numbers.sort() // 배열을 정렬하지만 원본 배열 자체가 변경됨
print(numbers)  // [0, 1, 2, 3, 3, 10]

```

```swift
3. 내림차순 정렬 
sorted(by:) 또는 sort(by:)를 사용해 내림차순 정렬 가능

let numbers = [100, 50, 110, 1, 10]
let descendingNumbers = numbers.sorted(by: >)
print(descendingNumbers)  // [110, 100, 50, 10, 1]
```

---

오늘은 이렇게 문법 심화 파트에서 배열 심화를 공부해봤습니다

내일은 딕셔너리 심화와 데이터 모델링을 공부해보겠습니다.