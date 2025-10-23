# Домашнее задание к занятию "`GitLab`" - `Марченко Николай`


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. ![Руководство по оформлению Markdown файлов] (https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1

Что нужно сделать:

1. Разверните GitLab локально, используя Vagrantfile и инструкцию, описанные в этом репозитории.
2. Создайте новый проект и пустой репозиторий в нём.
3. Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab.

В качестве ответа в репозиторий шаблона с решением добавьте скриншоты с настройками раннера в проекте.


### Решение 1

1. [Резвернут Gitlab, создан новый проект и репозиторий в нем:](https://github.com/Doskaks/8-03-gitlab-hw/blob/main/my_rep_nikolay.jpg)
   
   ![Резвернут Gitlab, создан новый проект и пустой репозиторий в нем](https://github.com/Doskaks/8-03-gitlab-hw/blob/main/my_rep_nikolay.jpg)
   
3. [Зарегистрировал gitlab-runner (в режиме Docker):](https://github.com/Doskaks/8-03-gitlab-hw/blob/main/Runners.jpg)

   ![Зарегистрировал gitlab-runner (в режиме Docker):](https://github.com/Doskaks/8-03-gitlab-hw/blob/main/Runners.jpg)

   [Настройки Runners:](https://github.com/Doskaks/8-03-gitlab-hw/blob/main/Setting_runners.jpg)

   ![Настройки Runners:](https://github.com/Doskaks/8-03-gitlab-hw/blob/main/Setting_runners.jpg)

 



---

### Задание 2

Что нужно сделать:

1. Запушьте репозиторий на GitLab, изменив origin. Это изучалось на занятии по Git.
2. Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы.
    
В качестве ответа в шаблон с решением добавьте:

- файл gitlab-ci.yml для своего проекта или вставьте код в соответствующее поле в шаблоне;
- скриншоты с успешно собранными сборками.
    

### Решение 2

1. [Запушty репозиторий на GitLab](https://github.com/Doskaks/8-03-gitlab-hw/blob/main/my_rep_nikolay.jpg)
   
   ![Запушty репозиторий на GitLab](https://github.com/Doskaks/8-03-gitlab-hw/blob/main/my_rep_nikolay.jpg)

2. Создан .gitlab-ci.ym:

```
stages:
  - test
  - build

test_go-01:
  stage: test
  image: golang:1.17
  script: 
   - go test .
  tags:
    - netology
```

[Сборка:](https://github.com/Doskaks/8-03-gitlab-hw/blob/main/test_go_01.jpg)
   
![Сборка:](https://github.com/Doskaks/8-03-gitlab-hw/blob/main/test_go_01.jpg)


