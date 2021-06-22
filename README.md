# 설치 과정
> Simulator 이용
- [참고자료](https://reactnative.dev/docs/environment-setup)
- [(ios 용) Xcode 설치](https://apps.apple.com/us/app/xcode/id497799835?mt=12)
- [(aos 용) 안드로이드 스튜디오 설치](https://developer.android.com/studio)

```
(생략) $ brew install node
$ brew install watchman (혹시 에러나면 가이드대로 특정 폴더 권한 부여)

=========== aos ===============
$ brew install --cask adoptopenjdk/openjdk/adoptopenjdk8
... 추가 작업 

=========== ios ===============
$ sudo gem install cocoapods


=========== 공통 ==============
$ npx react-native init project_name [--version X.XX.X] [--template react-native-template-typescript]
(package.json script command수정 후)
$ cd project_name
$ npm start
(혹은)
$ npm run ios // Xcode Simulator 에 연동되어서 열림.
$ npm run aos // 자바, android studio 등 추가 세팅 필요
```

- package.json 수정  
Q. run-aos, run-ios 을 위한 port 설정 못하나? 근본적인 metro port 설정은 안 바뀌던데

```json
// (default) 8081 은 docker 에서 사용하고 있었음.
"start": "react-native start --port=8088"
```

# 설치과정 2
> expo 를 이용하면 기본 세팅 필요 없음.

```
$ npm install -g expo-cli
$ expo init project_name
$ expo start
```

- aos : Expo Project 앱 깔아서 > Development(localhost:19002) 창에서 뜬 QR 코드 인식
- ios 바로 QR 코드 인식


# Typescript 설정
- [세팅](https://engineering.huiseoul.com/%EB%A6%AC%EC%95%A1%ED%8A%B8%EB%84%A4%EC%9D%B4%ED%8B%B0%EB%B8%8C%EC%97%90%EC%84%9C-%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0-2018-2ea78fe8f553)