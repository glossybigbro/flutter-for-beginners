# 🎯 Flutter for Beginners

노마드 코더의 [Flutter for Beginners](https://nomadcoders.co/flutter-for-beginners) 강의를 수강하며 학습한 내용을 정리한 저장소입니다.

## 📚 강의 소개

Flutter의 기초부터 실전 앱 개발까지 단계별로 학습하는 과정입니다. Dart 언어의 기본 문법부터 시작하여 UI 구성, 상태 관리, API 연동까지 Flutter 개발의 핵심 개념들을 다룹니다.

## 📖 커리큘럼 및 학습 진행 상황

### #1 Introduction

- [x] #1.0 Introduction (03:21)
- [x] #1.1 Requirements (02:05)
- [x] #1.2 Why Flutter (09:43)
- [x] #1.3 How Flutter Works (12:12)
- [x] #1.4 Flutter vs React Native (07:19)
- [x] #1.5 Recap (03:08)

### #2 Hello Flutter

- [x] #2.0 Installation (08:17)
- [x] #2.1 Dart Pad (03:04)
- [x] #2.2 Running Flutter (11:15)
- [x] #2.3 Hello World (15:25)
- [x] #2.4 Recap (05:48)
- [x] #2.5 Classes Recap (08:40)

### #3 UI Challenge ✅

- [x] #3.0 Header (16:47)
- [x] #3.1 Developer Tools (08:06)
- [x] #3.2 Buttons Section (10:42)
- [x] #3.3 VSCode Settings (06:18)
- [x] #3.4 Code Actions (04:27)
- [x] #3.5 Reusable Widgets (14:07)
- [x] #3.6 Cards (13:34)
- [x] #3.7 Icons and Transforms (10:01)
- [x] #3.8 Reusable Cards (14:44)
- [x] #3.9 Code Challenge (04:05)

**📁 프로젝트**: [`packages/ui_challenge`](./packages/ui_challenge)

### #4 Stateful Widgets

- [ ] #4.0 State (07:33)
- [ ] #4.1 setState (04:40)
- [ ] #4.2 Recap (05:04)
- [ ] #4.3 BuildContext (10:18)
- [ ] #4.4 Widget Lifecycle (07:18)

### #5 Pomodoro App

- [ ] #5.0 User Interface (13:35)
- [ ] #5.1 Timer (05:48)
- [ ] #5.2 Pause Play (04:26)
- [ ] #5.3 Date Format (10:27)
- [ ] #5.4 Code Challenge (01:59)

### #6 Webtoon App

- [ ] #6.0 Introduction (05:09)
- [ ] #6.1 AppBar (05:58)
- [ ] #6.2 Data Fetching (11:44)
- [ ] #6.3 fromJson (09:59)
- [ ] #6.4 Recap (06:09)
- [ ] #6.5 waitForWebToons (05:48)
- [ ] #6.6 FutureBuilder (07:05)
- [ ] #6.7 ListView (11:59)
- [ ] #6.8 Webtoon Card (13:55)
- [ ] #6.9 Detail Screen (13:37)
- [ ] #6.10 Hero (04:58)
- [ ] #6.11 Recap (05:30)
- [ ] #6.12 ApiService (10:15)
- [ ] #6.13 Futures (07:48)
- [ ] #6.14 Detail Info (06:10)
- [ ] #6.15 Episodes (15:45)
- [ ] #6.16 Url Launcher (12:31)
- [ ] #6.17 Favorites (17:10)
- [ ] #6.18 Thank You (02:21)

## 🗂️ 프로젝트 구조

이 저장소는 **Melos**를 사용하여 여러 Flutter 앱을 하나의 모노레포(monorepo)로 관리합니다.

```
flutter-for-beginners/
├── packages/
│   ├── ui_challenge/     # #3 UI Challenge 앱
│   └── webtoon/          # #6 Webtoon 앱 (예정)
├── pubspec.yaml          # 루트 패키지 설정
├── melos.yaml            # Melos 설정
└── README.md
```

### 왜 Melos를 사용하나요?

- **여러 앱을 하나의 저장소에서 관리**: 각 챕터별 앱을 독립적으로 개발하면서도 하나의 저장소에서 관리
- **의존성 관리 간소화**: 모든 패키지의 의존성을 한 번에 설치 및 업데이트
- **일관된 개발 환경**: 모든 앱에서 동일한 Flutter 버전과 설정 사용

## 🚀 시작하기

### 필수 요구사항

- **Flutter SDK** 3.10.1 이상
- **Dart SDK** (Flutter에 포함)
- **Melos** (전역 설치 필요)

### 설치 및 설정

1. **저장소 클론**

   ```bash
   git clone https://github.com/YOUR_USERNAME/flutter-for-beginners.git
   cd flutter-for-beginners
   ```

2. **Melos 설치** (처음 한 번만)

   ```bash
   dart pub global activate melos
   ```

3. **모든 패키지 의존성 설치**

   ```bash
   melos bootstrap
   ```

### 앱 실행하기

#### 방법 1: 터미널에서 실행

```bash
# UI Challenge 앱 실행
cd packages/ui_challenge
flutter run

# Webtoon 앱 실행
cd packages/webtoon
flutter run
```

#### 방법 2: Android Studio / VS Code

1. `flutter-for-beginners` 폴더를 IDE에서 열기
2. Run Configuration 생성:
   - **Android Studio**: Run → Edit Configurations → Flutter
   - **VS Code**: `.vscode/launch.json` 설정
3. 각 앱의 `lib/main.dart` 파일을 Dart entrypoint로 지정
4. 실행 버튼 클릭

## 🛠️ Melos 명령어

```bash
# 모든 패키지의 의존성 가져오기
melos get

# 모든 패키지 분석 (린트 체크)
melos analyze

# 모든 패키지 클린
melos clean

# 등록된 패키지 목록 보기
melos list
```

## 📱 프로젝트 상세

### UI Challenge (`packages/ui_challenge`)

Flutter의 기본 위젯들을 활용하여 아름다운 UI를 구현하는 프로젝트입니다.

**주요 학습 내용**:

- `Container`, `Row`, `Column` 등 기본 레이아웃 위젯
- 재사용 가능한 커스텀 위젯 만들기
- `BoxDecoration`을 활용한 스타일링
- `Transform` 위젯으로 애니메이션 효과
- 반응형 디자인 (`Expanded`, `Flexible`)

**구현 기능**:

- 지갑 잔액 표시 헤더
- Transfer/Request 버튼
- 다양한 스타일의 카드 위젯
- 아이콘과 변환 효과

### Webtoon App (`packages/webtoon`) - 예정

웹툰 정보를 API로 가져와 표시하는 앱입니다.

**주요 학습 내용** (예정):

- HTTP 통신 및 API 연동
- JSON 데이터 파싱
- `FutureBuilder`를 활용한 비동기 처리
- 상태 관리
- 네비게이션 및 라우팅
- 로컬 저장소 (즐겨찾기 기능)

## 📝 학습 노트

### Dart 패키지 명명 규칙

Dart에서는 패키지 이름에 **하이픈(`-`)을 사용할 수 없습니다**. 반드시 **언더스코어(`_`)를 사용**해야 합니다.

- ❌ `package:ui-challenge/...`
- ✅ `package:ui_challenge/...`

이는 Dart에서 패키지 이름이 식별자(identifier)로 사용되기 때문입니다. 폴더 이름은 `ui-challenge`로 해도 되지만, `pubspec.yaml`의 `name` 필드와 import 경로에서는 반드시 `ui_challenge`를 사용해야 합니다.

### 텍스트 정렬 팁

크기가 다른 텍스트를 나란히 배치할 때는 `CrossAxisAlignment.baseline`을 사용하면 자연스럽게 정렬됩니다:

```dart
Row(
  crossAxisAlignment: CrossAxisAlignment.baseline,
  textBaseline: TextBaseline.alphabetic,
  children: [
    Text('큰 텍스트', style: TextStyle(fontSize: 36)),
    Text('작은 텍스트', style: TextStyle(fontSize: 18)),
  ],
)
```

### 반응형 버튼 만들기

화면 크기에 따라 유연하게 늘어나는 버튼을 만들려면 `Expanded` 위젯을 사용합니다:

```dart
Row(
  children: [
    Expanded(child: Button(...)),
    SizedBox(width: 16),  // 버튼 사이 간격
    Expanded(child: Button(...)),
  ],
)
```

## 🔗 참고 자료

- [노마드 코더 - Flutter for Beginners](https://nomadcoders.co/flutter-for-beginners)
- [Flutter 공식 문서](https://docs.flutter.dev/)
- [Dart 공식 문서](https://dart.dev/)
- [Melos 문서](https://melos.invertase.dev/)

## 📄 라이선스

이 프로젝트는 학습 목적으로 만들어졌습니다.

---

**⭐ 학습 진행 중**: 이 저장소는 지속적으로 업데이트됩니다!
