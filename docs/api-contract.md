# API Контракт

## Таблица запросов
| Метод и путь | Тело | Успех | Возможная ошибка |
| :--- | :--- | :--- | :--- |
| GET /api/slots | — | 200, массив или [] | — |
| GET /api/slots/{id} | — | 200, объект | 404 |
| POST /api/slots | dateTime, disciplineId, teacherId | 201, id, number, status: New | 400 |
| PATCH /api/slots/{id}/student | studentId | 200 | 404, 409 |
| PATCH /api/slots/{id}/status | status | 200 | 404, 409 |

## Пример тела создания (POST /api/slots)
```json
{
  "dateTime": "2026-09-20T14:00:00",
  "disciplineId": 3,
  "teacherId": 10
}