# Исследование продаж Ozon — бренд Aura

1. Выручка по категориям товара

```sql
SELECT category
    , round(sum(order_amount)::numeric, 2) as total_sum
    , round((sum(item_cnt)::numeric), 0) as total_cnt
FROM DATA
WHERE status = 'Доставлен'
GROUP BY category
ORDER BY total_sum desc
```

| category | total_sum | total_cnt |
| :--- | :--- | :--- |
| Ручки раздельные | 2757600.00 | 1128 |
| Завертки/накладки | 1714880.00 | 1291 |
| Кнобы (ручка+защелка) | 925328.00 | 1424 |
| Петли | 661279.00 | 818 |
| Ограничители | 454992.00 | 582 |
| Механизмы+цилиндры | 364147.00 | 441 |
| Раздвижные системы | 5278.00 | 5 |
