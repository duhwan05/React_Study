---

<aside>
💡 **리액트 프로젝트 생성**

리액트 프로젝트를 생성할 때 우리는 명령어를 사용하여 프로젝트를 생성하게 된다.

**관련 명령어>**
1. **‘npx create-react-app’** = npx를 사용하여 create-react-app 패키지를 실행합니다. npx는 설치되지 않는 npm 패키지를 일시적으로 다운로드하여 실행할 수 있는 도구입니다.

2. **‘npm init react-app’** = npm init 명령어의 하위 명령어로 create-react-app을 실행합니다. npm init은 다양한 초기화 명령어를 포함하고 있습니다.

**차이점** 🤚
**npm init** 는 새로운 Node.js 프로젝트를 시작할 때 사용되며, package.json 파일을 생성하는데 중점을 둡니다. 

**반면에** **npx create-react-app**은 애플리케이션을 빠르게 생성하기 위한 명령어로, create-react-app 패키지를 실행하여 초기 프로젝트와 설정을 자동으로 생성합니다.

</aside>

<aside>
💡 **컴포넌트(Component)**

프로젝트를 생성하고 나서 **npm start**를 하는 순간 **index.js**가 우선적으로 실행된다.

리액트에서는 보통 컴포넌트를 만들어야하는데 **크게 2가지**로 만들수있다. **함수형 컴포넌트**와 **클래스형 컴포넌트**이다.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f761dc0d-dc23-45fa-adf3-b2f18e942bfe/07d2ad87-8764-49db-8e48-08ff0724f0b1/Untitled.png)

여기서 **컴포넌트(Component)란..?** >> **입력을 받아 출력하는 역할**

리액트는 Component 기반의 구조라는 특징을 가지고 있다.
리액트는 모든 페이지가 Component로 구성되어 있고 하나의 Component는 또 다른 여러개의 Component의 조합으로 구성될 수 있다.
이러한 Component들의 마치 레고 블록을 조립하듯 끼워 맞춰 새로운 Component를 만들 수 있다.

**<Component 사용시 장점>**
1. 코드 양을 줄일 수 있다.
2. 개발 시간을 줄일 수 있다.
3. 유지 보수 비용이 줄어든다.

---

### 라우터란?

페이지를 만들기 위해서는 먼저 **라우터**를 준비해야 합니다. 설치를 위해 새로운 터미널을 열고 설치합니다. 터미널이 열리면 워크스페이스로 설정되어 있으므로, 사용할 폴더로 이동한 후에 설치를 진행해야 합니다.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f761dc0d-dc23-45fa-adf3-b2f18e942bfe/6dee6da8-535d-4c9c-a496-1608598240b8/Untitled.png)

이처럼 **cd “이동할 폴더”** 명령어를 쓰면 그 폴더로 이동하고
이후에 **npm install react-router-dom@6**을 입력해준다.
여기서 **@6**은 **버전**이다.

이렇게 설치를 끝내면 라우팅을 할 준비를 끝낸것이다. 그래서 라우팅은 무엇인가?

**라우팅**은 **URL 경로에 따라 다양한 페이지를 로드하는 기능이다.** 

웹사이트는 각 페이지가 고유한 URL 경로를 가지며, 경로 변경에 따라 페이지 콘텐츠가 바뀐다. 리액트를 사용하지 않으면, 서버에서 HTML 파일을 다시 보내어 콘텐츠를 보여주지만, URL 변경마다 앱을 종료해야 한다. 
이 때문에 **SPA**(**S**ingle **P**age **A**pplication)를 사용하며, 사용자는 JavaScript를 통해 URL과 경로를 조작하고 콘텐츠를 바꿀 수 있다. 리액트에서는 URL 확인, 라우팅, 컴포넌트 로딩 등을 브라우저에서 수행하며, 이를 위해 코드 작성이나 third party 패키지 사용이 필요하다. React Router 패키지는 이런 작업을 지원한다.

---

### **export default 란?**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f761dc0d-dc23-45fa-adf3-b2f18e942bfe/0659bde7-08d4-40e8-9a67-5ad3370e28b3/Untitled.png)

보통 함수형 컴포넌트를 만드는 이유는 다른 곳에서 가져다 쓰기 위함인데 **마지막 줄인 export default 줄을 작성하지 않으면 다른 곳에서 사용할수가 없으니 주의해야한다.**

---

### 함수 선언 방식

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f761dc0d-dc23-45fa-adf3-b2f18e942bfe/2e60b608-55c4-4d1c-b44d-310dcbcb329f/Untitled.png)

### **주요 차이점 요약:**

- **함수 정의 방식**:
    - 첫 번째 코드는 **화살표 함수(**arrow function)를 사용하여 컴포넌트를 정의합니다.
    - 두 번째 코드는 **전통적인 함수 선언 방식**(function declaration)을 사용하여 컴포넌트를 정의합니다.
- **화살표 함수 vs. 전통적인 함수**:
    - **화살표 함수**: 간결한 문법을 제공하며, 특히 this 바인딩의 차이로 인해 **클래스 메서드나 콜백 함수**에서 많이 사용됩니다.
    - **전통적인 함수 선언**: 더 명시적이고, 함수 선언을 호이스팅(hoisting)합니다. 즉, **함수 선언 전에 호출할 수 있습니다.**
    
    ---
    
    ### 라우팅 사용방법
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f761dc0d-dc23-45fa-adf3-b2f18e942bfe/29f10432-01c3-49c5-aa2d-9e07c36ad1f5/Untitled.png)
    
    한 화면에서 다른 페이지를 불러와 표시하고 싶을 때는 라우팅을 사용하는데, 방법은 매우 간단합니다.
    nav 태그 안에 Link 태그를 사용하여 불러올 다른 페이지를 지정하고,
    아래에는 Routes 태그 안에 Route 태그를 사용하여 페이지를 설정합니다.
    **간단히 말해, Link의 'to'가 Routes의 'path'와 일치하면, 해당 element 주소를 요청하는 방식입니다.**
    
    ---
    
    ### State 변경에 대해서..
    
    우리는 state를 사용해 변수들을 저장하는데 state를 변경할 일들이 생깁니다. 하지만 state를 직접 변경할 경우 자바스크립트는 Heap 메모리에 있는 state가 변경 된것을 알아차리지 못하기 때문에 다른 방식으로 state를 변경해야 합니다.
    
    **예시)**
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f761dc0d-dc23-45fa-adf3-b2f18e942bfe/e50c0b42-685f-4207-80a3-0c1b2ffc6613/Untitled.png)
    
    useState를 사용하여 빈 문자열을 할당하고, 각각에 대해 inputs를 할당하여 복사합니다. 그 후, 입력란에서 작성된 내용들을 id와 value로 매칭하여 **inputs에 재할당하면** **state 상태가 변경**됩니다. 
    여기서 **...**은 **inputs 배열에 있는 데이터들을 분해하여 새로운 배열을 생성하는 것입니다.**
    
    ---
    
</aside>
