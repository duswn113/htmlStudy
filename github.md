## 유저 설정 확인 
git config --global user.name <br>
git config --global user.email 

<br>

## 유저 설정 
git config --global user.name "leekwanghyup" <br>
git config --global user.email "leekwanghyup@naver.com" <br>

## 로그인 정보 없애기 
git config --global credential.helper manager <br>
git credential-manager delete https://github.com <br>

## 로컬 저장소 설정 
- 프로젝트 폴더로 이동하여 다음 명령어 입력 
git init
 - 다음의 결과를 얻는다 
 - Initialized empty Git repository in /Users/ieunji/Desktop/Back-end/springbott_lecture/untact/.git/
 - 위 디렉토리가 로컬저장소라는 뜻이다.

## 원격저장소
- 원격 저장소 확인 
    git remote -v
- 원격 저장소 설정 
    git remote add origin http://github.com/leekwanghyup/untact
- 삭제 
    git remote remove origin 

## 원격저장소에 push 
- 로컬저장소에 추가 되지 않은 목록을 볼수 있다. 
    git status 
    
- 로컬저장소에 추가되지 않은 모든 목록을 로컬저장소에 추가  
    git add . 

- 커밋을해야 로컬저장소에 완전히 저장된다.  
    git commit -m "커밋283739"    

- 원격저장소에 업로드 
    git push origin master
    
    - 다음 메세지가 뜨면서 원격 저장소에 push가 안될 경우 
     ![rejected] master -> master (fetch first)
    git push origin +master       

- 원격저장소에서 가져오기 
    git pull origin master 