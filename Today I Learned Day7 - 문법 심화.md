# Today I Learned  Day7 - 문법 심화

---

## 딕셔너리 이해하기

---

필요한 이유: 여러 데이터 중 특정 값을 키로 쉽게 접근하고자 할때 딕셔너리를 사용합니다

개념: 딕셔너리는 키 와 값의 쌍으로 데이터를 저장합니다

---

## 딕셔너리의 심화: 키-값 구조 활용, 딕셔너리 조작

---

딕셔너리 생성과 기본 사용

---

```swift
var studentScores: [String: Int] = ["Alice": 90, "Bob": 85, "Charlie": 88]
```

```swift
값 가져오기
		키를 사용해 값을 가져올수있음 존재하지않는 키를 조회하면 nil 반환
		
let aliceScore = studentScores["Alice"]
print(aliceScore)  // Optional(90)

let unknownScore = studentScores["David"]
print(unknownScore)  // nil

```

```swift
기본값 제공
	키가 존재하지 않을 경우 기본값을 설정 가능

let davidScore = studentScores["David", default: 0]
print(davidScore)  // 0
```

---

딕셔너리에 요소 추가 및 수정

---

```swift
키와 값을 함께 순회

let studentScores = ["Alice": 95, "Bob": 89, "David": 92]

for (name, score) in studentScores {
    print("\(name): \(score)")
}
```

```swift
키만 가져오기

for name in studentScores.keys {
    print(name)
}
```

```swift
값만 가져오기

for score in studentScores.values {
    print(score)
}
```

---