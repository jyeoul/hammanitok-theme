# 햄만이톡 Android 테마 - APK 빌드 안내

이 프로젝트는 카카오톡 Android 사용자 테마 APK 제작을 위한 Android Studio 프로젝트입니다.
카카오 공식 사용자 테마 가이드의 `src/main/theme` 및 `src/main/theme-adv` 리소스 구조를 따릅니다.

## 가장 쉬운 방법: Android Studio

1. Android Studio에서 이 폴더를 엽니다.
2. Gradle Sync가 끝날 때까지 기다립니다.
3. `Build > Build Bundle(s) / APK(s) > Build APK(s)`를 선택합니다.
4. 생성된 APK는 다음 위치에서 찾을 수 있습니다.
   `app/build/outputs/apk/debug/app-debug.apk`
5. APK를 Android 휴대폰으로 옮겨 설치합니다.
6. 카카오톡에서 테마를 적용합니다.

## 명령줄

JDK 17과 Android SDK가 설치되어 있다면 Gradle 8.7으로 다음 명령을 실행할 수 있습니다.

```bash
gradle assembleDebug
```

## GitHub Actions

`.github/workflows/build-apk.yml`이 포함되어 있습니다.
GitHub 저장소에 프로젝트를 올린 뒤 **Actions > Build KakaoTalk Theme APK > Run workflow**를 실행하면 APK가 Artifact로 생성됩니다.

## 주의

- 이 프로젝트는 개인 사용 목적의 변환본입니다.
- iOS `.ktheme`와 Android 테마는 리소스 규격이 달라 말풍선의 9-patch 영역 등 일부 요소는 Android 기기에서 추가 조정이 필요할 수 있습니다.
- 패키지명은 테마 간 충돌을 피하기 위해 red/white가 서로 다르게 설정되어 있습니다.
