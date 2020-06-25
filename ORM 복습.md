1:N 관계

Article.objects.all()

Comment.objects.all()



게시글 생성 ORM

Article.objects.create(title='title', content='content')

article.user = request.user

댓글 생성 ORM

article = Article.objects.get(pk=article.pk)

Comment.objects.get(pk=article.pk)



유저 생성 ORM

### User.objects.create_user(username='name', password='password')

---





게시글이 가지고 있는 전체 댓글 불러오기

```shell
python manage.py shell_plus
article = Article.objects.get(pk=2)
Comments.objects.get(pk=article.pk)
```



특정 댓글이 어느 게시글과 연결되어있는지 확인하기

user1 = User.objects.get(pk=1)

user1

article1 = Article.objects.create(title='title', content='content', user=user1)

article1

Comment.objects.create(content='content', user=user1, article=article1)

user.article_set.all()

article = Article.objects.get(pk=4)
In [18]: article.comment_set.all()
Out[18]: <QuerySet [<Comment: Article:4번째 글, title-content, 3-content>]>

In [19]: user1.article_set.all()
Out[19]: <QuerySet [<Article: 4번째 글, title-content>, <Article: 5번째 글, title-content>]>    

In [20]: for article in user1.article_set.all():
    ...:     print(article.title)



게시글이 어느 유저와 연결되어있는지 확인하기



특정 유저가 작성한 전체 게시글 가져오기



특정 유저가 작성한 전체 댓글 가져오기

