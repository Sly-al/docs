# Устранение ошибки ERR.DS_API.FORMULA.VALIDATION.AGG.INCONSISTENT - Inconsistent aggregation among operands


## Описание проблемы {#issue-description}

При валидации формулы возникает ошибка:
```
ERR.DS_API.FORMULA.VALIDATION.AGG.INCONSISTENT - Inconsistent aggregation among operands
```

## Решение {#issue-resolution}

Такая ошибка возникает, когда аргументами одной и той же функции (или операндами одного оператора) являются одновременно агрегированное и неагрегированное выражения. 

{{ datalens-full-name }} не позволяет использовать в одном выражении агрегированные и неагрегированные значения – не получится использовать в одном выражении показатели (отображаются в датасете и в визарде синим цветом) и измерения (отображаются в датасете и в визарде зеленым цветом).

Подробнее пишем в [документации](../../../datalens/troubleshooting/errors/ERR-DS_API-FORMULA-VALIDATION-AGG-INCONSISTENT)

{% note info %}

При валидации данных и формул в датасете сервис может проверять большой объём данных, поэтому мы рекомендуем дополнительно отслеживать консистентность ваших данных и формул.

{% endnote %}
