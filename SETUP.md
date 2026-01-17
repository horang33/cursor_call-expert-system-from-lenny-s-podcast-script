# 설치 및 설정 가이드

Lenny's Podcast 전문가 조언 시스템을 Cursor에서 사용하기 위한 단계별 가이드입니다.

## 📋 필요한 것

- Cursor IDE (최신 버전 권장)
- Git (트랜스크립트 다운로드용)
- 약 100MB 디스크 공간 (트랜스크립트 저장용)

## 🚀 설치 단계

### 1단계: Lenny's Podcast 트랜스크립트 다운로드

트랜스크립트는 GitHub에서 다운로드할 수 있습니다.

#### 방법 A: Git Clone (권장)

```bash
# 원하는 위치로 이동
cd ~/Documents  # 또는 원하는 경로

# 트랜스크립트 저장소 클론
git clone https://github.com/ChatPRD/lennys-podcast-transcripts.git
```

#### 방법 B: ZIP 다운로드

1. https://github.com/ChatPRD/lennys-podcast-transcripts 방문
2. "Code" 버튼 클릭 → "Download ZIP"
3. 다운로드한 ZIP 파일 압축 해제
4. 원하는 위치로 이동

### 2단계: 이 패키지 다운로드

#### 방법 A: Git Clone

```bash
# 이 저장소를 클론 (저장소가 있다면)
git clone [YOUR_REPO_URL]
```

#### 방법 B: 직접 다운로드

1. 이 폴더의 모든 파일을 다운로드
2. 원하는 위치에 저장

### 3단계: 프로젝트에 설치

#### 옵션 1: 전역 설치 (모든 프로젝트에서 사용)

Cursor의 전역 설정 폴더에 설치:

```bash
# macOS/Linux
cp .cursorrules ~/.cursor/rules/lennys-expert.cursorrules

# Windows
copy .cursorrules %USERPROFILE%\.cursor\rules\lennys-expert.cursorrules
```

#### 옵션 2: 프로젝트별 설치 (권장)

특정 프로젝트에서만 사용:

```bash
# 프로젝트 루트로 이동
cd /path/to/your/project

# .cursorrules 파일 복사
cp /path/to/lennys-expert-advisor/.cursorrules .
```

### 4단계: 경로 설정

`.cursorrules` 파일을 열고 트랜스크립트 경로를 확인/수정하세요.

현재 설정은 상대 경로를 사용합니다:
```
../lennys-podcast-transcripts/
```

#### 경로 구조 예시

```
your-workspace/
├── your-project/
│   └── .cursorrules          # 여기에 설치
└── lennys-podcast-transcripts/  # 트랜스크립트 위치
    ├── episodes/
    └── index/
```

#### 다른 위치에 트랜스크립트가 있다면?

`.cursorrules` 파일에서 경로를 수정하세요:

```markdown
# 절대 경로 사용 예시
- 참조: `/Users/yourname/Documents/lennys-podcast-transcripts/index/product-management.md`

# 또는 다른 상대 경로
- 참조: `../../transcripts/lennys-podcast-transcripts/index/product-management.md`
```

### 5단계: Cursor 재시작

1. Cursor를 완전히 종료
2. Cursor 재실행
3. 프로젝트 열기

## ✅ 설치 확인

### 테스트 1: 간단한 질문

Cursor의 채팅창에서:

```
/lenny 프로덕트 마켓 핏을 어떻게 찾나요?
```

AI가 `[자동 선택: Product Expert]`를 표시하고 Brian Chesky 등의 이름을 언급하면 성공!

### 테스트 2: 실제 질문

```
/lenny 제품 우선순위를 어떻게 결정하나요?
```

`[자동 선택: Strategy Expert]`가 표시되고 Shreyas Doshi, Gibson Biddle 등의 프레임워크가 제시되면 성공!

### 테스트 3: 트랜스크립트 접근

```
/lenny Matt Mochary의 1:1 미팅 방법을 알려주세요.
```

`[자동 선택: Leadership Expert]`가 표시되고 실제 에피소드 내용을 참조한 답변이 나오면 완벽!

## 🔧 문제 해결

### 문제 1: 전문가가 인식되지 않음

**증상**: `/lenny`를 입력해도 일반 AI처럼 응답하고 `[자동 선택: Expert]`가 표시되지 않음

**해결책**:
1. `.cursorrules` 파일이 프로젝트 루트에 있는지 확인
2. 파일 이름이 정확히 `.cursorrules`인지 확인 (`.cursorrules.txt` 아님)
3. Cursor 재시작
4. 프로젝트를 Cursor에서 다시 열기

### 문제 2: 트랜스크립트를 찾을 수 없음

**증상**: "트랜스크립트를 찾을 수 없습니다" 또는 일반적인 답변만 제공

**해결책**:
1. 트랜스크립트 폴더 위치 확인:
   ```bash
   ls ../lennys-podcast-transcripts/
   # episodes/ 와 index/ 폴더가 보여야 함
   ```

2. `.cursorrules` 파일에서 경로 수정:
   ```bash
   # 현재 경로 확인
   pwd
   
   # 트랜스크립트 경로 확인
   ls /path/to/lennys-podcast-transcripts/
   ```

3. 절대 경로로 변경 (임시 해결책):
   `.cursorrules` 파일에서 모든 `../lennys-podcast-transcripts/`를
   `/full/path/to/lennys-podcast-transcripts/`로 변경

### 문제 3: 한국어로 응답하지 않음

**증상**: 영어로 답변

**해결책**:
1. `.cursorrules` 파일 확인 - "한국어로 응답" 지침이 있는지 확인
2. 질문을 한국어로 작성
3. 명시적으로 요청: "한국어로 답변해주세요"

### 문제 4: 너무 일반적인 답변

**증상**: 실제 게스트 이름이나 에피소드가 언급되지 않음

**해결책**:
1. 더 구체적인 질문 작성:
   ```
   # 일반적 ❌
   /lenny 제품 관리가 뭔가요?
   
   # 구체적 ✅
   /lenny 초기 스타트업에서 제품 로드맵을 어떻게 만들어야 하나요?
   ```

2. 특정 게스트 언급:
   ```
   /lenny Brian Chesky의 제품 관리 철학을 알려주세요.
   ```

### 문제 5: Cursor가 느리거나 응답 없음

**증상**: 질문 후 오래 기다려도 답변 없음

**해결책**:
1. 인터넷 연결 확인
2. Cursor API 키 확인 (설정 → API Keys)
3. 질문을 더 짧고 명확하게 수정
4. Cursor 재시작

## 📁 권장 폴더 구조

### 옵션 1: 워크스페이스 레벨 (권장)

```
my-workspace/
├── project-a/
│   └── .cursorrules          # 프로젝트 A용
├── project-b/
│   └── .cursorrules          # 프로젝트 B용
└── lennys-podcast-transcripts/  # 공유 트랜스크립트
    ├── episodes/
    └── index/
```

### 옵션 2: 프로젝트 내부

```
my-project/
├── .cursorrules
├── src/
├── docs/
└── resources/
    └── lennys-podcast-transcripts/
        ├── episodes/
        └── index/
```

### 옵션 3: 전역 위치

```
~/Documents/
└── lennys-podcast-transcripts/
    ├── episodes/
    └── index/

~/Projects/
└── my-project/
    └── .cursorrules  # 절대 경로 사용
```

## 🔄 업데이트

### 트랜스크립트 업데이트

새로운 에피소드가 추가되면:

```bash
cd /path/to/lennys-podcast-transcripts
git pull origin main
```

### 이 패키지 업데이트

새 버전이 나오면:

1. 새 `.cursorrules` 파일 다운로드
2. 기존 파일 백업
3. 새 파일로 교체
4. 경로 설정 다시 확인

## 💡 고급 설정

### 여러 프로젝트에서 사용

심볼릭 링크 사용 (macOS/Linux):

```bash
# 트랜스크립트 한 곳에만 저장
ln -s ~/Documents/lennys-podcast-transcripts ~/Projects/project-a/
ln -s ~/Documents/lennys-podcast-transcripts ~/Projects/project-b/
```

### 특정 전문가만 사용

`.cursorrules` 파일에서 필요 없는 전문가 섹션 제거:

```markdown
# 예: Product와 Growth만 사용
## 12개 전문가 분야
1. Product Expert (Product Management)
2. Growth Expert (Growth Strategy)
# 나머지 주석 처리 또는 삭제
```

### 커스텀 전문가 추가

`.cursorrules` 파일에 새로운 전문가 추가:

```markdown
13. **Design Expert** - Design 전문가
    - 대표: [게스트 이름들]
    - 분야: UI/UX, 디자인 시스템
    - 참조: `Lenny's podcast/lennys-podcast-transcripts/index/design.md`
    - 트리거 키워드: 디자인, UI, UX, 인터페이스
```

## 📞 추가 도움

### 문서
- [README.md](README.md): 전체 개요
- [EXAMPLES.md](EXAMPLES.md): 사용 예시
- [experts/](experts/): 각 분야별 상세 가이드

### 커뮤니티
- GitHub Issues: 버그 리포트
- GitHub Discussions: 질문 및 토론

### 리소스
- [Lenny's Podcast](https://www.youtube.com/@LennysPodcast): 원본 팟캐스트
- [Cursor 문서](https://cursor.sh/docs): Cursor 사용법
- [트랜스크립트 저장소](https://github.com/ChatPRD/lennys-podcast-transcripts): 원본 트랜스크립트

## ✅ 체크리스트

설치 완료 확인:

- [ ] Lenny's Podcast 트랜스크립트 다운로드 완료
- [ ] `.cursorrules` 파일을 프로젝트에 복사
- [ ] 트랜스크립트 경로 확인/수정
- [ ] Cursor 재시작
- [ ] `/lenny` 테스트 성공 (자동 전문가 선택 확인)
- [ ] 실제 질문으로 테스트 성공
- [ ] 트랜스크립트 참조 확인

모두 체크되었다면 준비 완료! 🎉

[README.md](README.md)로 돌아가서 사용 방법을 확인하세요.
