---
{"dg-publish":true,"permalink":"/instrukcziyi/gramps/yak-zminiti-movu-interfejsu-gramps-na-ukrayinsku-v-mac-os/","dgPassFrontmatter":true,"created":"2025-05-13T19:50:17.000+02:00","updated":"2025-05-13T19:59:06.000+02:00"}
---

### **Крок 1: Відкрити вміст програми Gramps**

1. Відкрийте папку **Програми (Applications)**.
2. Знайдіть **Gramps.app**.
3. Клацніть по Gramps правою кнопкою миші (або Ctrl + клік) і виберіть **“Показати вміст пакету” (Show Package Contents)**.

### **Крок 2: Перейти до файлу запуску**

1. Перейдіть у папку: Contents → Resources
2. Знайдіть файл **gramps_launcher.py**.

### **Крок 3: Відкрити файл у текстовому редакторі**

1. Клацніть правою кнопкою на файлі gramps_launcher.py.
2. Виберіть **“Відкрити за допомогою” → “TextEdit”** (або інший текстовий редактор).
### **Крок 4: Внести зміни**

1. Знайдіть рядок:
```python
app.main()
```
2. Безпосередньо перед цим рядком вставте наступний код:
```python
from os import environ
environ["LANG"] = "uk_UA.UTF-8"
environ["LANGUAGE"] = "uk"
environ["LC_MESSAGES"] = "uk_UA.UTF-8"
environ["LC_TIME"] = "uk_UA.UTF-8"
```
### **Крок 5: Зберегти файл**

1. Збережіть файл (**Файл → Зберегти**).  
2. Закрийте редактор.

### **Крок 6: Запустити Gramps**

1. Відкрийте Gramps із папки **Програми**.
2. Інтерфейс повинен відображатися українською мовою.