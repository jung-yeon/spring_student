# spring_student
## 학생 정보를 등록, 조회, 수정할 수 있는 Controller를 구현하라.

<ul>프로젝트 구성
<li>maven project</li>
<li>packaging: war</li>
<li>Spring MVC 사용</li>
<li>WebApplicationInitializer 이용해서 web.xml 파일이 없도록 한다.</li></ul>
</br>
<ul>클래스 작성 기본적으로 아래 3개의 클래스를 구현하여야 하고
<li>StudentRegisterController</li>
<li>StudentController</li>
<li>StudentRepositoryImpl</li>
<li>필요 시 클래스를 추가로 생성해도 무방함.</li>
<li>과제 내용과 관련없는 코드가 포함되어 있으면 안 된다.</li></ul>
</br>
<ul>Model 관련
<li>@ModelAttribute의 2가지 사용 방법을 모두 쓸 것</li>
<li>Model, ModelMap, ModelAndView를 각각 최소 1번 이상 사용할 것</li>
<li>GET /student/{studentId}?hideScore=yes</li>
<li>이 경우에는 점수와 평가 항목을 출력하지 않는다</li>
<li>GET /student/{studentId}와는 다른 별도의 Controller Method로 작성한다</li>
<li>등록, 수정 시 아래 조건으로 입력 폼을 검증해야 한다.</li>
<li>이름: 공백 제거 후 문자열의 길이가 0보다 커야 함</li>
<li>이메일: 이메일 형식이 맞아야 함</li>
<li>점수; 0점 이상 100점 이하</li>
<li>평가: 공백 제거 후 문자열의 길이가 0보다 크고 200보다 같거나 작아야 함</li></ul>
</br>
<ul>에러 처리는 다음의 조건을 만족해야 한다.
<li>다음 URL 접근 시 없는 리소스에 대한 접근일 경우 Controller 기반 예외 처리 방법을 이용해서 Http Status Code 404로 응답한다</li>
<li>GET /student/{studentId}</li>
<li>GET /student/{studentId}/modify</li>
<li>그 외의 예외는 @ControllerAdvice를 이용해서 예외 처리를 해야 한다.</li></ul>
</br>
<ul>REST API 에 대해
<li>학생 정보 등록: POST /studens</li>
<li>학생 정보 조회: GET /students/{studentId}</li>
<li>학생 정보 수정: PUT /students/{studentId}</li></ul>

### home
<img width="1440" alt="스크린샷 2022-12-27 오후 1 43 02" src="https://user-images.githubusercontent.com/77679326/209613579-7e8b5423-4b49-4ae8-aec0-257a8dfda9df.png">

### 다국어 처리
<img width="1440" alt="스크린샷 2022-12-27 오후 1 43 07" src="https://user-images.githubusercontent.com/77679326/209613637-227abd69-13e1-4b32-aac0-7f6d5605212d.png">

### 로그인 성공 화면
<img width="1440" alt="스크린샷 2022-12-27 오후 1 43 22" src="https://user-images.githubusercontent.com/77679326/209613706-9d034227-ad16-4687-9fac-e3fdf33499de.png">

### 학생 정보 등록 화면
<img width="1440" alt="스크린샷 2022-12-27 오후 1 44 11" src="https://user-images.githubusercontent.com/77679326/209613808-368ed924-c457-48dc-b7fb-0ad1c3ca1cbd.png">

### 학생 정보 조회 화면(점수O)
<img width="1440" alt="스크린샷 2022-12-27 오후 1 44 15" src="https://user-images.githubusercontent.com/77679326/209613832-87704369-06e0-460a-b0ef-48db076b1935.png">

### 학생 정보 조회 화면(점수x)
<img width="1440" alt="스크린샷 2022-12-27 오후 1 44 29" src="https://user-images.githubusercontent.com/77679326/209613961-e9964896-fba2-4948-ae90-64b002b69a7d.png">

### 학생 정보 수정
<img width="1440" alt="스크린샷 2022-12-27 오후 1 44 39" src="https://user-images.githubusercontent.com/77679326/209613981-331d16c2-07aa-4bfb-8839-76ae9eb5b1a6.png">

### 학생 정보 수정 후 화면
<img width="1440" alt="스크린샷 2022-12-27 오후 1 44 43" src="https://user-images.githubusercontent.com/77679326/209614039-ee3365a3-dcfa-4c9e-90c1-f9e852e9122e.png">
