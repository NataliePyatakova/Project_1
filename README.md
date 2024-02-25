## **Проект e-learning**
<hr>

### Стек:
Работа выполнена на Python с использованием Jupyter Notebook. Библиотеки: pandas, seaborn, matplotlib

<hr>

### Для реализации проекта необходимо решить следующие задачи:

1. Определить количество студентов, которые успешно сдали только один курс
2. Выявить самый сложный и самый простой экзамен: найди курсы и экзамены в рамках курса, которые обладают самой низкой и самой высокой завершаемостью
3. По каждому предмету определить средний срок сдачи экзаменов (под сдачей понимаем последнее успешное прохождение экзамена студентом)
4. Выявить самые популярные предметы (ТОП-3) по количеству регистраций на них. А также предметы с самым большим оттоком (ТОП-3)
5. Используя pandas, в период с начала 2013 по конец 2014 выявить семестр с самой низкой завершаемостью курсов и самыми долгими средними сроками сдачи курсов
6. Используя python, построить адаптированные RFM-кластеры студентов, чтобы качественно оценить свою аудиторию

<hr>

### Описание данных:

<strong>assessments.csv</strong> — этот датафрейм содержит информацию об оценках в тесте. Обычно каждый предмет в семестре включает ряд тестов с оценками, за которыми следует заключительный экзаменационный тест (экзамен).  
<strong>*Колонки*</strong>:
- code_module — идентификационный код предмета.
- code_presentation — семестр (Идентификационный код).
- id_assessment — тест (Идентификационный номер ассессмента).
- assessment_type — тип теста. Существуют три типа оценивания: оценка преподавателя (TMA), компьютерная оценка (СМА), экзамен по курсу (Exam).
- date — информация об окончательной дате сдачи теста. Рассчитывается как количество дней с момента начала семестра. Дата начала семестра имеет номер 0 (ноль).
- weight — вес теста в % в оценке за курс. Обычно экзамены рассматриваются отдельно и имеют вес 100%; сумма всех остальных оценок составляет 100%.

<strong>courses.csv</strong> — датафрейм содержит список предметов по семестрам.  
<strong>*Колонки*</strong>:
- code_module — предмет (идентификационный код).
- code_presentation — семестр (идентификационный код).

<strong>studentAssessment.csv</strong> — этот датафрейм содержит результаты тестов студентов. Если учащийся не отправляет работу на оценку, результат не записывается в таблицу.  
<strong>*Колонки*</strong>:
- id_assessment — тест (идентификационный номер).
- id_student — идентификационный номер студента.
- date_submitted — дата сдачи теста студентом, измеряемая как количество дней с начала семестра.
- is_banked — факт перезачета теста с прошлого семестра (иногда курсы перезачитывают студентам, вернувшимся из академического отпуска).
- score — оценка учащегося в этом тесте. Диапазон составляет от 0 до 100. Оценка ниже 40 неудачная/неуспешная сдача теста.

<strong>studentRegistration.csv</strong> - этот датафрейм содержит информацию о времени, когда студент зарегистрировался для прохождения курса в семестре.  
<strong>*Колонки*</strong>:
- code_module — предмет (идентификационный код).
- code_presentation — семестр (идентификационный код)
- id_student — идентификационный номер студента.
- date_registration — дата регистрации студента. Это количество дней, измеренное от начала семестра (например, отрицательное значение -30 означает, что студент зарегистрировался на прохождение курса за 30 дней до его начала).
- date_unregistration — дата отмены регистрации студента с предмета. У студентов, окончивших курс, это поле остается пустым.


<hr>

### Реализация проекта:
- Провела предварительное исследование и предобработку данных
- Сформулировала, что должно считаться курсом и зафиксировала эту информацию на протяжении всего проекта
- Определила количество студентов, которые сдали успешно только один курс
- Выявила самый сложный и самый простой экзамены
- По каждому предмету определила средний срок сдачи экзаменов
- Выявила ТОП-3 популярных предмета по количеству регистраций на них и предметы с самым большим оттоком
- Определила семестр с самой низкой завершаемостью курсов самыми долгими средними сроками сдачи курсов
- Провела сегментацию студентов, построила адаптированные RFM-кластеры

<hr>

### Результат:
- Выполнение проекта позволило сформировать определенную картинку об образовательной платформе как о продукте. На основе полученных результатов и выводов продуктовый менеджер сможет понять, какие курсы пользуются популярностью у пользователей, какие являются сложными, а какие наиболее легкими. Также исследование предоставит возможность продуктовому отделу выработать представление о сегментах пользователей данной платформы для дальнейшей разработки каких-либо решений, направленных на развитие и продвижение продукта. 
