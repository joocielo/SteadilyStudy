# javascript

### 모듈
	프로그램이 크고 복잡해지면 코드의 재활용성, 유지보수를 쉽게 하기위해 코드를 여러개의 파일로 분리한다.
	- 재활용, 개선에 용이함
	- 코드 수정시에 필요한 로직을 빠르게 찾을 수 있음
	- 필요한 로직만 로드하여 메모리 낭비 줄임
	- 브라우저의 경우 한번 다운로드 된 모듈이 저장되기 때문에 로직을 로드할때 시간, 네트워크 트래픽을 절약할 수 있음



**모듈이란**

순수한 자바스크립트에서는 모듈이라는 개념이 분명하진 않음. 그러나 자바스크립트가 구동되는 호스트 환경에 따라서 서로 다른 모듈화 방법이 제공됨. 여기서는 대표적인 호스트 환경인 웹브라우저에서 로직을 모듈화하는 방법에 대해서 배움.



**모듈이 없다면**

여러번 사용되는 함수의 경우 정의해서 사용하는 경우 유지보수도 어렵고 낭비가 될 것이다. 이때 모듈이 필요하다.



**모듈의 사용**

자주사용하는 함수를 외부 파일로 분리후, script태그로 불러온다. script태그는 HTML파일에서 해당 컨텐츠를 브라우저에 의해 javascript로 인식할 수 있게 한다.

	greeting.js
	```javascript
	function welcome(){
    return 'Hello world';
	}
	```

	main.html
	```html
	<!DOCTYPE html>
	<html>
	<head>
	    <meta charset="utf-8"/>
	    <script src="greeting.js"></script>
	</head>
	<body>
	    <script>
	        alert(welcome());
	    </script>
	</body>
	</html>
	```



**Node.js에서의 모듈의 로드**

호스트 환경에 따라서 모듈을 로드하는 방법이 달라짐
var circle = require('.node.circle.js');



**라이브러리**

라이브러리는 모듈과 비슷한 개념. 모듈이 프로그램을 구성하는 작은 부품으로서의 로직이라면 라이브러리는 자주 사용되는 로직을 재사용하기 편리하도록 잘 정리한 코드들의 집합. ex)jQuery