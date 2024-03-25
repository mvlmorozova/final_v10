# Требования

* Нельзя менять уже написанный код, тесты и другие файлы добавленные в проект
* Помимо стандартной библиотеки, вы можете использовать все что импортировано. Что не импортировано, то не используется.
* Выполняйте коммиты и пуши как можно чаще. Так вы будете видеть какие из тестов сработают, а какие нет.
* Во время работы не забывайте запускать саму утилиту и npm test

# Задание

Ваша задача написать консольную утилиту, которая анализирует переданный файл с информацией о машинах и выводит на экран некоторую статистику по данным из файла. Файлы хранятся в директории *\_\_fixtures\_\_* в формате CSV. Они используются для тестов и понадобятся вам, для запуска и проверки утилиты в терминале.

Пример запуска утилиты:

```bash
bin/cars.js __fixtures__/cars1.csv
Count: 20
Brands: Audi, BMW, Cadillac, Chevrolet, Ford
Cars price: Min price: 17999, Max price: 91999
Max sales: 7000
Outsider: Kia Forte
```

Вывод содержит фиксированный набор строк (Count, Models, ...), каждая из которых соответствует какой-то агрегированной информации по данным из файла. Например, первая строка содержит количество записей в переданном файле. Значения в этих строках зависят от данных внутри переданного файла. В примере выше число 20, в вашем случае может быть другое, зависит от того, с каким файлом ведется работа.

Каждая строчка в выводе утилиты, представляет собой небольшое отдельное вычислительное задание. Вам предстоит решать эти задачи по очереди. Ниже список этих заданий:

## 1 шаг

Выведите количество записей с данными в переданном файле. Учтите, что первая строчка в CVS файле является заголовочной, она не содержит данных и не должна учитываться. Вывод утилиты будет таким:

```bash
bin/cars.js __fixtures__/cars1.csv
Count: 20
```

## 2 шаг

Выведите список автомобильных брендов, для которых есть информация о продажах в переданном файле. Бренды в этом списке отсортированы в алфавитном порядке.

```bash
bin/cars.js __fixtures__/cars1.csv
Count: 20 # Не забывайте что предыдущее решение остается работать
Brands: Audi, BMW, Cadillac, Chevrolet, Ford
```

## 3 шаг

Выведите самое большое количество продаж по Европе.

```bash
bin/cars.js __fixtures__/cars1.csv
Count: 20
Brands: Audi, BMW, Cadillac, Chevrolet, Ford
Cars price: Min price: 17999, Max price: 91999
Max Europe sale: 7000
```

## 4 шаг

Выведите модель, минимально дешевого и максимально дорогого автомобиля, которая встречается в данных переданного файла. В данном случае речь идет о цене.

```bash
bin/cars.js __fixtures__/cars1.csv
Count: 20
Brands: Audi, BMW, Cadillac, Chevrolet, Ford
Cars price: Min price: 17999, Max price: 91999
```

## 5 шаг

Выведите бренд и модель самого непроданного автомобиля основываясь на средних продажах этого автомобиля по миру

С технической точки зрения, вам нужно посчитать средние продажи по всем регионам. Затем нужно определить какая модель принесла меньше всего прибыли.

```bash
bin/cars.js __fixtures__/cars1.csv
Count: 20
Brands: Audi, BMW, Cadillac, Chevrolet, Ford
Cars price: Min price: 17999, Max price: 91999
Max Europe sale: 7000
Outsider: Kia Forte
```

# Список доступных сайтов

- [Javascript](https://developer.mozilla.org/ru/docs/Learn/JavaScript)
- [Web development](https://developer.mozilla.org/en-US/docs/Learn)
- [Node](https://nodejs.org/ru/docs)
- [Hexlet](https://hexlet.io)
- [NPM](https://docs.npmjs.com/)
- [lodash](https://lodash.com/docs)
- [Github](https://github.com/)
- [Github Classrom](https://classroom.github.com/)
- [Github Docs](https://docs.github.com/ru)
- [ESLint](https://eslint.org/docs/latest/)
