# dn-bundles

### Как добавить свой пакет:
1. Ставим git
2. Делаем форк этого репозитория
3. Делаем git clone уже форкнутого репозитория ( который находится у вас в профиле )
```bash
git clone ссылка на форкнутый репозиторий
```

4. переходим в директорию проекта
```bash
cd dn-bundles
```

5. Создаем ветку ( желательно назвать ветку по своему )
```bash
git branch YourBranchName
```

6. Переходим в созданую ветку
```bash
git checkout YourBranchName
```

7. Добавляем файлы

8. Дальше выполняем такие команды ( незабудьте поменять на свои значения название пакета и ветки )
```bash
git add *.*
git commit -m "Added bundle YourBundleName"
git push --set-upstream origin YourBranchName
```

Гит попросит авторизоваться, авторизуетесь любым удобным способом ( для линуксоидов: гуглите как там это делается, насколько я знаю там не будет окна авторизации как в винде )

После того как зальете изменения на странице репозитория сверху появится плашка с кнопкой "create pull request" нажимаете ее, создаете пулл реквест и ждете когда я его приму или отклоню

### Структура
bundles - то куда закидываете ваш пакет, вместо пробелов используйте нижнее подчеркивание

images - иконка пакета, размер желателен не больше чем 32х32

bundle-list-v2.json - сюда добавляете всю информацию о файле
```json
{
    "name": "Название пакета должно быть таким же как в DN (в конфиге пакета ключ 'name')",
    "description": "Описание",
    "author": "автор",
    "image": "НАЗВАНИЕ_ИКОНКИ.png",
    "version": "1.0.0",
    "exampleUrl": "Ссылка на пример как использовать пакет)",
    "url": "НАЗВАНИЕ_ПАКЕТА.dnbundle"
}
```
exampleUrl: `это может быть просто проект или ссылка на git страничку с кодом (это не обязательный парраметр, если нет ссылки то указывать не надо`

Незабудьте добавить запятую после последнего пакета в списке