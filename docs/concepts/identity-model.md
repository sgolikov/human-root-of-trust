# Identity Model

> Данный документ является концепцией проекта Human Root of Trust.
>
> Документ не описывает реализацию и не является инструкцией по внедрению.

## 1. Назначение

Описать концепцию Identity Model в рамках проекта Human Root of Trust.

## 2. Проблема

TODO

## 3. Определение

Identity — это логический контур деятельности, обладающий собственными целями, доступами, артефактами и жизненным
циклом.

## 4. Что Identity не является

- человеком;
- аккаунтом;
- почтой;
- устройством;
- аппаратным ключом;
- vault;
- ролью в конкретной системе.

## 5. Identity Model

```text
ID-C01 Personal
ID-C02 Work
ID-C03 Admin
ID-C04 Public
```

Это пример модели MVP 1.0.

Проект не требует фиксированного набора Identity.

## 6. Identity Lifecycle

```text
Create
Use
Review
Retire
```

## 7. Зависимости

Для понимания механизмов восстановления и управления контролем см.:

- [root-capability](./root-capability.md)

## 8. Acceptance Criteria

- Identity имеет уникальный код;
- Identity имеет понятную цель;
- Identity может быть отделена от других Identity;
- компрометация одной Identity не должна автоматически компрометировать остальные;
- Identity может быть восстановлена через ROOT Capability.

## 9. Non-goals

- конкретные аккаунты;
- конкретные сервисы;
- структура vault;
- структура recovery;
- IAM implementation;
- OPSEC implementation.

## 10. Связанные документы

## 10. Связанные документы

- [root-capability](./root-capability.md)
- [vault-model](./vault-model.md)
- [location-model](./location-model.md)
