### GIT SHPORA V1.0

__ПУНКТ 1 Глобальные настройки конфига гита (контактные даннык для обратной связи)__
_git config --global user.name "Name Surname"_

__ПУНКТ 1.1__
_git config --glibal user.email "Email"_

---

__ПУНКТ 2 Иницилизация гита в нужную директорию__
_cd путь к директории (можно стразу открыть нужную папку и использовать команду ПУНКТ 2.1)_

__ПУНКТ 2.1 сообщаем гиту что эту директорию нужно сдеть репозиторием__
_git init_

---

__ПУНКТ 3 звязывание локального и удаляного репозитория__
_git remote add origin URL (удаленного репозитория)_

---

__ПУНКТ 4 Скачивание локального репозитория__
cd путь к директории (можно стразу открыть нужную папку и использовать следующую команду)

__ПУНКТ 4.1__
_git clone URL (удаленного репозитория) ДАННАЯ ПАПКА СРАЗУ ЯВЛЯЕТЬСЯ ЛОКАЛЬНИМ РЕПОЗИТОРИЕМ СВЯЗАНЫМ С УДАЛЕННЫМ РЕПОЗИТОРИЕМ И НЕ НУЖНО ПОВТОРЯТЬ ПУНКТ 2 - 2.1!!!_

---

__ПУНКТ 5 Отслеживание текущего статуса файла (у меня красным подсвечивалось неподготовленные к комиту файлы (измененное) зеленым подготовленые)__
_git status_

---

__ПУНКТ 6 Коммиты (подготовка файлов к сохранению (гит понимает что изменения в файле готовы к сохранению) только подготовленные файлы будут закомичены див. ПУНКТ 7)__
git add путь 

_Пример 1 папка/файл_ 

_Пример 2 . (git add .) коммит всех файлов_

---

__Для проверки повторяем ПУНКТ 5 должно подсвечивать зеленым__

---

__ПУНКТ 7 Коммиты сохраняем коммит в истории коммитов (по сути это чекпоинт к которому можно будет откатиться)__
_git commit -m "Название что бы можно было понть что тут или что было измененно"_

---

__ПУНКТ 8 Откат к нужной версии (коммиту)__ 
_git checkout хешкоммита_ 

---

__ПУНКТ 9 Загрузка на отдаленный репозиторий__
_git push (название репозитория (любой локальный репозиторий знает свой отдаленый под кодовым именем)) __origin__ далее имя ветки куда готим запушит изменения по дефолту main но может быть (master)_

---

__ПУНКТ 10 Допустит вы склонировали проект до дого как добавился какой-то нужный файл и вам он нужен__
_git pull origin main/(master) описание подходит из __ПУНКТА 9__
(Будут подкачаны все недостающие файлы (самая актуальная версия)) + истоия всех коммитов_

---

__ПУНКТ 11 Работа с ветками__
_git branch список всех доступних веток (__*__ отмечена ветка на которой вы находитесь)_

__ПУНКТ 11.1 Создание ветки__
_git branch название ветки которую мы хотим создать (новая dетка создается на основе данных осyовной ветки тоесть при создании они будут одинаковы)_

__ПУНКТ 11.2 Переключение веток__
_git checkout Имя ветки на которую хотим перейтиы_

__ПРИМЕЧАНИЕ коммит в новой ветке будет именно в НОВОЙ ветке а не в МЕЙН/МАСТЕР__

__ПУНКТ 11.3 Публикация новой ветки на удаленный репозиторий__
_git push origin название ветки (обычно называеться так же как вы ее назвали при создании)_

__ПУНКТ 11.4 СЛИЯНИЕ ВЕТОК__
_Сначла переходин в ту ветку в __КОТОРУЮ БУДЕМ ДЕЛАТЬ СЛИЯНИЕ ПУНКТ 11.2__

__ПУНКТ 11.4.1__ 
_git merge имя ветки которую вы хотив влить в ту ветку в КОТОРОЙ НАХОДИМСЯ СЕЙЧАС_

__ПУНКТ 11.4.2__ 
_git rebase имя ветки которую вы хотив влить в ту ветку в КОТОРОЙ НАХОДИМСЯ СЕЙЧАС_

_Разница между __11.4.1 и 11.4.2__ в том что __11.4.1__ в истории коммитов будет как один коммит а в __11.4.2__ будет вся история коммитов которые были в побочной ветки которую влили в основную (__в основном истользуеться 11.4.1__)_