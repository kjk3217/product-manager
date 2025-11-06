# 제품 사진 관리 PWA

시니어 분들을 위한 큰 글씨 버전의 모바일 앱입니다.

## 주요 변경사항

✅ **헤더 삭제** - 화면을 더 넓게 사용
✅ **폰트 크기 증가** - 시니어 분들이 보기 편하게
  - 버튼: 16px → 20px
  - 입력 필드: 16px → 20px  
  - 라벨: 14px → 18px
  - 제품 카드: 12px → 16px
  - 모달: 18px → 20px
✅ **PWA 지원** - 모바일 앱처럼 설치 가능
✅ **풀스크린 모드** - 앱처럼 전체 화면 사용

## 모바일 앱 설치 방법

### iPhone (Safari)
1. Safari에서 웹사이트 열기
2. 하단 공유 버튼 (⬆️) 탭
3. "홈 화면에 추가" 선택
4. "추가" 탭
5. 홈 화면에 앱 아이콘이 생성됨

### Android (Chrome)
1. Chrome에서 웹사이트 열기
2. 오른쪽 상단 메뉴 (⋮) 탭
3. "홈 화면에 추가" 또는 "앱 설치" 선택
4. "설치" 탭
5. 홈 화면에 앱 아이콘이 생성됨

## 필요한 파일

### 아이콘 이미지 (필수)
PWA로 설치하려면 아이콘 이미지가 필요합니다:

1. **icon-192.png** (192x192 픽셀)
2. **icon-512.png** (512x512 픽셀)

아이콘을 만드는 방법:
- Canva, Figma 등에서 제작
- 또는 https://www.favicon-generator.org/ 같은 도구 사용
- 제품 관리와 관련된 아이콘 (예: 카메라, 박스 등)

## 배포 방법

### Firebase Hosting (권장)
```bash
# Firebase CLI 설치
npm install -g firebase-tools

# Firebase 로그인
firebase login

# Firebase 프로젝트 초기화
firebase init hosting

# 배포
firebase deploy --only hosting
```

### Vercel (간편)
1. GitHub에 코드 업로드
2. Vercel에서 import
3. 자동 배포

### GitHub Pages
1. GitHub 저장소 생성
2. Settings → Pages에서 활성화
3. 파일 업로드

## 사용 방법

1. 웹사이트 접속 또는 설치한 앱 실행
2. 📷 등록 탭:
   - "사진 촬영" 버튼으로 제품 사진 찍기
   - 제품코드 입력
   - 소비자가격 입력
   - 저장하기
3. 📋 목록 탭:
   - 등록된 제품 보기
   - 검색으로 제품 찾기
   - 카드 탭하면 상세정보 보기

## 주의사항

- Firebase 설정은 이미 포함되어 있습니다
- 인터넷 연결이 필요합니다
- 카메라 권한을 허용해야 합니다

## 문제 해결

### 앱이 설치되지 않아요
- HTTPS가 필요합니다 (Firebase/Vercel은 자동 제공)
- icon-192.png와 icon-512.png 파일이 있는지 확인

### 글씨가 작아요
- 휴대폰 설정 → 디스플레이 → 글씨 크기를 조정하세요
- 더 크게 하려면 CSS의 font-size 값을 더 늘리면 됩니다

## 파일 구조

```
.
├── index.html       # 메인 HTML 파일
├── manifest.json    # PWA 설정 파일
├── sw.js           # 서비스 워커 (오프라인 지원)
├── icon-192.png    # 작은 아이콘 (만들어야 함)
├── icon-512.png    # 큰 아이콘 (만들어야 함)
└── README.md       # 이 파일
```
