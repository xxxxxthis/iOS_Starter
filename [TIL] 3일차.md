# [TIL] 3일차

---

안녕하세요 오늘은 내일배움캠프 사전캠프 3일차 TIL 입니다.

오늘은 챕터 2 문법 파트 2-1 복습 내용정리 입니다

[변수와 상수]

---

| 키워드 | 변경 가능 여부 | 예시 |
| --- | --- | --- |
| var | 가능 | var age = 20 |
| let | 불가능 | let pi = 3.14 |

Swift에서는 가능하면 let을 우선적으로 사용하고

변경이 필요한 경우에만 var 사용하는것이 좋음

예제코드

```swift
var userName = "철수"
    userName = "영희" // var(변수)은 값 변경 가능
    
let birthYear = 2005
    birthYear = 2006 // 오류 발생 let(상수)은 값 변경 뷸가능
```

---

**문제 풀어보기**

- 문제 1

  아래 코드에서 오류가 발생하는 부분을 찾고 이유 설명하기

- 코드

```swift
let appVersion = "1.0"
    appVersion = "1.1"
```

풀이

```swift
let 사용했기 때문에 오류발생
값을 변경하려면 var 사용해야함
```

---

[데이터 타입]

---

| 데이터 타입 | 설명 |
| --- | --- |
| Int | 정수 |
| Double | 실수 |
| Float | 부동소수점 숫자 |
| Bool | 논리값 |
| String | 문자열 |

예제코드

```swift
let age: Int = 20
let price: Double = 4.99
let isMember: Bool = false
let grrting: String = "안녕 스위프트"
```

---

문제 풀어보기

- 문제 1

      다음 변수를 올바르게 선언하고 값 할당하기

     **요구사항:  year , temperature , isPremiumUser**

풀이

```swift
let year: Int = 2025
var temperature: Double = 25.5
var isPremiumUser: Bool = true
```

     

---

[형 변환]

---

사용예시

정수 → 실수 변환

```swift
let integerNumber = 20
let doubleNumber = Double(integerNumber) // Int -> Double 변환
```

문자열 → 정수 변환

```swift
let strNumber = "123"
if let number = Int(strNumber) {
       print("변환된 숫자: \(number)")
       }
       else {
       print("변환실패")
       }
```

---

문제 풀어보기

- 문제 1

다음 변환이 올바르게 이루어지는지 확인하기

```swift
let price = "19.99"
let convertedPrice = Double(price)
print(convertedPrice)
```

풀이

```swift
Price 는 String 입니다 2번째 줄에서 Price를 Doule로 변환 했기 때문에
convertedPrice 는 Double로 잘 이루어집니다
```

---

[튜플]

---

예제코드

```swift
let position = (3, 4)
print(position)

let person = (name: "철수", age: 5)
print(person.name)
print(person.age) 
```

문제 풀어보기

---

- 문제 1

**상품명(String), 가격(Double), 재고(Int)를 하나의 튜플로 저장해 보세요.**

풀이

```swift
let store = (item: "사과", price: 4.99, stock: 5)
print(store.item)
print(store.price)
print(store.stock)
```

결과값

```swift
사과
4.99
5
```

---

# TMI

2-1 강의를 다시 듣는거라 처음 들었을때 보단 더 이해하기 쉬웠음

강의를 다 듣고 하나하나 내용을 정리 하니 기억에 더 잘 남는거 같음

사전캠프 퀘스트를 진행하다가 어려웠던 부분은 강의를 보면서 해결함

오늘 담당 매니저님과 상담을 통해 궁금했던 점 , 걱정헸던 부분을 깔끔하게 해결했음