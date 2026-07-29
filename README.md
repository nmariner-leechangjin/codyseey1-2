[최종 보고서] AI 멀티모달 파이프라인을 활용한 'AstroBean' 광고 제작
1. 프로젝트 개요 및 기획 의도
브랜드: AstroBean (가상 우주 커피 브랜드)
타겟 페르소나: IT/테크 업계에 종사하며 새로운 기술적 경험을 즐기는 2040 전문직 남녀. (바쁜 일상 속에서 '우주적 휴식'이라는 비현실적 럭셔리를 지향함)
핵심 메시지: "우주가 빚어낸 단 한 방울의 휴식, AstroBean"
디자인 전략: 심해와 우주를 연상시키는 Deep Blue(#00008B)와 Neon Blue(#00FFFF)를 메인 컬러로 설정하여 신비롭고 미래적인 톤앤매너 유지.
제작 선언: 본 프로젝트의 모든 소스는 AI로 생성되었으며, 직접 촬영물이나 유료 스톡 소스를 전혀 사용하지 않았음.
2. AI 도구 전략 및 비교 분석
2.1. 도구별 정량적 비교 (#13, #17)
도구 분류	사용 도구	품질(1~5)	생성 속도	비용(크레딧)	선택 근거 및 역할
이미지	Leonardo.ai	5	30초/장	150/일(무료)	T2I 기반의 고해상도 컨셉 아트 생성
비디오	Kling AI	4	2분/5초	66/일(무료)	카메라 워킹(Zoom)의 안정성 확보
비디오	Hailuo AI	5	3분/5초	0(Beta무료)	물리적 회전(Rotation)의 사실감 구현
오디오	Suno AI	4	1분/곡	50/일(무료)	브랜드 톤에 맞는 배경음악 프로토타이핑
나레이션	ElevenLabs	5	10초/문장	1만자(무료)	인간에 가까운 신뢰감 있는 음성 합성
2.2. T2I vs I2V 선택 근거 (#12)
T2I (Text-to-Image): 전체적인 구도와 색감(Deep Blue)을 확정 짓기 위해 사용.
I2V (Image-to-Video): T2I로 생성된 원두의 디자인을 유지하면서 움직임만 부여하기 위해 사용. (텍스트만으로 비디오 생성 시 발생하는 형태 왜곡 방지)
3. 스토리보드 및 상세 설계 (#2, #5)
씬	길이	화면 구성 및 목표	내레이션 (VO)	메타데이터 (예상)
1	3.5s	무중력 원두의 등장	"고요한 우주의 끝에서,"	1920x1080, 30fps
2	3.0s	원두의 질감과 회전	"완벽한 한 방울이 시작됩니다."	1920x1080, 30fps
3	3.5s	브랜드 로고와 여운	"AstroBean, 무중력을 마시다."	1920x1080, 30fps
합계	10.0s	최종 광고 영상	전체 나레이션 포함	MP4, H.264
4. 데이터 리스트 및 증빙 (#4, #6, #11)
파일명 규칙: AB_SCN_[번호]_[버전] (예: AB_SCN_01_V01.mp4)
구분	파일명	입력 프롬프트 요약	출력 결과 (증빙 링크/경로)
이미지	Scene1.jpg	Futuristic coffee bean, neon blue	[https://github.com/nmariner-leechangjin/codyseey1-2/blob/main/Scene1.jpg]
비디오	Scene1.mp4	Slow zoom in on bean	[https://github.com/nmariner-leechangjin/codyseey1-2/blob/main/Scene1.mp4]
오디오	AstroBean BGM.mp3	Space ambient, lo-fi	[https://github.com/nmariner-leechangjin/codyseey1-2/blob/main/Scene1.mp3]
최종본	0728.mp4	통합 편집 완료본	[https://github.com/nmariner-leechangjin/codyseey1-2/blob/main/0728.mp4]
5. 프롬프트 엔지니어링 및 수정 이력 (#3, #14)
[Scene 2 수정 로그]
일시: 2024-07-29 14:20
수정 전: Cinematic close-up of dark liquid coffee droplets floating in zero gravity...
수정 후: Extreme close-up of a single, premium roasted coffee bean floating in zero-gravity, glossy oily texture...
핵심 토큰 변화 비교 분석:

변경 전 토큰	변경 후 토큰	영향 및 의도
liquid droplets	roasted coffee bean	일관성: 액체의 불규칙성 제거, 브랜드 핵심 개체(원두)로 고정
dark	glossy oily texture	디테일: 고급스러운 원두 표면의 반사광 유도
floating	zero-gravity	물리법칙: 단순 부유가 아닌 우주 공간의 물리적 특성 강조
6. 제작 관리 및 리소스 계획 (#8, #9, #18)
6.1. 단계별 체크리스트 (#8)
기획: 타겟 설정 및 씬별 내레이션 확정 (책임: 기획자)
생성: T2I 이미지 생성 후 I2V 비디오 변환 (책임: AI 엔지니어)
검수: 씬 간 색감(Deep Blue) 및 해상도 일치 여부 확인 (책임: 디렉터)
6.2. 리소스 및 대체 계획 (#9, #18)
예상 생성 횟수: 씬당 이미지 10회, 비디오 5회 시도 예상.
크레딧 부족 시 시나리오:
우선순위: 씬 2(핵심 비주얼) > 씬 3(로고) > 씬 1(도입)
대체 도구: Kling 크레딧 소진 시 Luma Dream Machine으로 즉시 교체.
편집 전략: 비디오 생성 실패 시 이미지를 활용한 2.5D 패럴랙스 효과로 대체.
7. 기술적 표준 및 후처리 (#10, #15, #16)
색감 표준: sRGB 색공간 준수. 메인 컬러 코드 **#00008B(Deep Blue)**를 기준으로 모든 소스 매칭.
후처리 파라미터:
컬러 그레이딩: CapCut '시네마틱' 필터 (강도 70%) 적용.
대비/선명도: Contrast +15, Sharpen +20 설정하여 질감 강조.
컬러 매칭: 씬 1의 배경 이미지를 '참조 이미지'로 사용하여 전체 영상의 톤을 일치시킴.
8. 메시지 재구성 및 편집 규칙 (#19)
시간 단축 시 우선순위:
보존: 씬 2(원두 질감), 씬 3(브랜드 로고)
삭제/축소: 씬 1의 배경 인트로 구간을 1.5초로 단축.
규칙: 메시지의 핵심인 "AstroBean" 브랜드명 노출 시간은 최소 3초 이상 유지함.
