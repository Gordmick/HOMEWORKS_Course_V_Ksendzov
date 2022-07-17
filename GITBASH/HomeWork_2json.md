# HomeWork 2

## _Linux terminal (GitHub) commands_

| TASK | SOLUTION |
| ------ | ------ |
| 1. Создать внешний репозиторий c названием JSON | GitHub -> Create New Repository JSON |
| 2. Клонировать репозиторий JSON на локальный компьютер | git clone https://github.com/Gordmick/HOMEWORKS_Course_V_Ksendzov/edit/main/GITBASH/HomeWork_2json.md |
| 3. Внутри локального JSON создать файл “new.json” | cd JSON && touch new.json |
| 4. Добавить файл под гит | git add new.json |
| 5. Закоммитить файл | git commit -m "newfile" |
| 6. Отправить файл на внешний GitHub репозиторий | git push |

***7. Отредактировать содержание файла “new.json” - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате JSON***
```sh
vim new.json
{
"Full name": "Gordievskiy Mikhail Viktorovich",
"age": 36,
"pets": "five sea fish",
"future desired salary in dollars": 2000
}
```

| TASK | SOLUTION |
| ------ | ------ |
| 8. Отправить изменения на внешний репозиторий | git commit -am "change json" && git push |
| 9. Создать файл preferences.json | touch preferences.json |

***10. В файл preferences.json добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате JSON***

```sh
{
"Favorite cinema": "Interstellar",
"favorite series": "Game of Thrones",
"favorite food": "barbecue",
"favorite season": "summer",
"country you would like to visit": "Sweden"
}
```

***11. Создать файл sklls.json добавить информацию о скиллах которые будут изучены на курсе в формате JSON***

```sh
vim skills.json
{
"Skills1": "GIT",
"skills2": "SDLC",
"skills3": "STLC",
"skills4": "SQL",
"skills5": "Charles",
"skills6": "Postman",
"skills7": "JS",
"skills8": "Linux",
"skills9": "Jmeter",
"skills10": "ADB"
}
```

| TASK | SOLUTION |
| ------ | ------ |
| 12. Отправить сразу 2 файла на внешний репозиторий  | git add . && git commit -m "preferences and skill" && git push |
| 13. На веб интерфейсе создать файл bug_report.json | GitHub -> add file -> create new file -> bug_report.json |
| 14. Сделать Commit changes (сохранить) изменения на веб интефейсе | GitHub -> Commit changes |
| 15. На веб интерфейсе модифицировать файл bug_report.json, добавить баг репорт в формате JSON | GitHub -> bug_report.json -> edit this file |
```sh

{
"Summary": "Login page The button`register` not firing after clicking on the page",
"Project": "Shop H&M",
"Component": "Registration form",
"Version": "5,64",
"Severity": "Critical",
"Priority": "High",
"Status": "Open",
"Author": "Mikhail Gordievskiy",
"Steps for reproduce": "Open Login page, clicking the buttom `register`",
"Result":"The page does not go to the registration page",
"Expected Result":"The page goes to the registration page"
}
```


| TASK | SOLUTION |
| ------ | ------ |
| 16. Сделать Commit changes (сохранить) изменения на веб интерфейсе.  | GitHub -> commit changes |
| 17. Синхронизировать внешний и локальный репозиторий JSON  | git pull |

