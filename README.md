# StockGuard — práctica de GitHub Actions

Repositorio de práctica de la guía *Introducción práctica a GitHub Actions* (Línea de Profundización I – Big Data).
Clasifica el riesgo de inventario de un producto según el stock actual y el stock mínimo:

| Condición | Resultado |
|---|---|
| stock actual = 0 | `AGOTADO` |
| stock actual ≤ 50 % del mínimo | `CRITICO` |
| stock actual ≤ mínimo | `BAJO` |
| otro caso | `NORMAL` |
| stock negativo o mínimo ≤ 0 | `ValueError` |

```bash
python -m pip install -r requirements.txt
pytest -v
```

## Regla adicional: sobrestock
`detectar_sobrestock(stock_actual, stock_maximo)` devuelve `True` cuando hay más unidades que la capacidad máxima
(`stock_actual > stock_maximo`). En el límite exacto no hay sobrestock; valores negativos o un máximo ≤ 0 son inválidos.
