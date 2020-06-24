# Django Review Project

## Project 구성

1. #### project name : review

2. #### app name : musicians

## Models

```python
class Musician(models.Model):
    name = models.CharField(max_length=150)
    age = models.IntegerField()
    
class Album(models.Model):
    # Musician과 1:N 관계
    title = models.CharField(max_length=150)
    ...
```

## Admin

```python
# musicians/admin.py admin 정의
from .models import Musician, Album
admin.site.register(Musician, Album)
```

```python
# bash 관리자계정 생성
python manage.py createsuperuser
```



