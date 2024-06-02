# Проект "Анализ вакансий"

## Цель проекта
Изучение рынка труда в Москве и других городах центральной России для того, чтобы построить взаимосвязи между требованиями к сотрудникам и предложенными условиями работы. Анализ влияния ключевых факторов на размер заработной платы в вакансиях. Обучение модели линейной регрессии, предсказывающей значения заработной платы на основе опыта работы, рейтинга компании, факта нахождения в офисе и уровня занятости. Данные для анализа взяты с сайта [hh.ru](https://hh.ru).

## Шаг 1:
Изначально мы хотели брать готовый датасет с китайскими акциями, поскольку боялись, что не сможем ничего спарсить

## Шаг 2:
Но у нас получить [спарсить](https://github.com/knastas1a/project/blob/main/1.parsing/1.0_hh_parsing.ipynb) данные с сайта [hh.ru](https://hh.ru), поэтому мы переквалифицировались. 

## Шаг 3:
У нас получилось 8 столбцов: ссылка на вакансию, должность, заработная плата (указана через промежуток), компания, город, требуемый опыт, занятость и рейтинг компании. Собранные данные требовали некоторых [преобразований](https://github.com/knastas1a/project/blob/main/2.EDA/2.0_EDA.ipynb). Мы обработали столбец с зарплатой  так, чтобы там было одно число, из рейтинга тоже сделали число. Мы проверили данные на пропуски, их не оказалось (изначально было прописано в парсинге). В столбце "Занятость" получалось 2 признака, которые мы и разделили на отдельные столбцы - занятость по времени и локация сотрудника. Итого у нас получилось 3 категориальные переменные и две числовые. 

## Шаг 4:
Перед визуализацией [подготовили данные](https://github.com/knastas1a/project/3.visualisation/3.0_prep_for_visualisation.ipynb): добавили описание переменных, поправили значения в city (Москва/Другое), также немного изменили и другие признаки. После этого мы приступили к построению [графиков](https://github.com/knastas1a/project/3.visualisation/3.1_plots&thoughts.ipynb) и их анализу. Хочкется отдельно отметить интересный вывод из графика взаимосвязи зарплаты и рейтинга работодателей: мы заметили большое количество зарплат выше среднего, предложенных компаниями с рейтингом 2.0 - интересно подумать над обманом на рынке труда.

## Шаг 5:
Далее мы проверили несколько [гипотез](https://github.com/knastas1a/project/blob/main/4.hypotheses/4.0_hypotheses.ipynb). Во-первых, мы предположили, что высокий рейтинг компании не влияет на размер заработной платы, однако, по результатам t-теста, оказалось, что это не так. Во-вторых, было логично протестировать связь опыта работы и заработной платы, так, у нас получилось, что наличие большого опыта работы всё-таки играет роль.

## Шаг 6:
Перед обучением мы ещё немного поработали с  данными. С помощью [ОНЕ-кодирования](https://github.com/knastas1a/project/blob/main/5.ML/5.0_OHE.ipynb) преобразовали категориальные переменные.
Затем мы [обучили модель](https://github.com/knastas1a/project/blob/main/5.ML/5.2_ML.ipynb) c помощью метода линейной регрессии, в качестве метрики качества использовали МАЕ.

_Проект подготовлен командой "шКодим", а именно - студентками Беляевой Анастасией, Ибрагимовой Анной                           и Карповой Анастасией. Спасибо за внимание!_
