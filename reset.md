## A3. stash, reset, revert для управления изменениями
#### Изменения можно временно припрятать
#### Можно получить разницу между любыми коммитами
#### Коммит можно отменить другим коммитом
- `git stash` — сохранить все модифицированные файлы в виде набора изменений
- `git stash pop` — восстановить последний сохраненный набор изменений и удалить его из списка
- `git stash list` — показать список сохраненных наборов изменений
- `git reset --hard <commit>` — переместить текущую ветку на `<commit>`, задать индекс и директорию согласно коммиту, устранив всю разницу
- `git reset --mixed <commit>` — переместить текущую ветку на `<commit>`, задать индекс согласно коммиту, оставить разницу между исходным и новым состоянием в директории
- `git reset --soft <commit>` — переместить текущую ветку на `<commit>`, не задавать индекс и директорию согласно коммиту, а оставить разницу между исходным и новым состоянием в индексе и директории
- `git reset --hard HEAD~1` — отменить последний коммит
- `git revert <commit>` — создать коммит, отменяющий изменения из коммита
- `git diff <from_commit> [<to_commit>]` — вывести разницу между двумя коммитами
- `git diff --name-status <from_commit> [<to_commit>]` — список измененных файлов
- `git difftool <from_commit> [<to_commit>]` - вывести разницу с помощью difftool из настроек