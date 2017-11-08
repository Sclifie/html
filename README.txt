Новый проект
init - новая папка
Config ##Имя пользователя и настройки
git config ( /etc/gitconfig --system !3
		~/.config/git/config --global !2
			.git/config наследовать параметры репозитория !1 )
В системах семейства Windows Git ищет файл .gitconfig в каталоге $HOME (C:\Users\$USER для большинства пользователей). 
Кроме того, Git ищет файл /etc/gitconfig, но уже относительно корневого каталога MSys, 
который находится там, куда вы решили установить Git, когда запускали инсталлятор.

$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com

$ git config --global core.editor <emacs> где emacs - название эдитора

git config --list

git clone https git:// or user@server:path/to/repo.git

Определение состояния файлов и добавление/изменение-добавление/

жизнь состояния https://git-scm.com/book/en/v2/images/lifecycle.png
git status - состояния файлов или git status -s
gid add или git add *
git reset HEAD <file> вывод фала из add(отмена подготовки)
git checkout -- <file>  откат фала к предыдущей версии(причём перманентный)
git commit - открытие тестового редактора и коммент ит в нём
git commit -m "коментируем"
git commit -a -закомментировали, теперь меняем и скаждым коммитом не пользуемся ADD - использовать если ты главный над файлом проекта
$git commit --amend -операция отмены изменений, изменяется только комментарий
Пример:
$git commit -m 'название коммита'
$git add nazvanie faila
$gir commit --amend 
В итоге получится единый коммит — второй коммит заменит результаты первого.

git diff - не проиндексированные изменения
git diff <file-name> 
git diff --staged индексированные изменения после коммита
!!!!!!! git difftool --tool-help - используем тулзу

Игнорирование файлов
файл .gitignore
$ cat .gitignore 
*.[oa]  /** Первая строка предписывает Git игнорировать любые файлы заканчивающиеся на ``.o`` или ``.a`
*~ - временные файлы
[!oa].* - (!) в качестве первого символа. игнорировать "o" или "a" вначале

# no .a files
*.a
# but do track lib.a, even though you're ignoring .a files above
!lib.a
# only ignore the root TODO file, not subdir/TODO
/TODO
# ignore all files in the build/ directory
build/
# ignore doc/notes.txt, but not doc/server/arch.txt
doc/*.txt
# ignore all .txt files in the doc/ directory
doc/**/*.txt

Пустые строки, а также строки, начинающиеся с #, игнорируются.
Можно использовать стандартные glob шаблоны.
Можно начать шаблон символом слэша (/) чтобы избежать рекурсии.
Можно заканчивать шаблон символом слэша (/) для указания каталога.
Можно инвертировать шаблон, использовав восклицательный знак (!) в качестве первого символа. 

Работа с удалёнными репозиториями
git push origin master or git push <remote-name> <branch-name>
git remote
git remote add pb <url-репозитория>
git clone url далее>>
git fetch название(origin или что-то ещё) получение изменений со стороны удалённого репозитория



