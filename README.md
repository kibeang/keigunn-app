# ⚖️ 계근 앱 - Android APK 빌드

## 🚀 APK 받는 방법 (GitHub Actions 사용 — 무료)

### 1단계: GitHub 계정 만들기
👉 https://github.com/signup (무료)

### 2단계: 새 저장소 만들기
1. https://github.com/new 접속
2. Repository name: `keigunn-app` 입력
3. **Private** 선택 (내 코드 비공개)
4. **Create repository** 클릭

### 3단계: 이 폴더를 GitHub에 올리기
PC에서 `명령 프롬프트(cmd)` 열고:

```
cd 이-폴더-경로
git init
git add .
git commit -m "계근 앱 첫 업로드"
git branch -M main
git remote add origin https://github.com/내아이디/keigunn-app.git
git push -u origin main
```

### 4단계: APK 다운로드
1. GitHub 저장소 페이지 → **Actions** 탭 클릭
2. `Build APK` 워크플로우 → 최신 실행 클릭
3. 하단 **Artifacts** 섹션에서 `계근앱-APK` 다운로드
4. ZIP 파일 안의 `app-debug.apk` 를 안드로이드에 설치!

---

## 📱 안드로이드에 설치하기

1. 안드로이드 **설정** → **보안** → **알 수 없는 소스 허용** 켜기  
   (또는 설정 → 앱 → 특별한 앱 접근 → 알 수 없는 앱 설치)
2. `app-debug.apk` 파일을 안드로이드로 전송 (카카오톡, 이메일, USB 등)
3. 파일 탭에서 APK 파일 클릭 → 설치

---

## 📲 앱 사용법

- **기사 앱**: 입차 → 상차완료 → 출차 순서로 터치
- **지게차 앱**: 기사 입차 시 자동 알림 수신, 상차완료 처리

두 앱이 **같은 Wi-Fi + 같은 서버(PC)**에 연결되어 있을 때 실시간 연동됩니다.

---

## 📁 파일 구조
```
keigunn-android/
├── app/src/main/
│   ├── assets/          ← 기사앱·지게차앱 HTML
│   ├── java/.../        ← Android 앱 코드
│   └── AndroidManifest.xml
├── .github/workflows/   ← 자동 빌드 설정
└── README.md
```
