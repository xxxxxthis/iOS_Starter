# [TIL] 4일차

---

안녕하세요 오늘은 내일배움캠프 사전캠프 4일차 TIL 입니다.

오늘은 챕터 2 문법 파트 2-2 복습 내용정리 입니다

[배열]

---

배열은 동일한 데이터 타입을 여러 개 저장할 때 필요함.
예를 들어, 한 명의 학생이 여러 과목에 대한 성적을 가지고 있을 때 사용함.

배열은 같은 데이터 타입의 여러 값을 순차적으로 저장하는 자료형

배열의 크기는 고정되어 있지 않고 동적으로 변경할수있음

| 특징 | 설명 |
| --- | --- |
| 선언 | var number: [Int] |
| 초기화 | let number = [1, 2, 3, 4, 5] |
| 요소 접근 | number[0] (첫번째 요소) |
| 메서드 | appen(), remove(at:), sorted() 등 |

배열을 만들때는 []를 사용하여 값을 넣음

예제코드

```swift
// 선언과 초기화
    var numbers: [Int] = [1, 2, 3]
    
// 값 추가
        numbers.append(10) // 배열 끝에 10 추가

// 특정 값 제거
    numbers.remove(at: 1) // 인덱스 1의 값(2) 제거
    
// 값 정렬
    let sortedNumbers = numbers.sorted() // 오름차순 정렬

print(sortedNumbers) // [1, 3, 10]
```

---

**문제 풀어보기**

- 문제 1

**다음 배열의 선언과 값 추가, 첫 번째 요소 출력이 잘 이루어지는지 확인해 보세요.**

요구사항

정수 배열을 선언하고 10, 20, 30을 넣으세요.

배열에 40을 추가하고 첫 번째 요소를 출력하세요.

- 코드

```swift
var numbers: [Int] = [10, 20, 30] // 선언과 초기화

	numbers.append(40) // 값 추가

print(numbers[0]) // 출력
```

---

[딕셔너리]

---

딕셔너리는 키-값 쌍으로 데이터를 저장할 수 있는 자료형

딕셔너리는 데이터를 구분할 수 있는 키를 통해 값을 빠르게 찾아낼 수 있음

여러 데이터 중 특정 값을 키로 쉽게 접근하고자 할 때 딕셔너리를 사용함

딕셔너리는 키와 값의 쌍으로 데이터를 저장함

딕셔너리에서 각 키는 고유해야 하고,
하나의 키에 하나의 값이 대응함 값은 중복될 수 있지만,
키는 중복될 수 없음 딕셔너리는 데이터를 빠르게 찾고 관리할 때 유용함

| 특징 | 설명 |
| --- | --- |
| 선언 | var student: [Int: String] (학번: 이름) |
| 초기화 | let student = [101: “존”, 102: ”엘리스”] |
| 값 접근 | student[101]  (키을 이용해 값 접근) |
| 메서드 | updateValue(), removeValue(forKey:), keys, values 등 |

예제코드

```swift
// 선언과 초기화
	var student: [Int: String] = [101: "존", 102: "엘리스"]

// 값 접근
	student[101] // 존

// 딕셔너리는 없는 키 값에 값을 넣으면 새로운 딕셔너리 값이 추가됨
	student[103] = "페페"

// 값 수정
	student[102] = "철수"
	
// 딕셔너리에서 키 값에 해당하는 값 삭제
	student.removeValue(forKey: 101) // 101: "존" 삭제
	
// 값 출력
	print(student) // [102: "철수", 103: "페페"]
```

---

문제 풀어보기

- 문제 1

   **딕셔너리에 기존 학생의 정보를 수정하고, 새로운 학생 정보를 추가해 보세요.**

     **요구사항**

ID: 202의 이름을 emma로 변경

다음의 studnets 딕셔너리에 학생 ID 203과 이름 frank 를 추가하시오

```swift
var students: [Int: String] = [201: "David", 202: "Eva"]
```

풀이

```swift
var students: [Int: String] = [201: "David", 202: "Eva" ] // 선언과 초기화
	students[202] = "emma" // 값 변경
	students[203] = "frank" // 값 추가
	
	print(students) // [201: "David", 203: "frank", 202: "emma"]
```

     

---

[셋]

---

셋은 중복을 허용하지 않고, 순서가 없는 데이터 집합을 저장할 때 사용함
데이터를 추가할 때 중복을 자동으로 제거해줌

셋은 **순서가 없고**, **중복을 허용하지 않는** 자료형이에요. 인덱스를 사용해 값에 접근할 수 없음

셋은 데이터를 효율적으로 관리하고, 중복 제거가 필요한 경우에 유용함

| 특징 | 설명 |
| --- | --- |
| 선언 | var uniqueNumbers: Set<Int> |
| 초기화 | let fruits: set = [”사과”, “바나나”, “오렌지”] |
| 값 추가 | uniqueNumbers.insert(10) |
| 값 삭제 | uniqueNumbers.remove(10) |
| 포합 여부 | uniqueNumbers.contains(10) |

예제코드

```swift
// 선언과 초기화
    var fruits: Set<String> = ["사과", "오렌지", "망고"]
    
// 값 추가
    fruits.insert("포도")
    
// 값 제거
    fruits.remove("사과")

// 특정 값이 포함되어 있는지 확인
    if fruits.contains("오렌지") {
        print("오렌지가 셋에 포함되어 있어요")
            
        }

     
// 출력
    
    print(fruits) // ["망고", "포도", "오렌지"]

```

---

문제 풀어보기

- 문제 1
    
    다음 셋을 선언하고 바나나를 추가한 후 셋을 출력하기
    
    요구사항
    
     frutis 셋에 사과 포도 오렌지 를 추가하기
    
    셋에 바나나 를 추가하고 결과를 출력하기 
    

풀이

```swift
var fruits: Set<String> = ["사과", "포도", "오렌지"]
	fruits.insert("바나나")
	
print(fruits) // ["바나나", "오렌지", "사과", "포도"]
```

---

## 어려웠던 부분

---

사전캠프 퀘스트 연산자의 이해 마지막 과제를 진행하는 도중에 약간에 어려움이 있었지만

강의를 통해 해결했음   [공식 문서](https://docs.swift.org/swift-book/documentation/the-swift-programming-language)

# TMI

---

내일은 2-3 강의 부터 2-5 강의를 복습 후 내용정리 하기

스위프트 공식 문서 읽어보기  [공식 문서](https://docs.swift.org/swift-book/documentation/the-swift-programming-language)

챕터 3 듣기 전까지 문법 어느정도 숙지하기