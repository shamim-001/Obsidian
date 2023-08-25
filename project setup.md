# setup
- Choose a folder where you want to keep your django project. Here `0.template_django`
- install virtual environment if not installed
```bash
pip3 install pipenv
```
- install django into that folder
  ```bash
pipenv install django
```
check whether django is properly installed
```bash
python3 -m django --version
```
The folder will look like this->
![[Pasted image 20230810154609.png]]

- Activate virtual environment
  ```bash
pipenv shell
```
Your terminal will look like this-> 
![[Pasted image 20230810154851.png]]


```
pip3 freeze > requirements.txt
```

```
pip3 install -r requirements.txt
```

- Create the project folder
```bash
django-admin startproject mysite .
```

![[Pasted image 20230810155154.png]]

- Run your project
  ```bash
python3 manage.py runserver `portnumber(optional)`
```

your terminal -> 
![[Pasted image 20230810155421.png]]
Now copy the `url` or `ctrl` + click the url
![[Pasted image 20230810155635.png]]
