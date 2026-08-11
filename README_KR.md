# 햄만이톡 (red) — Android Theme Project

이 프로젝트는 업로드된 iOS `.ktheme`의 이미지/색상 구성을 Android 카카오톡 사용자 테마 프로젝트 구조로 옮긴 개인 사용용 작업본입니다.

## 원본
- `햄만이톡 _red_.ktheme`

## 중요한 점
- Android 카카오톡 사용자 테마는 APK 형태로 빌드/서명하여 설치하는 방식입니다.
- Android 공식 사용자 테마 가이드 기준(11.4.0)의 `src/main/theme`, `values`, `drawable-xxhdpi` 구조를 사용했습니다.
- iOS의 말풍선 PNG에는 Android용 9-patch 메타데이터가 없으므로, 변환 과정에서 기본 9-patch 경계를 자동 생성했습니다. 기기별 말풍선 늘어남은 실제 APK에서 확인/조정이 필요할 수 있습니다.
- iOS와 Android는 UI 구조가 달라서 100% 동일한 화면을 보장할 수 없습니다.

## Android Studio에서 빌드
1. 이 폴더를 Android Studio에서 엽니다.
2. JDK 17 및 Android SDK 34를 준비합니다.
3. Gradle sync 후 `Build > Generate Signed Bundle / APK > APK`로 서명된 APK를 생성합니다.
4. 생성된 APK를 휴대폰으로 옮겨 설치합니다.
5. 카카오톡 `더보기 > 설정 > 테마`에서 테마를 선택합니다.

## 패키지
`com.kakao.talk.theme.hammanitokred`

## 원본 파일 매핑
- `mainBgImage@3x.png` → `theme_background_image.png`
- `maintabBgImage@3x.png` → `theme_maintab_cell_image.png`
- Friends/Chats/OpenChats/Shopping/More 아이콘 → Android `theme_maintab_*` 리소스
- `chatroomBgImage@3x.png` → `theme_chatroom_background_image.png`
- Send/Receive bubble 이미지 → `theme_chatroom_bubble_me/you_*_image.9.png`
- Passcode 이미지 → `theme_passcode_*`
- `profileImg01.png` → `theme_profile_01_image.png`

## 색상
원본 CSS의 핵심 포인트인 `#ff2507` / `#ffffff` / `#000000`을 Android 색상 리소스에 반영했습니다.
