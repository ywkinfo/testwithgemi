# GitHub + Vercel 배포 가이드

한 줄 소개: GitHub에 코드를 올리고 Vercel로 즉시 배포할 수 있는 초보자용 원페이지 웹 프로젝트입니다.

## 📦 생성된 파일
- `index.html` - 메인 웹페이지
- `README.md` - 프로젝트 설명
- `.gitignore` - Git 제외 파일

## 🚀 배포 단계

### 1️⃣ GitHub에 새 레포지토리 생성
1. https://github.com/new 접속
2. Repository name 입력 (예: `my-first-deploy`)
3. Public 선택
4. **"Add a README file" 체크 해제** (이미 있음)
5. "Create repository" 클릭

### 2️⃣ GitHub Personal Access Token 생성 (처음 한 번만)
1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. "Generate new token (classic)" 클릭
3. Note: `vercel-deploy` 입력
4. 만료기간: 원하는 기간 선택
5. repo 권한 체크 ✅
6. "Generate token" 클릭
7. **토큰 복사해서 저장** (다시 볼 수 없음!)

### 3️⃣ GitHub에 코드 Push
아래 명령어를 하나씩 실행하세요:

```bash
# GitHub 레포지토리 연결 (YOUR-USERNAME과 REPO-NAME을 본인 것으로 변경)
git remote add origin https://github.com/YOUR-USERNAME/REPO-NAME.git

# main 브랜치로 변경
git branch -M main

# Push (YOUR-TOKEN을 위에서 복사한 토큰으로 변경)
git push https://YOUR-TOKEN@github.com/YOUR-USERNAME/REPO-NAME.git main
```

### 4️⃣ Vercel에서 배포
1. https://vercel.com 접속 후 GitHub 계정으로 로그인
2. "New Project" 클릭
3. GitHub 레포지토리 검색 후 "Import" 클릭
4. 프로젝트 설정은 기본값 그대로 두고 "Deploy" 클릭
5. 배포 완료! 🎉

---

## 💡 더 쉬운 방법
Claude Code에서 직접 push하고 싶다면:

```bash
cd /home/user/testwithgemi
git remote add origin https://YOUR-TOKEN@github.com/YOUR-USERNAME/REPO-NAME.git
git branch -M main
git push -u origin main
```

이후 Vercel에서 Import만 하면 끝!

---

## ✨ 프로젝트 특징
- 🎨 모던한 그라데이션 디자인
- 📱 완전한 반응형 레이아웃
- 🚀 GitHub + Vercel 자동 배포
- 💜 사용자 친화적인 UI/UX
