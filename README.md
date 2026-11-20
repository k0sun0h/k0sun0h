# 김선혜 — 드론·로봇 소프트웨어 지향

센서 데이터 처리·비전·자율비행을 목표로 하는 컴퓨터SW학과 학부생입니다.
웹 → 앱 → 백엔드/AI → 로봇 순으로 영역을 넓히며, **"입력 → 처리 → 출력" 파이프라인** 관점으로 프로젝트를 봐왔습니다.

- 정보처리기사 (2026.09) · 초경량비행장치 조종자 (2026.08)
- 학점 4.02 / 4.5 (수원대학교 컴퓨터SW학과, 2027.02 졸업예정)

## 로봇·드론 (지원 직무 핵심)

### [ROS2·OpenCV 객체 추적 및 처리 성능 분석](https://github.com/k0sun0h/ros2-opencv-demo)
`2026.10.13 ~ 10.28 · 개인 · Python/ROS2 Humble/OpenCV`
- ROS2 발행-구독 파이프라인으로 영상 객체 검출·추적, 입력 주파수별 처리 성능 측정
- launch 인자가 영상 발행 노드에 적용되지 않던 **발행 주기 오류 수정** (fps 파라미터 전달 누락)
- WSL2 CLI 데몬 hang 이슈 회귀 — **토픽을 직접 구독해 세는 검증 노드**로 측정 정확도 확보
- 실측: 10Hz 입력 99%(119/120), 28.7Hz 입력 79%(188/238), **44ms/frame ≈ 22.5Hz 처리 한계**

### [ROS2·slam_toolbox 2D 매핑 및 통신 진단](https://github.com/k0sun0h/ros2-slam-demo)
`2026.10.28 ~ 11.04 · 개인 · Python/ROS2/slam_toolbox/RViz`
- 오도메트리에 의도적 3% 오차를 주입한 가짜 로봇 노드로 SLAM 보정 동작 검증
- 0.05m 해상도 189×163 격자 지도 생성·저장(PGM/YAML), 5Hz 수신 빈도 검증
- DDS 구현 비교 실험(FastDDS 55.6% vs CycloneDDS 5.1%) — **"메시지 수신 ≠ 정상 매핑"** 발견, 원인 미확정 부분은 한계로 명시

## 백엔드·AI

### [Mobility Bridge — 교통약자 AI 이동지원 서비스](https://github.com/k0sun0h/mobility-bridge)
`2026.04 ~ 06 · 2인 팀 · 백엔드+AI 전담 · FastAPI/PostgreSQL/RandomForest/SHAP`
- 공공 API 4종 통합·정규화, PostgreSQL **Upsert** 기반 저장·갱신, FastAPI 조회·추천 API
- 규칙 기반 점수를 레이블로 활용한 합성데이터 800건 학습 — 계층화 분할 + class_weight로 불균형 대응
- SHAP 기여도를 한국어 설명으로 변환해 API 응답에 포함(XAI)
- 분류 정확도 88.75%(high F1 0.94) / 대기시간 MAE 2.59분, R² 0.9496

## 프론트엔드

### [MyMindMate — 아동·보호자 감정·일상 관리 앱](https://github.com/USW-MyMindMate/Frontend)
`2025.05 ~ 11 · 팀 · React Native(Expo)`
- 초기 화면 전체 구현: 부모/자녀 선택·로그인·회원가입·아이 홈(감정 팝업)·부모 홈(감정 통계 그래프)
- 감정 기록을 **배열 상태로 분리**해 목록·그래프 뷰 재사용 설계

### [진로레시피 — 희망 직업 기반 전공과목 추천 웹](https://github.com/Kimeunho0710/career-recipe)
`2025.03 ~ 06 · 졸업프로젝트 4인 · 프론트 대부분 주도(29/35 커밋)`
- 자격증 추천(모달)·전공 추천(학부/학과/학년 필터링)·로드맵·직업 상세·마이페이지
- 모바일 가로 스크롤 문제를 미디어쿼리·가변 폭으로 해결 — 반응형 패턴을 전 페이지 적용

### [SEMICOLON — 동아리 소개 웹](https://github.com/k0sun0h/Sem-colon_webpage)
`2025 여름 · 2인 · React/Vite`

## 기술 스택
`Python` `ROS2 Humble` `OpenCV` `slam_toolbox` `FastAPI` `PostgreSQL` `scikit-learn·SHAP` `React` `React Native` `Git`
