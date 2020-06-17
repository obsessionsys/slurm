# Урок 3 Слёрм

* Best Practice Docker и Docker-compose

##	Что мы хотим от программы
1.	Скорость (сборка, и быстрый релиз)
2.	Безопасность и контроль
3.	Удобство работы и прозрачность


## Ускоряемся 

-	Тюнинг Dockerfile
-	.dockerignore
-	Размер образа
-	Кэширование
-	Multi-stage сборка


```
docker build –t test_size .
```


## Усиливаем контроль и безопасность

- Не используем latest!
- Указываем  явные версии ПО
- 1 процесс – 1 контейнер
- The Twelve-factor App
- Метрики и логи приложения
- Настройка приложения через env
- Resource management
- Минимум привилегий процесса в контейнере (mount, host network, root…)
- Свой базовый образ || тестим образы на уязвимости (https://snyk.io)

```
docker-compose -f docker-compose.production.yml -f docker-compose.test.yml up --abort-on-container-exit --exit-code-from test
```

## Ссылки

* https://clck.ru/MBtKt - про CI/CD в целом

* https://docs.docker.com/compose/

* https://docs.docker.com/compose/gettingstarted/

* https://docs.gitlab.com/ee/ci/docker/using_docker_build.html

* https://docs.docker.com/develop/develop-images/baseimages/

* https://habr.com/ru/company/southbridge/blog/329138/