����� ������
init - ����� �����
Config ##��� ������������ � ���������
git config ( /etc/gitconfig --system !3
		~/.config/git/config --global !2
			.git/config ����������� ��������� ����������� !1 )
� �������� ��������� Windows Git ���� ���� .gitconfig � �������� $HOME (C:\Users\$USER ��� ����������� �������������). 
����� ����, Git ���� ���� /etc/gitconfig, �� ��� ������������ ��������� �������� MSys, 
������� ��������� ���, ���� �� ������ ���������� Git, ����� ��������� �����������.

$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com

$ git config --global core.editor <emacs> ��� emacs - �������� �������

git config --list

git clone https git:// or user@server:path/to/repo.git

����������� ��������� ������ � ����������/���������-����������/

����� ��������� https://git-scm.com/book/en/v2/images/lifecycle.png
git status - ��������� ������ ��� git status -s
gid add

������������� ������
���� .gitignore
$ cat .gitignore 
*.[oa]  /** ������ ������ ������������ Git ������������ ����� ����� ��������������� �� ``.o`` ��� ``.a`
*~ - ��������� �����
[!oa].* - (!) � �������� ������� �������. ������������ "o" ��� "a" �������

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

������ ������, � ����� ������, ������������ � #, ������������.
����� ������������ ����������� glob �������.
����� ������ ������ �������� ����� (/) ����� �������� ��������.
����� ����������� ������ �������� ����� (/) ��� �������� ��������.
����� ������������� ������, ����������� ��������������� ���� (!) � �������� ������� �������. 


