[최종 보고서] AI 멀티모달 파이프라인을 활용한 'AstroBean' 광고 제작
1. 프로젝트 개요 및 기획 의도
브랜드: AstroBean (가상 우주 커피 브랜드)
캠페인 목표: '무중력 로스팅'이라는 가상의 기술을 시각화하여 프리미엄 이미지 구축
핵심 메시지: "우주가 빚어낸 단 한 방울의 휴식, AstroBean"
디자인 전략: 심해와 우주를 연상시키는 Deep Blue와 Neon Blue를 메인 컬러로 설정하여 신비롭고 미래적인 톤앤매너 유지
2. AI 도구별 역할 및 선택 이유
도구 분류	사용 도구	선택 이유 (전략적 판단)
이미지	Leonardo.ai	일일 무료 크레딧 제공량이 넉넉하며, Canvas 편집 기능을 통해 프롬프트 수정 결과를 즉각적으로 반영할 수 있어 초기 컨셉 잡기에 최적이라 판단함.
비디오	Kling / Hailuo	단일 도구 사용 시 발생하는 크레딧 소모 및 대기열(Queue) 정체 문제를 해결하기 위해 파이프라인을 이원화함. 특히 Hailuo는 물리적 동세 구현에 강점이 있어 씬 2의 회전 장면에 전략적으로 배치함.
오디오	Suno AI	별도의 작곡 능력 없이도 텍스트만으로 브랜드 톤에 맞는 10초 분량의 배경음악을 가장 빠르게 프로토타이핑할 수 있어 선택함.
나레이션	ElevenLabs	무료 티어에서도 가장 인간에 가까운(High-fidelity) 음성 합성 품질을 보여주며, 브랜드의 신뢰도를 높이기에 가장 적합한 도구임.
3. 스토리보드 및 제작 상세 (Storyboard)
씬	길이	화면 구성 및 목표	사용 도구 및 선택 이유
1	3.5s	무중력 원두의 등장 (도입부)	Kling AI: 배경의 깊이감을 살리는 슬로우 줌인 효과가 가장 안정적임.
2	3.0s	원두의 질감과 회전 (핵심 비주얼)	Hailuo AI: 사물의 입체적 회전(Rotation) 표현력이 Kling보다 뛰어나 선택.
3	3.5s	브랜드 로고와 여운 (종결부)	Kling AI: 로고의 금속 질감에 은은한 빛(Glow) 효과를 주는 데 적합함.
3.1. 비주얼 생성 (Image & Video)
씬 번호	구분	입력 프롬프트 (원문)	출력 결과 요약 (한 줄)	생성 결과 파일명
Scene 1	이미지	A cinematic close-up shot of a futuristic coffee bean floating in zero gravity, glowing neon blue veins on the bean, inside a high-tech spaceship, soft bokeh background of stars, hyper-realistic, 8k, highly detailed --ar 16:9	무중력 상태에서 네온 빛이 감도는 미래형 원두 이미지	AB_IMG_01.png
비디오	Cinematic slow zoom in, floating coffee beans in zero gravity, spaceship background.	우주선 배경 속 원두를 향한 부드러운 슬로우 줌인 영상	AB_VID_01.mp4
Scene 2	이미지	Extreme close-up of a single, premium roasted coffee bean floating in zero-gravity, glossy oily texture, background of the futuristic spaceship interior and deep blue nebula from scene 1, cinematic blue rim lighting, hyper-realistic, 8k, sharp focus, highly detailed, 16:9	오일 질감이 강조된 원두와 푸른 성운 배경의 클로즈업 이미지	AB_IMG_02.png
비디오	Close up of a coffee bean rotating slowly, cinematic lighting, floating particles.	시네마틱한 조명 아래 천천히 회전하는 원두와 부유 입자 영상	AB_VID_02.mp4
Scene 3	이미지	Minimalist futuristic logo 'AstroBean' centered, sleek silver metallic texture, background of the same deep blue nebula and stars from previous scenes, cinematic blue neon rim lighting on the logo, elegant and premium atmosphere, 8k, sharp focus, 16:9	성운 배경 위 실버 메탈릭 질감의 AstroBean 로고 이미지	AB_IMG_03.png
비디오	Subtle camera movement, logo appearing with soft light glow.	은은한 광원 효과와 함께 나타나는 브랜드 로고 영상	AB_VID_03.mp4
3.2. 오디오 생성 (BGM & Narration)
구분	도구	입력 프롬프트 (원문)	출력 결과 요약 (한 줄)	생성 결과 파일명
BGM	Suno AI	Cinematic, space ambient, futuristic, lo-fi, 10 seconds, calm and premium	우주의 신비로움을 담은 차분하고 미래적인 앰비언트 곡	AB_BGM_Main.mp3
VO	ElevenLabs	AstroBean, the taste of zero gravity.	브랜드명과 슬로건을 강조한 신뢰감 있는 나레이션	AB_VO_Slogan.mp3

4. 프롬프트 설계 및 수정 프로세스 (Prompt Engineering)
[핵심 수정 사례: Scene 2]
수정 전: Cinematic close-up of dark liquid coffee droplets floating in zero gravity...
문제점: '액체 방울'은 형태가 계속 변해 씬 1의 '원두'와 시각적 연결성이 떨어지고, 브랜드 아이덴티티가 흐려짐.
수정 후: Extreme close-up of a single, premium roasted coffee bean floating in zero-gravity, glossy oily texture, background of the futuristic spaceship interior...
의도: 제품의 본질인 '원두'에 집중하고, 씬 1에서 사용한 배경 키워드를 재사용하여 시각적 일관성(Visual Consistency) 확보.
결과: 원두의 기름진 질감과 금속성 배경이 조화를 이루며 훨씬 프리미엄한 느낌 구현.
5. 도구별 결과 비교 및 의사결정 (솔직한 버전의 전문적 해석)
멀티 플랫폼 전략 (Multi-platform Strategy):
특정 AI 도구의 유료 전환 요구나 크레딧 제한이라는 현실적인 제약 사항을 제작 공정의 일부로 수용하였습니다.
이를 극복하기 위해 **Kling(줌인 효과 강점)**과 **Hailuo(사물 회전 강점)**를 교차 테스트하였으며, 각 도구가 가진 무료 크레딧 범위 내에서 최상의 컷을 선별하는 '비용 대비 고효율(Cost-effective)' 의사결정을 내렸습니다.
결과적으로 한 가지 도구에 의존할 때보다 더 다양한 시각적 피드백을 얻을 수 있었고, 이는 최종 영상의 다양성을 확보하는 계기가 되었습니다.
6. 통합 편집 및 기술적 최적화 (Integration)
톤앤매너 통합: 서로 다른 AI가 생성한 소스들의 색감을 맞추기 위해 CapCut에서 전체적으로 '시네마틱 블루' 필터를 적용하고 대비(Contrast)를 높임.
해상도 및 비율: 모든 소스를 16:9 비율로 통일하여 생성했으며, 최종 출력 시 1080p로 업스케일링하여 화질 저하 방지.
오디오 레이어링: Suno AI로 만든 배경음악 위에 ElevenLabs의 나레이션을 얹고, 나레이션이 나오는 구간에는 BGM 볼륨을 살짝 낮추는 '오디오 더킹' 기법 적용.
7. 결론 및 학습 성과
이번 프로젝트를 통해 단순히 AI에게 명령을 내리는 것을 넘어, 각 AI 모델의 특성(강점과 약점)을 파악하고 이를 파이프라인으로 연결하는 설계 능력의 중요성을 배웠습니다.

일관성 유지: 프롬프트에 공통 키워드를 삽입하여 멀티모달 환경에서의 이질감을 극복함.
문제 해결: 시드 유지의 한계를 프롬프트 구조 변경(액체→원두)으로 해결함.
통합 능력: 생성된 파편화된 소스들을 하나의 브랜드 메시지로 묶는 편집 과정의 중요성을 체득함.