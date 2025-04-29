# [TIL] 2일차

---

안녕하세요 오늘은 내일배움캠프 사전캠프 2일차 TIL 입니다.

오늘 배운 내용은 틀래스와 구조체 입니다.

[클래스 개념]

---

클래스(Class) 속성과 기능을 정의하는 사용자 정의 타입

클래스를 사용하면 객체지향적으로 프로그램을 구성 할수있음

클래스 기본문법

```swift
class 클래스이름 {
      var 속성이름: 타입
      init(초기화할값) {
           self.속성 = 초기화할값
        ]
        func 메서드이름() {
             실행할 코드
         }
       }
```

---

**문제 풀어보기**

- 문제 1

       학생 정보를 저장하고 자기소개를 출력하는 **Student** 클래스를 작성하세요.

      요구사항: name과 school 프로퍼티를 갖고 있어야 하고 introduce() 메서드는 자기소개 문장을 출력해야함

- 풀이

```swift
class Student {
      var name: String
      var school: String
      
      init(name: String, school: String) {
          self.name = name
          self.school = school
         }
         
      func introduce() {
           print("안녕하세요 저는 \(school)에 다니는 \(name)입니다")
         }
       } 
       
    let student = Student(name: "영희", school: "한국고등학교")
         student.introduce()
         
```

출력값

```swift
안녕하세요 저는 한국고등학교에 다니는 영희입니다
```

- 문제 2

      Car 클래스를 만들어 자동차의 현재 속도를 출력하는 메서드를 작성하세요.

     요구사항: brand , speed 라는 프로퍼티를 가지고 있어야하고

     describe() 메서드는 브랜드명과 속도를 출력해야함

- 풀이

```swift
class Car {
      var brand: String
      var speed: Int
      
      init(brand: String, speed: Int) {
          self.brand = brand
          self.speed = speed
         }
         
       func  describe() {
           print("현재 속력은\(speed)km/h이고 브랜드는 \(brand)입니다.")
         }
       } 
       
    let car = Car(brand: "벤츠", speed: 70)
         car.describe()
```

출력값

```swift
현재 속력은70km/h이고 브랜드는 벤츠입니다.
```

- 문제 3

      BankAccount 클래스를 작성해서 입출금 기능을 구현하세요.

     요구사항: owner , balance 프로퍼티가 있어야함 

    deposit(amount:)과 withdraw(amount:) 메서드를 통해 잔액을 변경할수있어야함

   출금시 잔액이 부족하면 “잔액부족” 메시지를 출력해야함

```swift
class BankAccount {
    var owner: String
    var balance: Int

    init(owner: String, balance: Int) {
        self.owner = owner
        self.balance = balance
    }

    func deposit(amount: Int) {
        balance += amount
        print("\(amount)원을 입금했습니다. 현재 잔액: \(balance)원")
    }

    func withdraw(amount: Int) {
        if amount > balance {
            print("잔액 부족")
        } else {
            balance -= amount
            print("\(amount)원을 출금했습니다. 현재 잔액: \(balance)원")
        }
    }
}

let account = BankAccount(owner: "철수", balance: 10000)
account.deposit(amount: 5000)
account.withdraw(amount: 12000)
account.withdraw(amount: 8000)
```

출력값

```swift
5000원을 입금했습니다. 현재 잔액: 15000원
12000원을 출금했습니다. 현재 잔액: 3000원
잔액 부족
```

---

[구조체 개념]

---

구조체는 클래스처럼 속성과 메서드를 가질 수 있지만, **값 타입**

값 타입이란 변수나 상수에 할당될 때 **값이 복사** 된다는 뜻이에요.

구조체 기본 문법

```swift
struct 구조체이름 {
    var 속성: 타입
    func 메서드이름() {
        실행할 코드
    }
}
```

---

문제 풀어보기

- 문제 1

      **책 정보를 저장하는** Book **구조체를 작성하세요.**

     **요구사항: title과 author 프로퍼티를 갖고 있어야 하고  description() 메서드는 책 정보를 출력해야 해요.**

```swift
struct Book {
    var title: String
    var author: String

    func description() {
        print("책 제목: \(title), 저자: \(author)")
    }
}

let book = Book(title: "내배캠 기록", author: "페페")
book.description() 
```

결과값

```swift
책 제목: 내배캠 기록, 저자: 페페
```

- 문제 2

      **Point 구조체를 만들어 좌표를 표현하고, 두 점 사이의 거리를 계산하는 메서드를 작성하세요.**

     **요구사항: x, y 프로퍼티를 갖고 있어야 함 , distance(to:) 메서드는 다른 점과의 거리를 반환해야 함**

                   피타고라스 정리를 사용해야 함

```swift
import Foundation

struct Point {
    var x: Double
    var y: Double

    func distance(to other: Point) -> Double {
        let dx = x - other.x
        let dy = y - other.y
        return sqrt(dx * dx + dy * dy)
    }
}

let p1 = Point(x: 0, y: 0)
let p2 = Point(x: 3, y: 4)
print(p1.distance(to: p2))
```

결과값

```swift
5.0
```

- **Movie 구조체를 만들어 영화 정보를 저장하고 별점을 계산하는 메서드를 작성하세요.**

      요구사항:title, ratingTotal, ratingCount 프로퍼티를 갖고 있어야 함

                   averageRating() 메서드는 평균 평점을 Double로 반환해야 함

                  ratingCount가 0일 경우 0.0을 반환해야 함

```swift
struct Movie {
    var title: String
    var ratingTotal: Int
    var ratingCount: Int

    func averageRating() -> Double {
        if ratingCount == 0 {
            return 0.0
        }
        return Double(ratingTotal) / Double(ratingCount)
    }
}

let movie = Movie(title: "스위프트의 정석", ratingTotal: 85, ratingCount: 20)
print(movie.averageRating()) 
```

결과값

```swift
4.25
```

---

# TMI

Swift가 처음이라 아직 문법이 익숙하지 않음

다음 챕터 넘어가기에는 부족한 점이 많아 재수강 필요함 

 이번주에는 문법개념 이해를 목표로 공부하겠음
