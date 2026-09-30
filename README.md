# VipnTech Router Releases

Публичные установочные файлы VipnTech для роутеров с уже установленным
OpenWrt. Репозиторий не содержит персональные Subscription URL, device tokens,
пароли или VLESS-конфигурации.

## Windows

1. Откройте последний release и скачайте `vipntech-router-windows-pilot.5.zip`.
2. Распакуйте ZIP и откройте PowerShell в полученной папке.
3. Проверьте release:

```powershell
.\vipntech-router-setup-windows-amd64.exe verify-release `
  --manifest .\release.json
```

4. Выполните read-only проверку роутера:

```powershell
.\vipntech-router-setup-windows-amd64.exe install `
  --manifest .\release.json `
  --router 192.168.1.1 `
  --state-dir "$env:LOCALAPPDATA\VipnTech\routers\home" `
  --dry-run
```

5. Повторите команду без `--dry-run`, чтобы установить ПО. Для явной смены
   LAN-адреса добавьте, например, `--lan-ip 192.168.77.1` и следуйте подсказке
   о переподключении.

Установщик не записывает firmware, разделы или bootloader и не проверяет
модель роутера. Требуется OpenWrt 24.10 или новее. Все скачиваемые артефакты
проверяются по SHA256 из `release.json`.
