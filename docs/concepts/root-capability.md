# ROOT Capability

> Данный документ является концепцией проекта Human Root of Trust.
>
> Документ не описывает реализацию и не является инструкцией по внедрению.

## 1. Назначение

Описать концепцию ROOT Capability в рамках проекта Human Root of Trust.

## 2. Проблема

При проектировании систем идентичности часто предполагается существование единого корневого объекта управления:

- root account;
- master password;
- hardware key;
- recovery email.

В современных цифровых экосистемах такой единый объект обычно отсутствует.

Контроль над системой определяется не одним артефактом, а способностью выполнять восстановление, ротацию и отзыв
доступа.

Для описания этой способности вводится понятие ROOT Capability.

## 3. Определение

ROOT Capability — это совокупность процедур, артефактов и полномочий, позволяющих восстановить контроль над системой.

## 4. Что ROOT не является

ROOT не является:

- аккаунтом;
- пользователем;
- identity;
- почтой;
- аппаратным ключом;
- vault;
- master password.

## 5. Состав ROOT Capability

```text
ROOT Capability
├─ Recovery
├─ Rotation
├─ Revoke
└─ Audit
```

Backup не является отдельной Capability.

Backup — механизм поддержки Recovery.

## 6. Связь с Identity

Identity отвечает на вопрос:

Кто действует?

ROOT отвечает на вопрос:

Как вернуть контроль?

Одна ROOT Capability может обслуживать несколько Identity.

## 7. Human Keys и Machine Identities

Human Keys ≠ Machine Identities

Human Keys:

- интерактивные;
- требуют PIN / Touch;
- используются человеком.

Machine Identities:

- работают без человека;
- используются в CI / cloud / cluster;
- управляются через IAM / KMS / Vault / Service Accounts.

## 8. Acceptance Criteria

- потеря одного устройства не приводит к потере контроля;
- потеря одного аппаратного ключа не приводит к потере контроля;
- компрометация одного слоя не даёт полного контроля;
- recovery-путь документирован;
- revoke-путь документирован;
- rotation-путь документирован;
- recovery не зависит от памяти владельца.

## 9. Non-goals

Документ не описывает:

- конкретные сервисы;
- конкретные инструменты;
- vault implementation;
- IAM implementation;
- KMS implementation;
- recovery automation;
- юридические процедуры;
- хранение секретов.

## 10. Связанные документы

- identity-model.md
- vault-model.md
- location-model.md
