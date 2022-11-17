# midterm
A tutorial for AI Application midterm

## 0. 환경 Setting

1. 제시된 이름 형식에 맞춰 개인 private repository 생성 후 `jinho311`과 `Artinto` 계정 collaborator로 추가

- Collaborator 설정하는 법
  > 해당 repository - 메뉴바 우측 상단 Settings - 좌측 상단 Collaborators - 계정 추가 - 상대가 email로 수락
  
2. Data Set Download 및 개인 Google Drive에 Upload (255MB)


## 1. 내 Repository에 Push  Pull Request 하기

### Drive mount
```python
from google.colab import drive
drive.mount('/content/drive')
```

### 경로 설정 및 change directory
```python
%cd /content/drive/MyDrive/Colab\ Notebooks
```

### GitHub token 발행

GitHub - 우측 상단 Profile - Dropdown에 Settings - 좌측 하단 Developer Settings - 좌측 Personal access tokens - Tokens(classic) - Generate new token - repo check - token 복사

### GitHub clone
```python
!git clone https://(token)@github.com/HaileyHyewonChung/(repository).git
```

### Directory 생성 및 경로 확인
```git
%cd (repository)/
```

### Initialize local repository
```
!git init
```

### 작성자 정보 입력
```
!git config --global user.email "99hyewon@naver.com"
!git config --global user.name "HaileyHyewonChung"
```

### Readme.md 수정

Google Drive에서 해당 파일 수정 후 수정사항 반영 확인

### Local에서 Commit하기
```
!git add .
!git commit -m "Edit Readme.md"
```

### 모든 기록된 version 확인
```
!git log
```

### Main으로 Push하기
```
!git push -u (repository) main
```

### Pull Request

GitHub의 해당 Repository에 들어가 Pull Request 작성


## 2. Collaborator의 Repository에 Push, Pull Request 및 Merge 하기

### Drive mount
```python
from google.colab import drive
drive.mount('/content/drive')
```

### 경로 설정 및 change directory
```python
%cd /content/drive/MyDrive/Colab\ Notebooks
```

### GitHub token 발행

GitHub - 우측 상단 Profile - Dropdown에 Settings - 좌측 하단 Developer Settings - 좌측 Personal access tokens - Tokens(classic) - Generate new token - token 복사

### GitHub clone
```
!git clone https://(token)@github.com/jinho311/(repository).git
```

### Directory 생성 및 경로 확인
```
%cd (repository)/
```

### Local Branch 만들고 이동
```
!git checkout -b (branch)
```

### 현재 branch 확인
```
!git status
```

### 파일 수정

Google Drive에서 해당  수정 후 수정사항 반영 확인

### User 정보 입력
```
!git config --local user.email "99hyewon@naver.com"
!git config --local user.name "HaileyHyewonChung"
```

### Commit 하기
```
!git add .
!git commit -m "Edit Readme.md by HaileyHyewonChung"
```

### Remote에 Push하기
```
!git remote add (repository) https://HaileyHyewonChung:(token)@github.com/jinho311/(repository).git
!git push (repository) (branch)
```

### Pull Request & Merge

해당 repository에서 Pull Request 작성 및 Merge


## 3. 여러 가지 Error들

### 

