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



## βοΈ How to use 
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


## π§ Directory Structure
```
βββ Web-Security/                           - λ°±μλ νλΌμ€ν¬ λλ ν λ¦¬
    βββ package.lock.json                   - λΌμ΄λΈλ¬λ¦¬ κ΄λ¦¬ νμΌ
    βββ requirements.txt                    - λͺ¨λλ€μ μ λ¦¬ν νμΌ
    βββ app.py                              - Flask μ€ν μν νμΌ
    βββ output/                             - pdfμ κ²°κ³Όκ° μ μ₯λλ λλ ν λ¦¬
    βββ templates/
         βββ upload.html                   -ν΄λΌμ΄μΈνΈλ‘λΆν° pdfλ₯Ό λ°μμ΄
         βββ result.html                   -ν΄λΌμ΄μΈνΈμκ² pdf parsing κ²°κ³Όλ₯Ό λ³΄μ¬μ€
         βββ uploads/                      -ν΄λΌμ΄μΈνΈλ‘ λ°μμ¨ pdfλ₯Ό μ μ₯νλ κ³³
```
## π» API
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
