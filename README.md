# Практическая работа №1. «Делимся проектом с миром»

**Сделать папку репозиторием —** `git init`

**«Разгитить» папку, если что-то пошло не так, —** `rm -rf .git`

**Проверить состояние репозитория —** `git status`

**Подготовить файлы к сохранению —** `git add`

**Например:**
```bash
git add --all
git add readme.txt
```
**Выполнить коммит** — `git commit`

**Просмотреть историю коммитов —** `git log`

**GitHub быстрый старт** (https://docs.github.com/ru/get-started/quickstart)

**Для генерации SSH-пары можно использовать программу ssh-keygen.**

Откройте терминал и введите следующую команду.
```bash
ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub" 
```
**Для добавления сгенерированного ключа:**
1. Перейдите на GitHub и выберите пункт Settings (англ. «настройки») в меню аккаунта.
2. В меню слева нажмите на пункт SSH and GPG keys.
3. В открывшейся вкладке выберите New SSH key (англ. «новый SSH-ключ»).
4. В поле Title (англ. «заголовок») напишите название ключа. Например, Personal key (англ. «личный ключ»).
5. В поле Key type (англ. «тип ключа») должно быть Authentication Key (англ. «ключ аутентификации»).
6. В поле Key скопируйте ваш ключ из файла .pub.
7. Нажмите на кнопку Add SSH key (англ. «добавить SSH-ключ»).
8. Проверьте правильность ключа с помощью следующей команды.
```bash
ssh -T git@github.com 
```
**Привязать удаленный репозиторий к локальному**
```bash
cd ~/dev/first-project
git remote add origin git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ_РЕПОЗИТОРИЯ%.git 
```
**Убедиться, что репозитории связаны, —** `git remote -v`
**Отправить изменения на удалённый репозиторий —** `git push`
```bash
git push -u origin main # Если команда приведёт к ошибке, попробуйте 
                          # заменить main на master.
```						  
**Форматирование README.md** (https://gist.github.com/fomvasss/8dd8cd7f88c67a4e3727f9d39224a84c)				  