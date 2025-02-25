# NM


Описание данных  
Данные находятся в файле `/datasets/autos.csv.`  

Признаки (features)  
`DateCrawled` — дата скачивания анкеты из базы.  
`VehicleType` — тип автомобильного кузова.  
`RegistrationYear` — год регистрации автомобиля.  
`Gearbox` — тип коробки передач.  
`Power` — мощность автомобиля (л. с.).  
`Model` — модель автомобиля.   
`Kilometer` — пробег автомобиля (км).  
`RegistrationMonth` — месяц регистрации автомобиля.  
`FuelType` — тип топлива.  
`Brand` — марка автомобиля.  
`Repaired` — информация о том, был ли автомобиль в ремонте. 
`DateCreated` — дата создания анкеты.  
`NumberOfPictures` — количество фотографий автомобиля.  
`PostalCode` — почтовый индекс владельца анкеты (пользователя).  
`LastSeen` — дата последней активности пользователя.  
Целевой признак (target)  
`Price` — цена автомобиля (в евро).  
Данные содержат информацию о характеристиках автомобилей, их пробеге, состоянии и параметрах регистрации, что позволяет использовать их для прогнозирования стоимости автомобилей на вторичном рынке.  



Отчет по выполненному проекту
Сервис по продаже автомобилей с пробегом «Не бит, не крашен» разрабатывает приложение, которое поможет пользователям оценивать рыночную стоимость своего автомобиля. Для этого была построена модель машинного обучения, способная предсказывать цену автомобиля на основе его характеристик.

Этапы работы:   
1. Загрузка и изучение данных  
Данные были загружены из файла `/datasets/autos.csv.`  
Проведено исследование структуры данных:  

Проверено наличие пропусков и аномальных значений.  
Выполнено заполнение и обработка пропусков в признаках.  
Удалены неинформативные столбцы, которые не влияли на предсказания.  
2. Подготовка данных  

Данные разделены на обучающую, валидационную и тестовую выборки.
Категориальные признаки закодированы.  
Числовые признаки масштабированы.  
3. Обучение и сравнение моделей  
Обучены и протестированы несколько моделей:  

Градиентный бустинг (LightGBM).
Более простая модель (например, LinearRegression или RandomForest).  
Для каждой модели выполнен подбор гиперпараметров.  
Оценены ключевые параметры моделей:  

Время обучения.  
Время предсказания.  
Качество предсказаний (метрика RMSE).  
4. Выбор лучшей модели  
На основе критериев заказчика:  

Оптимизирован баланс между качеством предсказаний, временем обучения и временем предсказания.  
Выбрана модель, обеспечивающая наименьшее значение RMSE (< 2500).  
Проверено качество лучшей модели на тестовой выборке.  
Итоговые выводы  
Построена модель, которая предсказывает рыночную стоимость автомобилей с высокой точностью.  
Проведено сравнение моделей, выявлена оптимальная по критериям заказчика.  
Достигнуто значение RMSE ниже 2500, что подтверждает успешность решения задачи.  
Результаты могут быть использованы в дальнейшем развитии приложения для оценки стоимости автомобилей, а также в бизнес-стратегии сервиса «Не бит, не крашен».  