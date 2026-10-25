# 수도권 온에어 FM 라디오 (Seoul On-Air FM Radio Android APK Project)

수도권 주요 FM 라디오 18개 채널(KBS, MBC, SBS, EBS, TBS, YTN, 국악, CBS, 극동, 불교, 평화) 실시간 청취 및 **실시간 오디오 지문 인식(5초 샘플링) + LRCLIB 싱크 가사 하이라이트 + Android Auto + Jetpack Glance 홈 화면 위젯**을 모두 지원하는 Kotlin + Jetpack Compose + Media3 프로젝트입니다.

## 주요 구현 사양
1. **다크 글래스모피즘 UI & 아날로그 FM 다이얼 바**
   - `88.0MHz ~ 108.0MHz` 부드러운 바늘 포인터 이동 애니메이션 및 5바 오디오 이퀄라이저
   - 취침예약 타이머 모달(15/30/45/60/90분), 커스텀 `.m3u8`/`.mp3` URL 저장 모달, GitHub Actions 빌드 가이드 모달
2. **KBS · MBC · SBS 동적 토큰 스트림 Resolver (`StationRepository.kt`)**
   - SBS 파워FM/러브FM, MBC 표준FM/FM4U, KBS 1·2·쿨·클래식FM 실시간 토큰 `.m3u8` 자동 추출
3. **5초 오디오 샘플링 지문 인식 & LRCLIB 실시간 싱크 가사 (`SongAndLyricsService.kt`)**
   - 3.5초 간격 자동 하이라이트 및 스크롤, 가사 집중 모드 및 클립보드 전체 복사
4. **Android Auto (`MediaLibraryService`) & 홈 화면 위젯 (`RadioWidgetReceiver.kt`)**
   - 차량용 Android Auto에서 채널 탐색/재생 및 바탕화면 Jetpack Glance 위젯에서 즉시 주파수 변경
