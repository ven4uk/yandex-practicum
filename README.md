# Yandex Practicum

Репозиторий для отчета по практической работе

## Чему начился?

- Работать с базовыми командами в терминале
- Создавать локальный репозиторий
- Вести локальный проект
- Создавать удаленный репозиторий
- Синхронизировать локальный репозиторий

## Пример практики

Создание репозитория проходит через несколько команд  

```bash
mkdir reponame && cd reponame && git init
```

Подключение к удаленному репозиторию  

```bash
git remote add origin URL_TO_SSH_GITHUB
```


## Расширение горизонтов

### Коммиты

Чтобы ориентироваться по изменениям в репозитории использутся коммиты. Они же в свою очередь имеют идентификатор на базе хэш функции.

По этим коммитам можно посмотреть лог репозитория и понять какие проводились изменения, но необходимо писать информативные комментарии к коммитам.

### Статусы файлов

Через команду 

```bash
git status
```

Можно ознакомиться с текущим состоянием репозитория.

Файлы могут принимать такие статусы как:

- untracked;
- tracked;
- staged;
- modified.

Их переходы можно описать схемой.

```mermaid
flowchart LR;
    A(file create) -- "touch fileA.txt" --> B(untracked);
    B(untracked) -- "git add ." --> C(staged);
    C(staged) -- "git commit -m ..." --> D(tracked/comitted);
    C(staged) -- "edit file" --> E(modified) -- "git add ." --> C(staged);
```

