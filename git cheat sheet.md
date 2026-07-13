# Git 기본 치트 시트 (Cheat Sheet)

## Git의 3가지 핵심 영역
* **Working Directory**: 실제 작업 중인 파일들이 위치하는 영역입니다.
* **Staging Area**: Working Directory에서 변경된 파일 중 다음 버전에 포함시킬 파일들을 선택적으로 추가하거나 제외할 수 있는 중간 준비 영역입니다.
* **Repository**: 버전 이력과 파일들이 영구적으로 저장되는 영역입니다. 모든 버전과 변경 이력이 기록됩니다.

---

## Git 초기 설정 (사용자 정보 등록)
* **`git config --global user.email "메일주소"`**: Commit 작성자(author)의 이메일 정보를 설정합니다.
* **`git config --global user.name "유저네임"`**: Commit 작성자(author)의 이름 정보를 설정합니다.
* **`git config --global -l`**: Git global 설정 정보를 확인합니다.

---

## Git 기본 명령어
* **`git init`**: 로컬 저장소 설정(초기화)을 수행하며, Git의 버전 관리를 시작할 디렉토리에서 진행합니다.
* **`git add <파일명>`**: 변경사항이 있는 파일을 staging area에 추가합니다.
* **`git commit -m "메시지"`**: staging area에 있는 파일들을 저장소에 기록하며, 해당 시점의 버전을 생성하고 변경 이력을 남깁니다.
* **`git status`**: 현재 로컬 저장소의 파일 상태를 확인합니다.
* **`git log`**: Commit history를 확인합니다.
* **`git log --oneline`**: Commit 목록을 한 줄로 확인합니다.

---

## ⚠️ 주의사항
* Git 로컬 저장소 내에 또다른 Git 로컬 저장소를 만들지 말아야 합니다.
* 이미 Git 로컬 저장소인 디렉토리 내부 하단에서 `git init` 명령어를 다시 입력하지 않아야 합니다.
* Git 저장소 안에 Git 저장소가 있을 경우, 가장 바깥 쪽의 Git 저장소가 안쪽의 Git 저장소의 변경사항을 추적할 수 없게 되기 때문입니다.