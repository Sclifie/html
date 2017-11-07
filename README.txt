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
gid add

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


