This is a project of the 'Web Security' class, a cybersecurity major at Ewha Womans University. It is a website that detects malicious pdfs through machine learning and PDF parsing.

## testing



https://user-images.githubusercontent.com/79822913/173197709-1891cb5c-8194-4e81-b0a0-08746a96932a.mp4


<br/><br/>
This is the main page. You can upload pdf files more than one.<br/>
_/upload_ <br/>
![image](https://user-images.githubusercontent.com/79822913/147897628-d1b3e6fb-0504-4043-9b96-a7a41ccf2bb0.png)

<br/><br/>
After pdf parsing, results are displayed <br/>
_/uploader_<br/>
![image](https://user-images.githubusercontent.com/79822913/147897642-3e23a61b-fb2e-494f-954d-501b1624f4cf.png)



## ✏️ How to use 
### 1. Cloning
```
$ git clone https://github.com/harloxx/Web-security.git
```
### 2. Make Virtual Environment & Download Requirements
+ Project Environment : VMware Workstation 16 Player, Ubuntu 16.04
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
$ source myenv/bin/activate
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
    ├── package.lock.json                   - 라이브러리 관리 파일
    ├── requirements.txt                    - 모듈들을 정리한 파일
    ├── app.py                              - Flask 실행 위한 파일
    ├── output/                             - pdf의 결과가 저장되는 디렉토리
    └── templates/
         ├── upload.html                   -클라이언트로부터 pdf를 받아옴
         ├── result.html                   -클라이언트에게 pdf parsing 결과를 보여줌
         └── uploads/                      -클라이언트로 받아온 pdf를 저장하는 곳
```
## 💻 API
#### main page, pdf upload
```
GET /upload
```
#### pdf upload & pdf parsing result
```
POST /uploader
```
+ Request
```
{
    "files" : "file[]",
    "enctype" : "multipart/form-data"
}
```
+ Response
```
{
    "benign": [benign file list],
    "malicious" : [malicious file list]
}

```
