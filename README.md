### 📌 게시판 프로젝트 (Board Project)
> 이 프로젝트는 스파르타 게시판 과제로 제출한 프로젝트입니다. \
> Spring Boot 기반의 CRUD 게시판이며, 게시글 작성, 수정, 삭제, 댓글 기능을 포함하고 있습니다.

<br/>

### 기술 스택

| 구성 요소  | 기술                      |
| ------ | ----------------------- |
| 언어     | Java 17                 |
| 프레임워크  | Spring Boot 3.x         |
| 빌드 도구  | Gradle                  |
| 데이터베이스 | H2 (In-Memory)          |
| ORM    | Spring Data JPA         |
| 기타     | Lombok, Bean Validation |

<br/>

### 프로젝트 구조

```
src
└── main
    └── java
        └── io/sparta/board              
            ├── app          
            │   ├── domain
            │   │   ├── comment
            │   │   └── post 
            │   │       ├── application   
            │   │       │   ├── facade
            │   │       │   └── usecase           
            │   │       ├── infrastructure
            │   │       │   └── exception
            │   │       ├── model
            │   │       │   ├── entity
            │   │       │   └── repository           
            │   │       ├── controller
            │   │       ├── dto
            │   │       │   ├── request
            │   │       │   └── response       
            │   │       └── mapper
            │
            └── global
                ├── config     
                ├── entity           
                └── exception

└── test
    └── java
        └── io/sparta/board/httpClient          

```

<br/>

### 주요 기능

| 기능        | 설명                   |
| --------- | ------------------------ |
| 게시글 작성 | 게시글 제목, 내용은 필수 항목   |
| 게시글 수정 | 제목과 내용만 수정 가능 |
| 게시글 삭제 | 삭제 시 게시글과 함께 해당 게시글의 모든 댓글도 삭제 처리, soft-delete |
| 게시글 단건 조회  | 게시글에 포함된 모든 댓글 목록을 조회 |
| 댓글 등록  | 댓글 내용은 필수 항목 |
| 댓글 수정  | 댓글 내용만 수정 가능 |
| 댓글 삭제  | 댓글 삭제 시 삭제 상태에 대한 변경만 처리, soft-delete |

<br/>

### 실행 방법

```bash
git clone https://github.com/Yang-Sooyoung/board.git
cd board
./gradlew clean build
```

**애플리케이션 실행 후 접속:**
[http://localhost:8080](http://localhost:8080)

**H2 Console:**
[http://localhost:8080/h2-console](http://localhost:8080/h2-console)

* JDBC URL: `jdbc:h2:mem:testdb`
* User Name: `sa`

<br/>

### 참고자료

* [게시판 과제 개발 가이드](https://github.com/sparta-standard/docs/wiki/게시판-과제-개발-가이드)
* [게시판 과제 제출 가이드](https://github.com/sparta-standard/docs/wiki/게시판-과제-제출-가이드)

</br>

#### 🙋‍♀️ 만든 사람

- 👩‍💻 이름: 양수영 (Yang Sooyoung)
- 🔗 GitHub: [@Yang-Sooyoung](https://github.com/Yang-Sooyoung)

<br/>

