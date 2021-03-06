# Github & 배포



## 1. Github 기초

### 1.1 Git

- 파일의 변천사를 저장하는 역할
- 누가, 무엇을, 어디서, 언제 변경했는지에 대한 내용 기록 ⇒ 코드의 변화 기록

### 1.2 Github

- git과 코드를 저장하고 관리하는 서비스

    ![github_image(1)](./img/github(1).png)

- 개발자의 포트폴리오 역할

### 1.3 Github 환경설정

- Git, Git Bash 다운 및 GitHub 계정 생성

### 1.4 Repository 생성 및 첫 Push

- Github 웹사이트에서 Repository 생성

```bash
git init
git remote add origin Repository_address
git add . # directory에 있는 모든 파일이 업로드 준비 상태에 들어감
git commit -m "(원하는 내용)" 
git push origin master # push를 해야 Repository에 업로드됨
```

- Github와 Local PC가 연결되어 있고 (점선), local에서 repository에 파일을 업로드(화살표)

    ![github_image(2)](./img/github(2).png)




## 2. Netlify 배포

### 2.1 정적, 동적 페이지

- 정적 페이지 (Static page)

    ![github_image(3)](./img/github(3).png)

- 동적 페이지 (Dynamic page)

    ![github_image(4)](./img/github(4).png)

### 2.2 Netlify 배포과정

![github_image(5)](./img/github(5).png)

- Netlify의 경우 정적 페이지만 업로드 할 수 있음
- 실제로 배포해 봄! (likelion8th-session repository)

    [My Notes](https://infallible-euclid-3fa87f.netlify.app/)




## 3. Github 사용법 및 협업

### 3.1 자주 쓰는 Git 명령어

- `git init` : git 저장소를 초기화
- `git add .` : 폴더에 변경된 모든 파일 staging area에 올리기
- `git commit -m "커밋에 대한 설명"` : 유사시 돌아갈 수 있는 저장소의 체크 포인트 생성
- `git remote add origin http://원격 저장소 주소.git` : 원격 저장소 (remote repository) 연결
- 기본적인 Git 명령어의 수행 과정

    ![github_image(6)](./img/github(6).png)

- `git branch 브랜치명` : 새로운 브랜치 생성
- `git checkout 브랜치명` : 해당 브랜치로 생성
- `git push origin 브랜치` : 원격 저장소의 특정 브랜치에 프로젝트 저장
- `git pull origin 브랜치` : 원격 저장소의 특정 브랜치에서 변경사항 pull
- `git clone http://원격 저장소 주소.git` : 원격 저장소에 있는 파일 전체 복사
- `git status` : git 저장소의 상태 확인

### 3.2 Github를 이용한 협업

1. 원격 저장소 생성 (Github repository 생성)
2. 팀원을 Collaborator로 추가
3. 초기 프로젝트 push
4. 팀원들의 로컬에 프로젝트 pull
5. 팀원 각자의 브랜치를 생성하여 작업
6. 브랜치에 작업한 내용을 push
7. Master와 merge 하기 전 pull request
8. Pull request 확인 후 Mater와 merge

### 3.3 Fork를 이용한 협업

1. 작업 하고 싶은 Repository fork 해오기
2. 자신의 로컬에서 작업
3. 변경사항을 자신의 브랜치에 Push
4. 원본 Repository 소유자에게 Pull Request 요청
5. 소유자가 Pull Request를 승인하여 merge하면 자동으로 Collaborator 추가