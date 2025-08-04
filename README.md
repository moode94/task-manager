

1. إعداد المشروع:
- سويت مجلد جديد وبدأت مستودع Git:
  
  git init
  

أنشأت ملف اسمه `tasks.txt` وضفت فيه مهمات مثل:
  - Learn Git basics
  - Set up Git repository

 2. أضفت المهام وسويت commit:

git add tasks.txt
git commit -m "Add initial tasks"


3. اشتغلت على فروع:

فرع لإضافة مهام:
 
  git checkout -b feature/add-tasks

  وضفت مهام وسويت commit.

- فرع لحذف مهام:

  git checkout -b feature/remove-tasks

  حذفت مهمة وسويت commit.

4. دمج الفروع:

- رجعت للفرع الرئيسي ودمجت الفرعين:

  git checkout master
  git merge feature/add-tasks
  git merge feature/remove-tasks


- إذا صار تعارض عدلت الملف يدوياً وسويت commit.
 5. استخدمت rebase:

- أنشأت فرع `feature/update-tasks` وعدلت مهمات.
- بعدين سويت rebase:
  
  git checkout master
  git rebase feature/update-tasks
  

 6. تراجعت عن خطأ:

- أضفت مهمة خاطئة وسويت commit.
- تراجعت عنها بـ:

  git revert <commit-id>
 

7. رفعت المشروع على GitHub:

- أضفت المستودع البعيد:

  git remote add origin <repo-url>
  git push -u origin master
