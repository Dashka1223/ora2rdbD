1. CREATE USER user1 IDENTIFIED BY "password1";
Создает пользователя с паролем
2. CREATE USER user2 IDENTIFIED BY "password2"
   DEFAULT TABLESPACE users;
Создает пользователя и назвачаает ему табличное пространство. RedDatabase не поддерживает назначение табличного пространства по умолчанию для пользователя.
3. CREATE USER user3 IDENTIFIED BY "password3"
   PASSWORD EXPIRE;
Создает пользователя с истекающим паролем т.е. при первом входе система заставит пользователя сменить пароль.
4. CREATE USER user4 IDENTIFIED EXTERNALLY;
Создает пользователя с внешней аутентификацией т.е. Oracle не проверяет пароль а полагается на операционную систему или сетевые сервисы.Прямого аналога в RedDatabase нет. Можно использовать плагины аутентификации (USING PLUGIN).
5. CREATE USER user5 IDENTIFIED BY "password5" PROFILE profil;
Создает пользователя и назначает ему профиль. Прямого аналога в RedDatabase нет,но есть политика безопасности (SECURITY POLICIES).Она может частично заметять функционал профиля.
6. CREATE USER user6 IDENTIFIED BY "password6"
   TEMPORARY TABLESPACE temp;
Создает пользователя и назначает ему времменное табличное пространство. Аналога в  RedDatabase нет.
7. CREATE USER user7 IDENTIFIED BY "password7"
   QUOTA 100M ON users;
Создает пользователя с ограничением на использование дискового протранства в табличном пространстве.Аналога в  RedDatabase нет, но можно создать отдельное табличное пространство с ограниченным размером.
8. CREATE USER user8 IDENTIFIED BY "password8"
   ACCOUNT LOCK;
Cоздает пользователя с заблокированной учетнй записью.Прямого аналога в RedDatabase нет,но можно реализовать такую функцию с помощью политики безопасности (CREATE POLICY) и через триггер аутентификации.
9. CREATE USER user9 NO AUTHENTICATION;
Создает пользователя без требования аутентификации. Аналога в RedDatabase нет.
10. CREATE USER user10 IDENTIFIED GLOBALLY;
Создает пользователя с глобальной аутентификацией т.е. пользователь аутентифицируется через внешние централизованные системы, а не через локальные пароли в самой БД. В RedDatabase нет прямого аналога, но можно использовать  LDAP-плагин.
11. CREATE USER user11 IDENTIFIED BY "password11"
    ENABLE EDITIONS;
Создает пользователя с поддержкой редакций. Аналога в RedDatabase нет.
