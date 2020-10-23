# Дататон

### Авторы & распределение ролей в команде
- Андрей Ветров - продакт-менеджер, разработчик (обработка данных hydro), тимлид по созданию датасетов
- Анна Казанцева - проджект-менеджер,разработчик (обработка данных meteo)
- Михаил Стриженов - разработчик (обработка данных meteo_new), описание артефактов в GitHub
- Максим Щиколодков - главный дизайнер в Miro, описание артефактов в Miro
- Максим Бобуров - разработчик (обработка данных hydro_2018-2020)

### Описание датасета
Датасет содержит полный архив данных наблюдений на гидрологических постах сети Росгидромета за период с 1984 по 2018 гг. Содержит данные об уровнях воды, расходах, температуре воды, наблюдения за поверхностью воды (становление ледостава, вскрытие).

### Источник структуры датасета
Структура датасета содержит данные о погоде с гидрологических постов. Датасет прендназначен для разработки алгоритм прогнозирования уровней воды р. Амур для следующих населенных пунктов (гидропостов): Джалинда, Благовещенск, Иннокентьевка, Ленинское, Хабаровск, Комсомольск-на-Амуре, Николаевск-на-Амуре на 10 дней вперед.

### Методы сбора и обработки данных
Информация предоставлена Росгидрометом с сетей гидрологических постов. Данные сгруппированы по параметрам и представлены в формате csv.

### Структура репозитория
Jupiter notebook, dfs_description.md (описание датасета), README.md и ссылку на датасет.

### Формат данных
Датасет содержит([готовые pkl файлы](https://yadi.sk/d/Da5pcOMhg-dnPQ)): 
- Датафрейм daily
Содержит ежедневные значения уровня воды и температуры воды на гидрологический постах за период с 1984 по 2018 гг.
Cобран из 198 csv-файлов

- Датафрейм ice
Содержит периодические значения (раз в 5 дней) высоты снега и толщины льда на гидрологических постах за период с 1984 по 2018 гг.
Cобран из 181 csv-файлов

- Датафрейм meteo
Cобран из 108 файлов meteo/NNNNNNN.csv, где NNNNNNN номер синтаптической станции. Cодержит архив наблюдений на метеостанциях сети Росгидромета с 1985 по 2018, всего 108 станций

- Датафрейм meteo_new
Содержит данные наблюдений на метеостанциях за период с 01-01-1984 по 31-03-2020. Количество станций меньше (только те, что входят сеть Всемирной Метеорологической Организации), чем в прошлом, но больше полей и охват Cобран из 34 csv-файлов

- Датафрейм hydro_2018_2020
Cобран из 1 файла Содержит ежедневные значения уровня воды на гидрологический постах за период с 2018 по настоящее время.
