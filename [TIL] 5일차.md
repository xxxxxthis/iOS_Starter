# [TIL]  5일차

---

안녕하세요  오늘은 챕터 2 문법파트 2-3부터 2-5 강의 복습 내용 정리 입니다.

1. 조건문과 반복문
2. 함수와 옵셔널
3. 클래스와 구조체

위 3개 강의를 요약 정리 했습니다.

- 조건문
    
    필요성 및 개념설명
    
    필요이유
    
     프로그래밍에서는 특정 조건에 따라 코드의 실행 흐름을 제어해야 하는 경우가 많음
    
    예를 들어 사용자가 입력한 값이 양수인지 음수인지에 따라 다른 동작을 수행하거나
    
    로그인 정보가 올바른지 확인해야 할 때 조건문을 사용함
    
    개념과 설명
    
    if문
    
    if문은 특정 조건이 ture 일 때만 코드 블록을 실행함
    
    기본 문법
    
    ```swift
    if 조건 {
    		실행 할 코드
    	}
    ```
    
    예제
    
    ```swift
    let age = 20
    
    	if age >= 18 {
    			print("성인입니다.")
    		}
    ```
    
    if else문
    
    if문의 조건이 false일 경우, else 블록을 실행할 수있음
    
    기본 문법
    
    ```swift
    if 조건 {
    		실행 할 코드 (조건이 참일때)
    	}
    	else {
    		실행할 코드 (조건이 거짓일때)
    	}
    ```
    
    예제
    
    ```swift
    let temperature = 15
    	
    	if temperature >= 20 {
    		print("따뜻함")
    	}
    		else {
    		print("쌀쌀함")
    	}
    ```
    
    if else if else문
    
    여러 개의 조건을 검사해야 할 경우 else if문을 추가하여 사용할 수 있음
    
    기본 문법
    
    ```swift
    if 조건1 {
    	실행할 코드1
    	}
    	if else 조건2 {
    		실행할 코드2
    	}
    	else {
    		 실행할 코드3
    		}
    ```
    
    예제
    
    ```swift
    let score = 85
    
    if score >= 90 {
        print("A학점")
    }
    else if score >= 80 {
        print("B학점")
    }
    else if score >= 70 {
        print("C학점")
    }
    else {
      print("F 학점")
    }
    
    ```
    
    switch문
    
    switch문은 값이 특정한 경우에 따라 실행 할 코드를 분기 할 때 사용함
    
    if-else문보다 가독성이 뛰어나고 실핼 속도가 빠를수 있음
    
    기본 문법
    
    ```swift
    switch 값 {
    	case 패턴1:
    			실핼할 코드
    	case 패턴2:
    			실행할 코드
    	default:
    			실행할 코드
    	}
    ```
    
    예제
    
    ```swift
    let grade = "B"
    	switch grade {
    			case "A":
    				print("훌륭한 성적")
    			case "B":
    				print("좋은 성적")
    			case "C":
    				print("보통 성적")
    			default:
    				print("노력필요")
    			}
    ```
    
    범위를 사용한 예제
    
    ```swift
    let number = 7
    	switch number {
    		case 1...5:
    			print("1에서 5 사이")
    		case 6...10:
    			print("6부터 10 사이")
    		default:
    			print("그 외의 숫자")
    		}
    		
    ```
    
    ---
    
- 반복문
    
    필요성 및 개념설명
    
    필요이유
    
    프로그래밍을 하다보면 같은 동작을 여러번 수행해야 하는 경우가 많음
    
    만약 같은 코드를 여러번 복사해서 사용한다면 코드가 길어지고 관리하기 어려워짐
    
    반목문을 사용하면 코드의 중복을 줄이고 가독성을 높일수있음
    
    개념과 설명
    
    for-in 반복분
    
    for-in 반복문은 일정한 범위의 값을 순회하며 실행할때 사용함
    
    기본 문법
    
    ```swift
    for 변수 in 범위 {
    		실행할코드
    }
    ```
    
    예제
    
    ```swift
    for i in 1...5 {
    		print("\(i)번째 반복")
    	}
    ```
    
    배열을 사용한 예제
    
    ```swift
    let fruits = ["사과", "바나나", "포도"]
    
    for fruit in fruits {
        print(fruit)
    }
    
    ```
    
    while 반복문
    
    while 반복문은 조건이 참(true)인 동안 계속 실행함
    
    기본 문법
    
    ```swift
    while 조건 {
        실행할 코드
      }
    ```
    
    예제
    
    ```swift
    var count = 10
        while count > 0 {
            print("남은시간: \(count)")
            count -= 1
        }
    
    ```
    
    repeat-while 반복문
    
    repeat-while 반복문은 while과 유사하지만 무조건 한번은 실행 한후 조건을 검사함
    
    기본 문법
    
    ```swift
    repeat {
    		실행할 코드
    	}
    	 while 조건
    ```
    
    예제
    
    ```swift
    var count = 3
        repeat {
            print("카운드: \(count)")
            count -= 1
        }
    while count > 0
    
    ```
    
    반복문 제어
    
    break문
    
    break는 반복문을 즉시 종료함
    
    예제
    
    ```swift
     for i in 1...10 {
            if i == 5{
               break
            }
               print(i)
         }
    
    ```
    
    continue문
    
    continue는 현재 반복을 건너뛰고 다음 반복을 실행함
    
    예제
    
    ```swift
    for i in 1...5 {
        if i == 3 {
            continue
        }
        print(i)
    }
    
    ```
    
- 함수
    
    필요성 및 개념설명
    
    필요이유
    
    코드를 작성하다 보면 같은 기능을 여러번 사용해야 하는 경우가 많음
    
    같은 코드를 반복해서 작성하면 유지보수가 어렵고 가독성이 떨어짐
    
    이러한 문제를 해결하기 위해 함수를 사용함
    
    개념과 설명
    
    함수
    
    함수는 특정 기능을 수행하는 코드 블록임
    
    함수는 입력값(매개변수)을 받아 처리 한후 결과값(반환값)을 반환 할수 있음
    
    기본 문법
    
    ```swift
    func 힘수이름(매개변수: 타입) -> 반환타입 {
    			실행할 코드
    			return 반환값
    		}
    ```
    
    예제
    
    ```swift
    func add(a: Int, b: Int) -> Int {
            return a + b
        }
    
    let result = add(a: 3, b: 5)
    print(result)
    ```
    
    반환 값이 없는 함수
    
    ```swift
    func getCurrentYear() -> Int {
        return 2025
    }
    
    let year = getCurrentYear()
    print(year)
    ```
    
    인자 레이블 생략 (_ 사용)
    
    swift 에서는 함수 호출시 인자 레이블을 생락 햘수있음
    
    ```swift
    func greet(_ name: String) {
        print("안녕 \(name)")
    }
    greet("영희")
    ```
    
    중첩 함수
    
    함수 안에 또 다른 함수를 선언할수있음
    
    ```swift
    func outerFunction() {
        func innerFunction() {
            print("내부 함수")
        }
    
        innerFunction()
    }
    
    outerFunction()
    ```
    
    클로저
    
    클로저는 이름이 없는 함수(익명함수)
    
    기본문법
    
    ```swift
    { (매개변수) -> 반환타입 in
        실행할 코드
    }
    ```
    
    예제
    
    ```swift
    let multiply = { (a: Int, b: Int) -> Int in
        return a * b
    }
    
    let result = multiply(3, 4)
    print(result)
    ```
    
    클로저를 함수의 매개변수로 사용
    
    ```swift
    func operateOnNumbers(a: Int, b: Int, operation: (Int, Int) -> Int) -> Int {
        return operation(a, b)
    }
    
    let sum = operateOnNumbers(a: 5, b: 10) { (x, y) in
        return x + y
    }
    
    print(sum)
    ```
    
    범위를 사용한 예제
    
    ```swift
    let number = 7
    	switch number {
    		case 1...5:
    			print("1에서 5 사이")
    		case 6...10:
    			print("6부터 10 사이")
    		default:
    			print("그 외의 숫자")
    		}
    ```
    
    ---
    
- 옵셔널
    
    필요성 및 개념설명
    
    필요이유
    
    swift 에서는 값이 존재하지 않을 수도 있는 변수를 처리해야 하는 경우가 있음
    
    얘를 들어 사용자가 입력한 값이 없거나 특정 연산의 결과가 없을수도 있음
    
    이런 경우 nil값을 처리할 필요가 있음
    
    개념과 설명
    
    옵셔널이란 값이 있을수도 없을수도 있는 타입을 의미
    
    값이 없을 경우 nil이 저장됨
    
    기본 문법
    
    ```swift
    var 변수명: 타입? = 값
    ```
    
    예제
    
    ```swift
    var name: String? = "철수"
    print(name)
    
    name = nil
    print(name)
    ```
    
    옵셔널 바인딩 if let
    
    옵셔널 변수의 값을 안전하게 사용하려면 if let을 사용하여 nil 여부를 확인 해야함
    
    ```swift
    var name: String? = "철수"
    
    if let unwrappedName = name {
        print("이름: \(unwrappedName)")
    } else {
        print("이름이 없음")
    }
    ```
    
    옵셔널 바인딩 guard let
    
     guard let을 사용하면 조건이 충족되지 않을 경우 즉시 함수를 종료함
    
    ```swift
    func printName(_ name: String?) {
        guard let unwrappedName = name else {
            print("이름이 없음")
            return
        }
    
        print("이름: \(unwrappedName)")
    }
    
    printName(nil)
    printName("철수")
    ```
    
    옵셔널 강제 해제
    
    ! 를 사용하면 강제로 값을 추출할수 있지만 값이 nil일 경우 오류가 발생할수있음
    
    ```swift
    var name: String? = "철수"
    print(name!)
    ```
    
    nil 병합 연산자 ??
    
    ?? 연산자를 사용하면 값이 nil일 경우 기본값을 저장할수있음
    
    ```swift
    let userName: String? = nil
    let displayName = userName ?? "게스트"
    
    print(displayName)
    
    ```
    
    ---
    
- 클래스
    
    필요성 및 개념설명
    
    필요이유
    
    프로그램을 작성하다보면 현실 세계의 개념을 코드로 표한해야 할 떄가 많음
    
    예를 들어 학생 자동차 은행 계좌 처럼 속성과 행동이 함께 있는 개념들을 다루어야 함
    
    이떄 이러한 개념들을 표현 하기위해 클래스를 사용함
    
    개념과 설명
    
    클래스
    
    클래스는 속성(프로퍼티)과 기능(메서드)을 정의하는 사용자 정의 타입
    
    클래스를 사용하면 객체지향적으로 프로그램 구성 할수있음
    
    기본 문법
    
    ```swift
    class 클래스명 {
    		var 속성이름: 타입
    		init(초기화할값) {
    				self.속성 = 초기화할값
    				}
    				func 메서드명() {
    					실행할코드
    				}
    			}
    ```
    
    예제
    
    ```swift
    class Person {
        var name: String
        var age: Int
    
        init(name: String, age: Int) {
            self.name = name
            self.age = age
        }
    
        func introduce() {
            print("안녕하세요, 저는 \(name)이고 \(age)살이에요.")
        }
    }
    
    let person1 = Person(name: "철수", age: 21)
    person1.introduce()
    ```
    
    클래스의 특성 
    
    클래스는 참조타입 임
    
    객체를 변수에 할당 하거나 함수에 전달할떄 값이 복사가 되는게 아닌 참조가 전달됨
    
    ```swift
    let person2 = person1
    person2.name = "철수"
    
    print(person1.name)
    ```
    
    클래스의 특성 2
    
    클래스 내부에는 데이터를 저장하는 프로퍼티 , 동작을 수행하는 메서드가 있음
    
    ```swift
    class Cat {
        var name: String = "야옹이"
    
        func meow() {
            print("\(name)가 울어요 미야옹!")
        }
    }
    
    let cat = Cat()
    cat.meow()
    ```
    
    ---
    
- 구조체
    
    필요성 및 개념설명
    
    필요이유
    
    간단한 데이터 집합을 표현하고 싶을때 구조체 사용
    
    값을 복사해서 사용해야 할 경우 즉 독립적인 복사본이 필요할 경우 구조체가 적합함
    
    개념과 설명
    
    구조체
    
    구조체는 클래스처럼 속성과 메서드를 가질수 있지만 값 타입
    
    값타입은 변수나 상수에 할당될떄 값이 복사가 됨
    
    기본 문법
    
    ```swift
    struct 구조체명 {
        var 속성: 타입
        func 메서드명() {
            실행할 코드
        }
    }
    ```
    
    예제
    
    ```swift
    struct Rectangle {
        var width: Double
        var height: Double
    
        func area() -> Double {
            return width * height
        }
    }
    
    let rect = Rectangle(width: 5.0, height: 25.0)
    print("면적은 \(rect.area())")
    
    ```
    
    구조체 특성
    
    구조체는 값 타입이기 때문에 변수에 할당되거나 함수에 전달될떼 값이 복사됨
    
    ```swift
    var rect1 = Rectangle(width: 2.0, height: 50.0)
    var rect2 = rect1
    
    rect2.width = 20.0
    print(rect1.width)
    print(rect2.width)
    ```
    
    구조체의 프로퍼티, 메서드, 이니셜라이저
    
    구조체는 기본적으로 멤버와이즈 이니셜라이즈를 제공
    
    ```swift
    struct User {
        var username: String
    
        func greet() {
            print("만나서 반가워요 \(username)님")
        }
    }
    
    let user = User(username: "페페")
    user.greet()
    ```
    
    ---
    

---

내일배움캠프 사전캠프 1주일차 후기

처음 공부하는거라 당연히 낯설고 어렵지만 재밌음

매일매일 TIL을 작성하니 내가 오늘 어떤 활동을 했는지 또 어떤걸 배웠는지를 명확하게 정리할수 있었음