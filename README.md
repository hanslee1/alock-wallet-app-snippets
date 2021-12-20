# 에이락 월렛 ALock Wallet (Lite)

- [에이락 월렛](https://www.alock.co.kr/)은 가상자산 리워드 서비스를 제공하는 앱으로, Ionic 5 기반 앱을 React Native로 개선하는 프로젝트에 참여하였습니다.
- 실제 앱 개발 프로젝트는 아직 진행 중이며, 본 repository는 인턴 3명이 4주간 작업한 내용을 결합한 lite 버전입니다.
- 기간 : 2021.11.15 ~ 2021.12.09
- 인원 : 3명

<br/>

## :computer: 사용 기술 및 개발 환경

|       분류       |   사용 언어 혹은 기술   |
| :--------------: | :---------------------: |
|       언어       |       **TypeScript**        |
|      프론트엔드       |       **React Native**, **React Navigation**, **React Hooks**, **Styled Components**  |
|   런타임 환경    |         **Node.js**         |
|   버전관리 툴    |    **Git, GitHub**    |
|       IDE        |   **Visual Studio Code**    |
| 커뮤니케이션       | **Slack, Notion**           |
|      그 외       | **ESLint, Prettier, Babel** |

<br/>

## 👨‍👩‍👧‍👦 Team

- [김지현](https://github.com/jihnk) : Menu(메뉴) & QrRead(QR 코드 스캔) 스크린 구현
- [이성재](https://github.com/sjhanslee) : Onboarding(온보딩), AppVersionInfo(앱 버전 정보) & InquiryConfirmation(1:1 문의 등록 완료) 스크린 및 OnboardingItem 컴포넌트 구현
- [이욱창](https://github.com/wook95) : Splash(스플래시) & Inquiry(1:1 문의 등록) 스크린 구현

<br/>

## 📑 구현 기능 상세

### 1. 공통 구현 사항

- `OnboardingItem`
  - 온보딩 및 각 "완료" 스크린에 사용되는 카드 컴포넌트를 가변적으로 구현

### 2. Splash Screen (스플래시)

- `react-native-splash-screen` 라이브러리와 ios, android 네이티브로 처음 등장하는 배경을 만들어 구현

### 3. Onboarding Screen (온보딩)

- 자동, 수동 스크롤 가능한 온보딩 스크린 구현
- 자동 스크롤 시 `react-spring`을 활용한 crossfading 이미지 구현
- 수동 스크롤 시 `Animated` API의 interpolation을 활용한 이미지 구현
- `AsyncStorage`를 사용하여 앱 첫 launch 시에만 보이게 설계

### 4. Menu Screen (메뉴)

- `react-navigation` 라이브러리를 이용한 스크린 이동 구현
- `react-native-share` API를 활용한 공유기능 구현
- `<ScrollView>`를 활용한 배너 캐러셀 구현
- `<FlatList>`를 활용한 dropdown 메뉴 구현
- Submenu와 dropdown을 컴포넌트화하여 toggle 기능 구현

### 5. QR Code Scan Screen (QR 코드 스캔)

- `react-native-qrcode-scanner` 라이브러리를 활용한 QR 코드 스캔 화면 구현
- `react-navigation` 라이브러리를 이용한 스크린 이동 구현
- `<ImageBackground>`를 활용하여 View 구현

### 6. Inquiry Screen (1:1 문의 등록)

- UX를 고려하여 자동 focusing 기능 구현

### 7. Inquiry Confirmation Screen (1:1 문의 등록 완료)

- `OnboardingItem`을 활용한 등록 완료 스크린 구현

### 8. App Version Info Screen (앱 버전 정보)

- `react-native-version-check` 라이브러리를 통해 사용 중인 앱 버전과 최신 앱 버전을 비교
- 두 버전이 다를 시 OS에 따라 Apple App Store 혹은 Google Play Store로 이동하는 '업데이트' 버튼을 조건부 렌더링으로 구현
- Device에 Store 앱이 없을 시 웹 스토어로 이동하게끔 예외처리

<br/>

## ※ References

- 본 repository는 [(주)에이락](https://a-fun.co.kr/)에 사전 허가를 받은 후에 만들었습니다. 이 코드를 활용하여 상업적인 이득을 취하거나 무단으로 배포할 경우에는 법적으로 문제 될 수 있습니다.
