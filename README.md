# Предсказание цены квартиры по её характеристикам
## Описание
В следующем наборе данных представлена небольшая выборка цен на квартиры в Москве.

Признаки:
price: цена квартиры в $1000 / the price of a flat in 1000$;

totsp: общая площадь квартиры, кв.м. / total square of a flat, m2;

livesp: жилая площадь квартиры, кв.м. / living square of a flat, m2;

kitsp: площадь кухни, кв.м. / kitchen square, m2;

dist: расстояние от центра в км. / distance to the city center, km;

metrdist: расстояние до метро в минутах / distance to the nearest metro station, min;

walk: 1 – пешком от метро, 0 – на транспорте / 1 - walk to metro, 0 - using transport;

brick: 1 – кирпичный, монолит ж/б, 0 – другой / 1 - brick, monolithic house, 0 - anothers;

floor: 1 – этаж кроме первого и последнего, 0 – иначе / 0 - the first or the last floor, 1 - anothers;

code: число от 1 до 8, обозначающее район города / number from 1 to 8 of the city area:

    1. Север, около Калужско-Рижской линии метро / North of the city, around Kaluzhsko-Rizhskaya metro line;
    
    2. Север, около Серпуховско-Тимирязевской линии метро / North of the city, around Serpukhovsko-Timiryazevskaya metro line;
   
    3. Северо-запад, около Замоскворецкой линиии метро / North-West, around Zamoskvoretskaya metro line;
    
    4. Северо-запад, около Таганско-Краснопресненской линиии метро / North-West, around Tagansko-Krasnopresnenskaya metro line;
    
    5. Юго-восток, около Люблинской линиии метро / South-East, around Lyublinskaya metro line;
    
    6. Юго-восток, около Таганско-Краснопресненской линиии метро / South-East, around Tagansko-Krasnopresnenskaya metro line;
    
    7. Восток, около Калининской линиии метро / East, around Kalininskaya metro line;
    
    8. Восток, около Арбатско-Покровской линиии метро / East, around Arbatsko-Pokrovskaya metro line.

## Очистка данных

Была проведена очистка от полных дубликатов данных и аномалий.

Для вычисления аномалий были использованы графики scatterplot и histplot

## Построение моделей

Было два этапа построения моделей:

    1. Без гиперпараметров
    
    2. С подбором гиперпараметров
    
Использовались модели Ridge, KNeighborsRegressor, RandomForestRegressor

Использовалась оценка R^2

По результатам моделей лучше всего отработала модель  RandomForestRegressor, её предсказательная способность оказалась равной 0.78
