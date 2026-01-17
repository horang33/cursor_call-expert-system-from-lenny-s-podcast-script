# Lenny's Podcast 전문가 조언 시스템

Lenny's Podcast의 269개 에피소드 트랜스크립트를 기반으로 12개 분야 세계적 전문가들의 조언을 제공하는 Cursor Rules 패키지입니다.

## 🎯 이게 뭔가요?

Cursor IDE에서 `/lenny` 명령어로 질문하면 AI가 자동으로 적절한 전문가를 선택하여 Lenny's Podcast에 출연한 세계적인 전문가들의 실제 인사이트와 조언을 제공합니다.

**예시:**
```
질문: "/lenny 프로덕트 마켓 핏을 어떻게 찾나요?"

응답: [자동 선택: Product Expert]

Brian Chesky와 Rahul Vohra의 관점에서 답변드리겠습니다.

프로덕트 마켓 핏(PMF)은 "사용자가 제품 없이는 살 수 없다"고 느끼는 상태입니다.

구체적으로:
1. **40% 테스트** (Sean Ellis): 사용자에게 "이 제품이 없어진다면?"이라고 물었을 때 40% 이상이 "매우 실망할 것"이라고 답하면 PMF 달성
2. **리텐션 커브**: 코호트 리텐션이 평평해지는 지점 찾기
3. **유기적 성장**: 사용자들이 자발적으로 추천하기 시작

Brian Chesky가 "Airbnb의 초기 성장" 에피소드에서 강조한 것처럼...
```

## 🎓 12개 전문가 분야

AI가 질문 내용을 분석하여 자동으로 적절한 전문가를 선택합니다:

| 전문가 | 분야 | 대표 게스트 | 트리거 키워드 |
|--------|------|------------|--------------|
| **Product Expert** | Product Management | Brian Chesky, Julie Zhuo, Shreyas Doshi | 제품, 프로덕트, 기능, 로드맵, PMF |
| **Strategy Expert** | Product Strategy | Shreyas Doshi, Gibson Biddle, Shishir Mehrotra | 전략, 우선순위, OKR, 의사결정 |
| **Leadership Expert** | Leadership | Matt Mochary, Kim Scott, Ben Horowitz | 리더십, 관리, 1:1, 피드백 |
| **Growth Expert** | Growth Strategy | Brian Balfour, Casey Winters, Elena Verna | 성장, 리텐션, 실험, A/B테스트 |
| **Engineering Expert** | Engineering | Will Larson, Camille Fournier, Nicole Forsgren | 엔지니어링, 개발, 아키텍처 |
| **AI Expert** | AI & Machine Learning | Chip Huyen, Logan Kilpatrick, Fei-Fei Li | AI, 머신러닝, ChatGPT, LLM |
| **Career Expert** | Career Development | Gergely Orosz, Camille Fournier, Jackie Bavaro | 커리어, 이직, 면접, 승진 |
| **Culture Expert** | Culture & Team Building | Stewart Butterfield, Molly Graham, Claire Hughes Johnson | 문화, 채용, 원격, 팀빌딩 |
| **Sales Expert** | Sales | Pete Kazanjy, Jason Lemkin, April Dunford | 영업, 세일즈, B2B, 계약 |
| **Marketing Expert** | Marketing | April Dunford, Seth Godin, Lulu Cheng Meservey | 마케팅, 브랜딩, 포지셔닝 |
| **Entrepreneur Expert** | Entrepreneurship | Jason Fried, Drew Houston, Tobi Lutke | 창업, 스타트업, 투자, VC |
| **Personal Expert** | Personal Development | Matt Abrahams, Graham Weaver, Jerry Colonna | 생산성, 커뮤니케이션, 스트레스 |

## 🚀 빠른 시작

### 1. 설치

1. 이 폴더를 다운로드하거나 클론하세요
2. `.cursorrules` 파일을 프로젝트 루트에 복사하세요
3. Lenny's Podcast 트랜스크립트를 다운로드하세요 ([GitHub](https://github.com/ChatPRD/lennys-podcast-transcripts))

### 2. 폴더 구조

```
your-project/
├── .cursorrules                    # 이 파일을 복사
└── lennys-podcast-transcripts/     # 트랜스크립트 폴더
    ├── episodes/
    └── index/
```

### 3. 사용 방법

Cursor에서 `/lenny` 뒤에 질문을 입력하면 AI가 자동으로 적절한 전문가를 선택합니다:

```
/lenny 제품 로드맵을 어떻게 만들어야 하나요?
/lenny 1:1 미팅을 효과적으로 진행하려면?
/lenny 리텐션을 어떻게 개선하나요?
```

AI가 질문의 키워드를 분석하여 가장 적합한 전문가(Product, Leadership, Growth 등)를 자동으로 매칭합니다.

## 📚 각 전문가가 답변할 수 있는 질문

### Product Expert (Product Management)
- 제품 로드맵, 우선순위 결정
- 제품-시장 적합성 찾기
- 제품 팀 관리
- 제품 지표 및 분석
- **상세 가이드**: [experts/product-management.md](experts/product-management.md)

### Strategy Expert (Product Strategy)
- 제품 전략 수립
- 우선순위 결정 프레임워크
- 의사결정 방법론
- OKR 설정 및 관리
- **상세 가이드**: [experts/product-strategy.md](experts/product-strategy.md)

### Leadership Expert (Leadership)
- 팀 관리 및 리더십
- 1:1 미팅, 피드백
- 조직 설계
- 관리자로의 전환
- **상세 가이드**: [experts/leadership.md](experts/leadership.md)

### Growth Expert (Growth Strategy)
- 성장 전략 및 실험
- 제품 주도 성장 (PLG)
- 리텐션 개선
- A/B 테스팅
- **상세 가이드**: [experts/growth.md](experts/growth.md)

### Engineering Expert (Engineering)
- 엔지니어링 리더십
- 팀 생산성
- 기술 전략
- 개발 프로세스
- **상세 가이드**: [experts/engineering.md](experts/engineering.md)

### AI Expert (AI & Machine Learning)
- AI 제품 개발
- ML 시스템 구축
- LLM 활용
- AI 전략
- **상세 가이드**: [experts/ai-ml.md](experts/ai-ml.md)

### Career Expert (Career Development)
- 커리어 성장 전략
- 면접 및 이직
- 스킬 개발
- IC vs 관리자 경로
- **상세 가이드**: [experts/career.md](experts/career.md)

### Culture Expert (Culture & Team Building)
- 회사 문화 구축
- 채용 및 온보딩
- 원격 팀 관리
- 조직 확장
- **상세 가이드**: [experts/culture.md](experts/culture.md)

### Sales Expert (Sales)
- B2B 영업 전략
- 엔터프라이즈 세일즈
- 세일즈 조직 구축
- 영업 프로세스
- **상세 가이드**: [experts/sales.md](experts/sales.md)

### Marketing Expert (Marketing)
- 포지셔닝 및 메시징
- 브랜드 빌딩
- 콘텐츠 마케팅
- PR 및 스토리텔링
- **상세 가이드**: [experts/marketing.md](experts/marketing.md)

### Entrepreneur Expert (Entrepreneurship)
- 스타트업 시작하기
- 자금 조달
- PMF 찾기
- 스케일링
- **상세 가이드**: [experts/entrepreneurship.md](experts/entrepreneurship.md)

### Personal Expert (Personal Development)
- 커뮤니케이션 스킬
- 생산성 및 시간 관리
- 스트레스 관리
- 습관 형성
- **상세 가이드**: [experts/personal-skills.md](experts/personal-skills.md)

## 💡 사용 예시

### 예시 1: 제품 전략 수립
```
질문: /lenny 제품 로드맵을 어떻게 만들어야 하나요?

응답: [자동 선택: Strategy Expert]

Shreyas Doshi와 Gibson Biddle의 관점에서 답변드리겠습니다.

제품 로드맵은 "무엇을 만들 것인가"보다 "왜 만드는가"에 초점을 맞춰야 합니다.

구체적으로:
1. **테마 기반 로드맵**: 개별 기능이 아닌 전략적 테마로 구성
2. **Now-Next-Later 프레임워크**: 구체적 날짜 대신 우선순위 단계로 표현
3. **가설 명시**: 각 항목이 어떤 비즈니스 가설을 검증하는지 명확히

Gibson Biddle가 "Netflix의 제품 전략" 에피소드에서 강조한 것처럼,
DHM 모델(Delight, Hard-to-copy, Margin-enhancing)로 각 항목을 평가하세요...

참고 에피소드:
- Shreyas Doshi - 제품 우선순위 결정
- Gibson Biddle - Netflix 제품 전략
```

### 예시 2: 팀 관리
```
질문: /lenny 효과적인 1:1 미팅은 어떻게 진행하나요?

응답: [자동 선택: Leadership Expert]

Matt Mochary와 Kim Scott의 관점에서 답변드리겠습니다...
```

### 예시 3: 성장 전략
```
질문: /lenny 리텐션을 어떻게 측정하고 개선하나요?

응답: [자동 선택: Growth Expert]

Casey Winters와 Brian Balfour의 관점에서 답변드리겠습니다...
```

더 많은 예시는 [EXAMPLES.md](EXAMPLES.md)를 참고하세요.

## 📖 상세 문서

- **[SETUP.md](SETUP.md)**: 설치 및 설정 가이드
- **[EXAMPLES.md](EXAMPLES.md)**: 각 전문가별 실제 사용 예시
- **[experts/](experts/)**: 12개 분야별 상세 가이드

## 🎯 이 시스템의 장점

### 1. 실제 전문가의 조언
- 이론이 아닌 실전 경험
- 세계적 기업의 실제 사례
- 검증된 프레임워크와 방법론

### 2. 맥락이 있는 답변
- 어떤 게스트의 어떤 에피소드에서 나온 조언인지 명시
- 여러 전문가의 관점을 종합
- 구체적인 예시와 사례

### 3. 즉각적인 접근
- Cursor에서 바로 질문
- 269개 에피소드의 지식 활용
- 필요할 때 언제든지 조언 받기

## 🔧 고급 사용법

### 복합 질문
여러 분야에 걸친 질문을 하면 AI가 자동으로 여러 전문가를 선택합니다:

```
질문: /lenny 초기 스타트업의 제품 전략과 성장 전략을 어떻게 연결하나요?

응답: [자동 선택: Product Expert + Growth Expert]
```

### 특정 상황
구체적인 상황을 설명하면 더 맞춤형 조언을 받을 수 있습니다:

```
질문: /lenny 저는 5명 팀의 신입 관리자입니다. 
      첫 1:1 미팅에서 무엇을 물어봐야 하나요?

응답: [자동 선택: Leadership Expert]
```

## 📊 포함된 내용

- **269개 에피소드** 트랜스크립트 기반
- **12개 전문가 분야** 체계적 분류
- **50+ 주요 게스트** 인사이트
- **93개 토픽** 커버
- **실전 프레임워크** 및 사례

## 🤝 기여하기

이 프로젝트를 개선하고 싶으신가요?

1. 새로운 전문가 분야 제안
2. 더 나은 프레임워크 추가
3. 사용 예시 공유
4. 버그 리포트

## 📜 라이선스 및 출처

### 출처
- **트랜스크립트**: [Lenny's Podcast Transcripts Archive](https://github.com/ChatPRD/lennys-podcast-transcripts)
- **원본 콘텐츠**: [Lenny's Podcast](https://www.youtube.com/@LennysPodcast)

### 사용 조건
- 교육 및 개인 학습 목적으로 사용
- 원저작자(Lenny Rachitsky)와 게스트들의 권리 존중
- 상업적 사용 시 별도 허가 필요

### 면책 조항
- 이 시스템은 비공식 프로젝트입니다
- Lenny's Podcast와 공식적인 관련이 없습니다
- 모든 조언은 참고용이며, 실제 적용 시 본인의 판단이 필요합니다

## 🌟 추천 사용 사례

### 제품 관리자
- 제품 전략 수립 시
- 우선순위 결정 시
- 팀 관리 고민 시

### 엔지니어링 리더
- 팀 구조 설계 시
- 기술 전략 수립 시
- 커리어 결정 시

### 창업자
- 스타트업 시작 시
- PMF 찾기
- 자금 조달 준비

### 성장 담당자
- 성장 전략 수립 시
- 실험 설계 시
- 채널 선택 시

## 📞 문의 및 지원

- 이슈: GitHub Issues
- 개선 제안: Pull Requests
- 질문: Discussions

## 🙏 감사의 말

- **Lenny Rachitsky**: 훌륭한 팟캐스트와 인터뷰
- **모든 게스트들**: 귀중한 인사이트 공유
- **ChatPRD**: 트랜스크립트 아카이브 제공
- **Cursor**: 강력한 AI 코딩 도구

---

**버전**: 1.0  
**마지막 업데이트**: 2026-01-16  
**에피소드 수**: 269개  

**시작하기**: [SETUP.md](SETUP.md)를 읽고 설치하세요!
