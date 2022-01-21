# Leesson6-jdbc
CREATE TABLE country(
                      id SERIAL PRIMARY KEY NOT NULL ,
                      countryName VARCHAR(30) NOT NULL ,
                      countryArea VARCHAR(30) NOT NULL ,
                      population INT NOT NULL ,
                      countryAge INT NOT NULL

);
INSERT INTO country(countryName, countryArea, population, countryAge)
VALUES ('Kyrgyzstan','199 951 км²  ',6687835,31),
       ('Uzbekistan','448 900 км²  ',34739400,31),
       ('Kazakhstan','2 724 902 км²',19263375,31);

CREATE TABLE city(
                     id SERIAL PRIMARY KEY NOT NULL ,
                     cityName VARCHAR(30) NOT NULL ,
                     cityArea VARCHAR(30) NOT NULL ,
                     population INT NOT NULL ,
                     CountryOfThisCity VARCHAR(30) NOT NULL
);
INSERT INTO city(cityName, cityArea, population,CountryOfThisCity)
VALUES('Bishkek   ','127 км²   ',1088900,'Kyrgyzstan'),
      ('Tashkent  ','357,84 км²',2538400,'Uzbekistan'),
      ('Nur-Sultan','797,33 км²',1002874,'Kazakhstan');

CREATE TABLE mayors(
    id SERIAL PRIMARY KEY NOT NULL ,
    fist_name VARCHAR(30) NOT NULL ,
    last_name VARCHAR(30) NOT NULL ,
    data_birth_day DATE NOT NULL,
    nationality VARCHAR(30) NOT NULL
);
INSERT INTO mayors(fist_name, last_name, data_birth_day, nationality)
VALUES('Айбек    ','Джунушалиев','06-06-1976','Кыргыз'),
      ('Имамназар','Бурканов   ','11-04-1965','Кыргыз'),
      ('Алмаз    ','Мамбетов   ','15-03-1976','Кыргыз');

DROP TABLE country;
DROP TABLE city;
DROP TABLE mayors;
