# Описание данных



1. ### /hydro/

   Полный архив данных наблюдений на гидрологических постах сети Росгидромета за период с 1984 по 2018 гг. Содержит данные об уровнях воды, расходах, температуре воды, наблюдения за поверхностью воды (становление ледостава, вскрытие).

  ## Датафрейм daily

  Cобран из 198 csv-файлов 

  Содержат ежедневные значения уровня воды на гидрологический постах за период с 1984 по 2018 гг.

  date - дата измерений

  stage_avg - средний уровень воды за день (см.)

  stage_min - минимальный уровень воды за день (см.)

  stage_max – максимальный уровень воды за день (см.)

  temp - средняя температура воды за день (°C)

  water_code - код состояния водного объекта

  id - номер гидрологического поста

  ## Датафрейм ice

  Cобран из 181 csv-файлов 

  Содержит периодические значения (раз в 5 дней) высоты снега и толщины льда на гидрологическом посте

  date datetime64[ns] - дата измерения

  ice_high Толщина льда (см)

  snow_high Высота снега (см)

  place_code'Место измер - код места ледовых измерений

  id - номер гидрологического поста

    

2. ### /hydro_2019-2020

- **new_data_all.csv**

  Файл с данными только об уровнях воды за период 01-01-1984 — 01-10-2020.  Содержит не только архивные данные, но и оперативные с 2018 по настоящее время.

  - 'time' - дата замера
  - 'max_level' - максимальный уровень за день
  - 'identifier' - номер гидрологического поста

- **new_data_target.csv** 

  ​	Подмножество файла **new_data_all.csv** для целевых гидрологических постов

  

3. ### /meteo/

   Архив данные наблюдений на метеостанциях сети Росгидромета с 1985 по 2018  

  meteo_df - это датафрейм, собранный из 108 файлов meteo/NNNNNNN.csv, где NNNNNNN номер синтаптической станции meteo_df содержит архив наблюдений на метеостанциях сети Росгидромета с 1985 по 2018, всего 108 станций  
  в датафрейме 9959296 строк, 21 колонка  
  Названия колонок:  
  1 station_name Название станции  
  2 station_id Идентификатор станции  
  3 visibility_distance Горизонтальная дальность видимости  
  4 visibility_distance_quality Признак качества  
  5 wind_direction Направление ветра  
  6 wind_direction_quality Признак качества  
  7 wind_speed_avg Средняя скорость ветра  
  8 wind_speed_avg_quality Признак качества  
  9 wind_speed_sign Признак наличия знака >  
  10 wind_speed_max Максимальное скорость ветра  
  11 wind_speed_max_quality Признак качества  
  12 wind_speed_max_sign Признак наличия знака >  
  13 precipitation_amount Сумма осадков за период между сроками  
  14 precipitation_amount_quality Признак качества  
  15 temperature_ground Температура поверхности почвы в срок  
  16 temperature_ground_quality Признак качества  
  17 temperature_air Температура воздуха в срок по сухому терм-ру  
  18 temperature_air_quality Признак качества  
  19 humidity Относительная влажность воздуха в срок  
  20 humidity_quality Признак качества  
  21 time Срок наблюдения  
  Типы данных float64(10), int64(9), object(2)  
  

1. ### /meteo_new

   Датасет с данными наблюдений на метеостанциях за период с 01-01-1984 по 31-03-2020. Количество станций меньше (только те, что входят сеть Всемирной Метеорологической Организации), чем в прошлом, но больше полей и охват
  
    #### До обработки
* **{номер метеостанции}.csv**
  * stationNumber  Синоптический индекс станции Всемирной Метеорологической организации 
  * date формат year-month-day hour:minutes:seconds год месяц день срок по Гринвичу
  * localDate формат year-month-day hour:minutes:seconds год месяц день срок источника (местный)
  * timePeriodNum  Номер срока в сутках по поясному декретному зимнему времени (ПДЗВ)  
  * localTime  Время местное  
  * tz  Номер часового пояса  
  * startMeteoDay  Начало метеорологических суток по ПДЗВ  
  * horizontalVisibility  Горизонтальная видимость  
  * horizontalVisibilityQuality  Признак качества  
  * horizontalVisibilitySign  Признак наличия знака «>»  
  * cloudCoverTotal  Общее количество облачности  
  * cloudCoverTotalQuality  Признак качества  
  * pastWeather  Погода между сроками  
  * pastWeatherQuality  Признак качества  
  * presentWeather  Погода в срок наблюдения  
  * presentWeatherQuality  Признак качества  
  * windDirection  Направление ветра  
  * windDirectionQuality  Признак качества  
  * windSpeed  Средняя скорость ветра  
  * windSpeedQuality  Признак качества  
  * windSpeedSign  Признак наличия знака «>»  
  * maximumWindGustSpeed  Максимальная скорость ветра  
  * maximumWindGustSpeedQuality  Признак качества  
  * maximumWindGustSpeedSign  Признак наличия знака «>»  
  * totalAccumulatedPrecipitation  Сумма осадков за период между сроками  
  * totalAccumulatedPrecipitationQuality  Признак качества  
  * soilTemperature  Температура поверхности почвы  
  * soilTemperatureQuality  Признак качества  
  * groundMinimumTemperature  Минимальная температура поверхности почвы  
  * groundMinimumTemperatureQuality  Признак качества  
  * airTemperature  Температура воздуха по сухому термометру  
  * airTemperatureQuality  Признак качества  
  * minimumTemperatureAtHeightAndOverPeriodSpecified  Минимальная температура воздуха между сроками  
  * minimumTemperatureAtHeightAndOverPeriodSpecifiedQuality  Признак качества  
  * maximumTemperatureOverPeriodSpecified  Максимальная температура воздуха между сроками  
  * maximumTemperatureOverPeriodSpecifiedQuality  Признак качества  
  * relativeHumidity  Относительная влажность воздуха  
  * relativeHumidityQuality  Признак качества  
  * vapourPressure  Дефицит насыщения водяного пара  
  * vapourPressureQuality  Признак качества  
  * dewpointTemperature  Температура точки росы  
  * dewpointTemperatureQuality  Признак качества  
  * pressure  Атмосферное давление на уровне станции  
  * pressureQuality  Признак качества  
  * pressureReducedToMeanSeaLevel Атмосферное давление на уровне моря  
  * pressureReducedToMeanSeaLevelQuality  Признак качества  
  * characteristicOfPressureTendency Характеристика барической тенденции  
  * characteristicOfPressureTendencyQuality  Признак качества  
  * HourPressureChange3  Величина барической тенденции  
  * HourPressureChange3Quality  Признак качества  stationId  идентификатор локальный (атрибут _meteo_ в [АСУНП](http://asunp.meteo.ru/geoits-rest/services/asunp/geo.json))

  #### После обработки

  0   stationNumber                                     Синоптический индекс станции Всемирной Метеорологической организации  
  1   timePeriodNum                                     Номер срока в сутках по поясному декретному зимнему времени (ПДЗВ)  
  2   localTime                                         Время местное  
  3   tz                                                Номер часового пояса  
  4   startMeteoDay                                     Начало метеорологических суток по ПДЗВ  
  5   horizontalVisibility                              Горизонтальная видимость  
  6   horizontalVisibilityQuality                       Признак качества  
  7   cloudCoverTotal                                   Общее количество облачности  
  8   pastWeather                                       Погода между сроками  
  9   presentWeather                                    Погода в срок наблюдения  
  10  windDirection                                     Направление ветра  
  11  windSpeed                                         Средняя скорость ветра  
  12  maximumWindGustSpeed                              Максимальная скорость ветра  
  13  totalAccumulatedPrecipitationQuality              Признак качества  
  14  soilTemperature                                   Температура поверхности почвы  
  15  groundMinimumTemperature                          Минимальная температура поверхности почвы  
  16  airTemperature                                    Температура воздуха по сухому термометру  
  17  minimumTemperatureAtHeightAndOverPeriodSpecified  Минимальная температура воздуха между сроками  
  18  maximumTemperatureOverPeriodSpecified             Максимальная температура воздуха между сроками  
  19  relativeHumidity                                  Относительная влажность воздуха  
  20  vapourPressure                                    Дефицит насыщения водяного пара  
  21  dewpointTemperature                               Температура точки росы  
  22  pressure                                          Атмосферное давление на уровне станции  
  23  pressureReducedToMeanSeaLevel                     Атмосферное давление на уровне моря  
  24  characteristicOfPressureTendency                  Характеристика барической тенденции  
  25  HourPressureChange3                               Величина барической тенденции  
  26  stationId                                         int64  
  27  date                                              datetime64[ns]  
  28  localDate                                         datetime64[ns]  

