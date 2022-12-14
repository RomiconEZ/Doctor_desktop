# Разработчики
* Даутов Руслан 
* Неронов Роман 
* Смолина Алина 
* Менкеев Александр 
* Ивашечкин Алексей 
# Описание
1. Разработать концепцию “Рабочего стола” с разработкой 5 пользовательских режимов с разными функциями. Пользовательские режимы: Разработчик, Соразработчик, Администратор [клиники, центра], Врач, Регистратура.
2. Создать удобный и интуитивно понятный интерфейс.
3. Автоматизировать передачу выбранных данных нейросети на “Рабочий стол”.
4. Сделать страницу Входа, чтобы у каждого врача был свой профиль.
## Наименование
Рабочий стол кардиохирурга
## Предметная область
Врачи и сотрудники учреждений
Пациенты
Данные КТ
# Данные
https://app.quickdatabasediagrams.com/#/d/gM3Nav
## Общие ограничения целостности
Разграничение доступа к удалению и добавлению сотрудников(только администратор может удалять и добавлять сотрудников)
Разграничение доступа к удалению и добавлению пациентов(только врач и регистратура может удалять и добавлять пациентов)
# Пользовательские роли
* Разработчик
* Соразработчик
* Администратор
* Врач
* Регистратура
## Для каждой роли - наименование, ответственность, количество пользователей в этой роли?
* Разработчик - developer (возможность добавлять данные КТ (в формате DICOM), ЭХОКГ, антропометрии пациента, клинические данные и данные анамнеза пациент; возможность расширения функций соразработчиков и врачей/экспертов.)
* Соразработчик - codeveloper (Возможность вносить "сырые" данные КТ (в формате DICOM), ЭХОКГ, антропометрии пациента, клинические данные и данные анамнеза пациента.)
* Администратор - admin (функция добавления и регулирования деятельности профилей врачей/экспертов пределах учреждения (клиники/центра))
* Врач - doctor (возможность загрузки в специальных формах  "сырых" данных КТ (в формате DICOM либо цифровые показатели, размеров и состояния аорты на различных уровнях), ЭХОКГ, антропометрии пациента, клинические данные и данные анамнеза пациент. Далее отправляет эти данные для анализа нейросети и получает заключение о наличии/отсутствии патологии или сомнительном диагнозе). Возможность добавлять пациента, редактировать его персональные данные и медицинские данные. Возможность удалять пациента.
* Регистратура - regis (возможность удаления пациента, возможность добавления пациента и его персональных данных.)

# UI / API
Страницы:
* страница логина
* главное меню
* личная страница врача
* список пациентов
* список сотрудников
* страница карточки пациента
* страница карточки сотрудника(просмотр/редактирование)
* страница добваления пациента
* страница добавления сотрудника

# Технологии разработки
* React
* Laravel
## Язык программирования
* Typescript
* PHP
## СУБД
MySQL
