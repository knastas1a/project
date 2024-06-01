# Проект по hh.ru

## Шаг 1:
Изначально мы хотели брать готовый датасет с китайскими акциями, поскольку боялись, что не сможем ничего спарсить

## Шаг 2:
Но у нас получить спарсить данные с сайта хх, поэтому мы переквалифицировались. Цель нашего проекта - научиться предсказывать заработную плату в зависимости от занятости, рейтинга компании и формата работы (удаленка, офис и тд). Также хотим попробовать кластеризовать должности и построить прогноз на этой основе в том числе. 

## Шаг 3:
У нас получилось 8 столбцов: ссылка на вакансию, должность, з/п (указана через промежуток), компания, город, требуемый опыт, занятость и рейтинг компании. Обработали столбец с зп так, чтобы там было одно число, из рейтинга тоже сделали число. В столбце "Занятость" получалось 2 признака, которые мы и разделили на отдельные столбцы - занятость по времени и локация сотрудника. Итого у нас получилось 3 потенциально категориальные переменные и две числовые.
