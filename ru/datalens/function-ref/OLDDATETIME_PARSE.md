---
editable: false
sourcePath: ru/_api-ref/datalens/function-ref/OLDDATETIME_PARSE.md
---

# OLDDATETIME_PARSE



#### Синтаксис {#syntax}


```
OLDDATETIME_PARSE( value )
```

#### Описание {#description}
Переводит выражение `value` в устаревший формат даты и времени. В отличие от [OLDDATETIME](OLDDATETIME.md), поддерживает множество форматов.

**Типы аргументов:**
- `value` — `Строка`


**Возвращаемый тип**: `Дата и время (устаревший)`

#### Примеры {#examples}

```
OLDDATETIME_PARSE("2019-01-02 03:04:05") = #2019-01-02 03:04:05#
```

```
OLDDATETIME_PARSE("20190102030405") = #2019-01-02 03:04:05#
```

```
OLDDATETIME_PARSE("20190102 030405") = #2019-01-02 03:04:05#
```

```
OLDDATETIME_PARSE("2019.01.02 03:04:05") = #2019-01-02 03:04:05#
```

```
OLDDATETIME_PARSE("02/01/2019 03:04:05") = #2019-01-02 03:04:05#
```

```
OLDDATETIME_PARSE("2019-01-02 03:04") = #2019-01-02 03:04:00#
```

```
OLDDATETIME_PARSE("2019-01-02 030405") = #2019-01-02 03:04:05#
```

```
OLDDATETIME_PARSE("2019 Jan 02 03:04:05") = #2019-01-02 03:04:05#
```


#### Поддержка источников данных {#data-source-support}

`Материализованный датасет`, `ClickHouse 19.13`.
