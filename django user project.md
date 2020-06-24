# Article : USER

### Article 모델에 외래키 설정 후 마이그레이션 작업 진행

----

#### - 연결할 User모델은 settings.AUTH_USER_MODEL

#### - 마이그레이션 작업을 진행 시 기존의 데이터에 USER정보가 없으므로 Default값 설정

#### - 현재 프로젝트의