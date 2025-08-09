# 모각코 강남 웹사이트

모여서 각자 코딩하는 모임을 위한 정적 웹사이트입니다.

## 특징

- 📱 반응형 디자인 (모바일/태블릿/데스크톱)
- 🎨 모던하고 깔끔한 UI/UX
- 📧 이메일 연락 기능
- 🚀 정적 사이트 (별도 서버 불필요)

## 사진 추가 위치

웹사이트에서 사진을 추가할 수 있는 위치들:

### 1. 히어로 섹션 (메인 화면)
- 파일 위치: `index.html` 라인 45-50
- 루카831 건물 외관 사진 추천
- 크기: 400px x 300px 정도

### 2. 장소 섹션 - 메인 사진
- 파일 위치: `index.html` 라인 145-150
- 루카831 대표 사진
- 크기: 600px x 250px 정도

### 3. 장소 섹션 - 내부 사진들
- 파일 위치: `index.html` 라인 151-160
- 내부 공간 사진 2장
- 크기: 각각 280px x 120px 정도

## 사진 추가 방법

1. 사진 파일을 프로젝트 폴더에 `images/` 디렉토리를 만들어 저장
2. HTML에서 `<div class="image-placeholder">` 부분을 `<img>` 태그로 교체

예시:
```html
<!-- 기존 -->
<div class="image-placeholder">
    <i class="fas fa-building"></i>
    <p>루카831 건물 사진<br>위치를 지정해주세요</p>
</div>

<!-- 사진 추가 후 -->
<img src="images/luca831-exterior.jpg" alt="루카831 건물 외관" class="venue-image">
```

## 로컬에서 실행하기

```bash
# 간단한 HTTP 서버 실행 (Python 3)
python -m http.server 8000

# 또는 Node.js가 있다면
npx serve .
```

브라우저에서 `http://localhost:8000` 접속

## 배포하기

이 사이트는 정적 사이트이므로 다음 서비스들에 쉽게 배포할 수 있습니다:

- **Netlify**: 가장 추천 (무료, 자동 배포)
- **Vercel**: Next.js 외에도 정적 사이트 지원
- **GitHub Pages**: GitHub 저장소와 연동
- **Firebase Hosting**: Google의 호스팅 서비스

### Netlify 배포 방법
1. [netlify.com](https://netlify.com) 가입
2. "New site from Git" 클릭
3. GitHub/GitLab 저장소 연결 또는 폴더 드래그앤드롭
4. 자동으로 배포 완료!

## 연락 기능

현재 "연락하기" 버튼은 사용자의 기본 이메일 클라이언트를 열어줍니다. 
실제 이메일 주소로 변경하려면 `script.js` 파일의 `mailtoLink` 부분을 수정하세요:

```javascript
const mailtoLink = `mailto:your-email@example.com?subject=${subject}&body=${body}`;
```

## 커스터마이징

- **색상 변경**: `styles.css`에서 색상 변수들을 수정
- **폰트 변경**: `index.html`의 Google Fonts 링크 수정
- **내용 수정**: `index.html`에서 텍스트 내용 변경
