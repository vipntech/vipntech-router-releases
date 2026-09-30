# VipnTech Router Releases

Публичные установочные файлы VipnTech для роутеров с уже установленным
OpenWrt. Репозиторий не содержит персональные Subscription URL, device tokens,
пароли или VLESS-конфигурации.

[Открыть список установочных релизов](https://github.com/vipntech/vipntech-router-releases/releases)

## Windows

1. Откройте последний release и скачайте `vipntech-router-windows-pilot.7.zip`.
2. Полностью распакуйте ZIP.
3. Дважды щёлкните `START-VIPNTECH.cmd` и следуйте подсказкам.
4. Если программа изменила LAN-адрес, переподключитесь к Wi-Fi или кабелю и
   снова запустите `START-VIPNTECH.cmd`.

`CHECK-ROUTER.cmd` выполняет необязательную безопасную проверку без изменений.
Вводить команды PowerShell или Command Prompt не требуется. Launcher спросит
текущий IP роутера и желаемый IP после настройки. Если LAN менять не нужно,
второй вопрос можно оставить пустым.

Установщик не записывает firmware, разделы или bootloader и не проверяет
модель роутера. Требуется OpenWrt 24.10 или новее. Все скачиваемые артефакты
проверяются по SHA256 из `release.json`.
