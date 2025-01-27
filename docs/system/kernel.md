# Ядро

С образом ALT Regular Gnome (с версии `20231122`) поставляется две версии ядра `un-def` и `std-def`

- std-def — стабильное ядро с longterm (LTS) поддержкой
- un-def — стабильное ядро с Interim Releases (IR) поддержкой

## Обновление ядер

Обновить текущие ядро можно через терминал:

```shell
su -
update-kernel
```

После успешного обновления ядра и модулей перезгрузите операционную систему.

:::info
update-kernel обновляет в том числе и модули ядра. Утилита выведит список обновляемых модулей, необходимо подтвердить операцию в терминале набрав Y
:::

Обновить выбранную ветку ядра в системе через интерфейс ЦУС:

- Открыть ЦУС и ввести пароль администратора
- Перейти в раздел «Обновить ядро»
- Нажать кнопку «Обновить ядро»

![Kernel](/kernel/kernel-1.png)

После успешного обновления ядра и модулей перезгрузите операционную систему.

## Переключить ветку ядра

Если ветка ядра не установлено в системе, то переключить его можно только через терминал:

```shell
su -
update-kernel -t std-def
```

Если ветка установлена (с версии `20231122`), то изменить ветку по умолчанию можно через ЦУС:

- Открыть ЦУС и ввести пароль администратора
- Перейти в раздел «Обновить ядро»
- Выбрать ядро в списке «Установленные ядра»
- Нажать кнопку «Сделать ядро загружаемым по умолчанию»

![Alt text](/kernel/kernel-2.png)

## Удаление старых версий ядра:

```shell
su -
remove-old-kernels
```