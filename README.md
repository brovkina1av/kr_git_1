cd kr_git_1
git remote add origin https://github.com/brovkina1av/kr_git_1/edit/main/README.md
git push -u origin master
mkdir kr_git_1
cd kr_git_1
git init
git config user.name brovkina1av
git config user.email taras090130@gmail.com
echo "Курс \"Промышленное программирование\", контрольная работа." > README.txt
date +"%d.%m.%Y" >> README.txt  
echo brovkina1av >> README.txt
git add README.txt
git commit -m "Initial commit: README.txt with date and author"
git checkout -b solution_A
echo "print('Решение задачи \"Геометрические фигуры\"')" > geom.py
git add geom.py
git commit -m "Add solution for geometric figures (geom.py)"
git checkout master
git checkout -b solution_B
echo "print('Решение задачи \"Дроби: равенство\"')" > fract.py
git add fract.py
git commit -m "Add solution for fraction equality (fract.py)"
git checkout solution_A
git checkout -b result_AB
git merge solution_B --no-ff
