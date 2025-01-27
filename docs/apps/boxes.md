---
title: Boxes
appstreamRepo: org.gnome.Boxes
appstreamFlatpak: org.gnome.Boxes
metainfo:
    active: true
    thumb:
        src: /boxes/org.gnome.Boxes.png
        title: Boxes
    summary: Виртуализация стала проще
    developer: 
        name: The GNOME Project
    site:
        url: https://gnomeboxes.org/
        anchor: gnomeboxes.org
    licence:
        url: https://www.gnu.org/licenses/old-licenses/lgpl-2.1.ru.html#SEC1
        anchor: LGPL-2.1
    translate:
        url: 
        anchor: hosted.weblate.org
    issue: 
        url: https://gitlab.gnome.org/GNOME/gnome-boxes/issues
        anchor: gitlab.gnome.org
    flathub:
        url: https://flathub.org/apps/org.gnome.Boxes
    sisyphus:
        url: https://packages.altlinux.org/ru/sisyphus/srpms/gnome-boxes/
---

# Boxes

Boxes — официальная утилита для рабочего стола GNOME, которая позволяет вам создавать виртуальные машины из образов операционной системы несколькими щелчками мыши.

## Установка из репозитория

**Boxes** можно установить любым привычным и удобным способом:

<!--@include: ./parts/install/software-repo.md-->


**Установка через терминал**

::: code-group

```shell[apt-get]
su -
apt-get update
apt-get install gnome-boxes
```         
```shell[epm]
epm -i gnome-boxes
```
:::


## Установка c помощью Flatpak

При наличии пакета [Flatpak](/flatpak), можно установить **Boxes** одной командой:

```shell
flatpak install flathub org.gnome.Boxes
```

<!--@include: ./parts/install/software-flatpak.md-->

## Подготовка к использованию Boxes

Для запуска необходим установить и запустить набор виртуализации:

::: code-group

```shell[apt-get]
su -
apt-get update
apt-get install libvirt libvirt-kvm
```
```shell[epm]
epm -i libvirt libvirt-kvm
```

:::

```shell
su -
gpasswd -a USER vmusers
systemctl enable libvirtd
systemctl start libvirtd
```

`USER` — имя вашего пользователя.

## 3D-ускрорение

Boxes предоставляет возможность включать или отключать 3D-ускорение для ваших виртуальных машин, если оно поддерживается как гостевой, так и хостинговой системой. Настройка позволить вам повысить производительность повседневных приложений (включить анамацию рабочего окружения) и игр, требующих графической обработки.

1. Выберите бокс, и нажмите правой кнопкой мышки, в открывшемся контекстном меню веберите пункт параметры.
2. Если бокс поддерживает 3D-ускорение, в настройках появится переключатель 3D ускорение. По умолчанию он отключен. Чтобы включить 3D-ускорение, просто переключите переключатель рядом с ним в положение включить.

:::info
Когда вы включаете 3D-ускорение для виртуальной машины, которая уже запущена, изменения вступают в силу после перезапуска бокса.
:::

## Комбинация клавиш

### Обзор 

| Комбинация клавиш |      Описание      | 
| ----------------- | ------------------ |
| [[F1]] | Справка |
| [[F10]] | Открыть главною меню |
| [[Ctrl]] + [[N]] | Создать новую виртуальную машину |
| [[Ctrl]] + [[F]] | Поиск |
| [[Ctrl]] + [[?]] | Комбинации клавиш |
| [[Ctrl]] + [[Q]] | Закрыть окно / Закрыть приложение |

### Создание виртуальной машины и настройка параметров

| Комбинация клавиш |      Описание      | 
| ----------------- | ------------------ |
| [[Alt]] + [[→]] | Перейти к следующей странице |
| [[Alt]] + [[←]] | Перейти к предыдущей странице |

### Отображение виртуальной машины

| Комбинация клавиш |      Описание      | 
| ----------------- | ------------------ |
| [[CtrlL]] + [[AltL]] | Перейти к следующей странице |
| [[Alt]] + [[←]] | Вернуться к обзору |
| [[Ctrl]] + [[Q]] | Закрыть окно / Закрыть приложение |
| [[F11]] | Войти / Выйти из полноэкранного режима |