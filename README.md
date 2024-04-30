# React + Nginx + Docker 로 App 실행

> 해당 자료는, React App을 Nginx를 이용하여 Docker로 실행하는 방법을 설명합니다.
> "웹 화면이 보이기 전까지 어떤일이 일어날까?"에 대한 발표자료로 사용하기 위함입니다.
> Network에서 보이는 "요청", "응답"에 대한 것을 순차적으로 바라보고 
> 그 과정에서 받아오는 HTTP Data가 어떻게 처리되는지를 확인합니다. ( Content-Type Kinds )


### ```React App``` Install
```bash
$ npm install 
```

### ```React App``` Docker Image Build
```bash
$ docker build -t react-app .
```

### ```Nginx``` Docker Run
```bash
$ docker run -d -p 80:80 --name react-app react-app
```
- 이후 브라우저에서 ```http://localhost```로 접속하여 확인합니다.