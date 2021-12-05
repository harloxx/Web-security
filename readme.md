## ✏️ How to use 
### 1. Cloning
```
$ git clone https://github.com/harloxx/Web-security.git
```
### 2. Make Virtual Environment & Download Requirements
+ Go to *Web-security/* directory
```
cd Web-security
```
+ Make virtual environment
```
$ pip install virtualenv
$ virtualenv myenv # make virtual environment
```
+ Activate virtual environment
```
$ .\myenv\Scripts\activate
```
+ Go back to Web-security directory and install requirements.txt
```
(myenv) $ pip install -r requirements.txt 
```
+ If you want to deactivate
```
(myenv) $ deactivate
```
### 3. RUN
+ Run Flask
```
(myenv) $ flask run
```


## 🔧 Directory Structure
```
├── Web-Security/                           - 백엔드 플라스크 디렉토리
    ├── requirements.txt                    - 모듈들을 정리한 파일
    ├── app.py                              - Flask 실행 위한 파일
    ├── output/                             - pdf의 결과가 저장되는 디렉토리
    └── templates/
         ├── upload.html                   -클라이언트로부터 pdf를 받아옴
         ├── result.html                   -클라이언트에게 pdf parsing 결과를 보여줌
         └── uploads/                      -클라이언트로 받아온 pdf를 저장하는 곳

```
