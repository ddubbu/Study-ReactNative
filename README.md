# 설치 과정

- [참고자료](https://reactnative.dev/docs/environment-setup)
- [(ios 용) Xcode 설치](https://apps.apple.com/us/app/xcode/id497799835?mt=12)
- [(aos 용) 안드로이드 스튜디오 설치](https://developer.android.com/studio)

```
(생략) $ brew install node
$ brew install watchman (혹시 에러나면 가이드대로 특정 폴더 권한 부여)

=========== aos ===============
$ brew install --cask adoptopenjdk/openjdk/adoptopenjdk8

=========== ios ===============
$ sudo gem install cocoapods
$ npx react-native init project_name [--version X.XX.X] [--template react-native-template-typescript]
(package.json script command수정 후)
$ cd project_name
$ npm start
(혹은)
$ npm run ios // Xcode Simulator 에 연동되어서 열림.
$ npm run aos // 왜 에러나지?
```

- package.json 수정

```json
// (default) 8081 은 docker 에서 사용하고 있었음.
"start": "react-native start --port=8088"
```
