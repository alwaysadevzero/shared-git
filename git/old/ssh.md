## Создание SSH-ключа

Откройте терминал (в ОС Windows откройте Git Bash) и введите:

ssh-keygen -t ed25519 -C "your_email@example.com"

где _**[your_email@example.com](mailto:your_email@example.com)**_ - ваш e-mail. В терминале Git Bash используется комбинация `Shift + Ins` вместо `Ctrl + V` для вставки текста из буфера обмена.

Далее будут заданы вопросы (где будут располагаться ключи, пароль, подтверждение пароля) для ответа на которые рекомендую просто нажать `Enter`:

[![SSH for Win](https://github.com/TUstiugov/ssh-hints-for-win/raw/main/img/01.png "SSH-key for Windows")](https://github.com/TUstiugov/ssh-hints-for-win/blob/main/img/01.png)

После этого, для запуска ssh-агента, введите в терминале:

eval "$(ssh-agent -s)"

[![SSH for Win](https://github.com/TUstiugov/ssh-hints-for-win/raw/main/img/02.png "SSH-key for Windows")](https://github.com/TUstiugov/ssh-hints-for-win/blob/main/img/02.png)

И последний шаг, введите в терминале:

ssh-add ~/.ssh/id_ed25519

[![SSH for Win](https://github.com/TUstiugov/ssh-hints-for-win/raw/main/img/03.png "SSH-key for Windows")](https://github.com/TUstiugov/ssh-hints-for-win/blob/main/img/03.png)

## [](https://github.com/TUstiugov/ssh-hints-for-win/blob/main/ssh-hints-for-win.md#%D0%B4%D0%BE%D0%B1%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BA%D0%BB%D1%8E%D1%87%D0%B0-%D0%B2-github)Добавление ключа в GitHub.

Перейдите в папку `C:\Users\"NickName"\.ssh`, где _**NickName**_ - ваш аккаунт Windows. Откройте в любом текстовом редакторе (блокнот) файл `id_ed25519.pub`. Начинаться он должен примерно так: `ssh-ed25519` . Скопируйте в буфер обмена все его содержимое (Ctrl+A -> Ctrl+C).

Откройте GitHub и откройте `Settings`:

[![SSH for Win](https://github.com/TUstiugov/ssh-hints-for-win/raw/main/img/04.png "SSH-key for Windows")](https://github.com/TUstiugov/ssh-hints-for-win/blob/main/img/04.png)

Потом перейдите в раздел `SSH and GPG keys`:

[![SSH for Win](https://github.com/TUstiugov/ssh-hints-for-win/raw/main/img/05.png "SSH-key for Windows")](https://github.com/TUstiugov/ssh-hints-for-win/blob/main/img/05.png)

Нажмите на кнопку `New SSH key`:

[![SSH for Win](https://github.com/TUstiugov/ssh-hints-for-win/raw/main/img/06.png "SSH-key for Windows")](https://github.com/TUstiugov/ssh-hints-for-win/blob/main/img/06.png)

В поле `Title` введите любое название для ключа, а в поле `Key` вставьте ключь (Ctrl+V) который вы скопировали из файла `id_ed25519.pub`. Нажмите на кнопку `Add SSH key`.

[![SSH for Win](https://github.com/TUstiugov/ssh-hints-for-win/raw/main/img/07.png "SSH-key for Windows")](https://github.com/TUstiugov/ssh-hints-for-win/blob/main/img/07.png)

На вашу почту должно прийти письмо с подтверждением добавления ключа.

При первом обращении к GitHub в терминале у вас спросят хотите ли продолжить, введите `yes` и нажмите `enter`:

[![SSH for Win](https://github.com/TUstiugov/ssh-hints-for-win/raw/main/img/08.png "SSH-key for Windows")](https://github.com/TUstiugov/ssh-hints-for-win/blob/main/img/08.png)