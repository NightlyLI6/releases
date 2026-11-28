# Руководство по установке

> [!WARNING]
> Все ваши данные будут удалены. **Перед прошивкой создайте резервную копию данных.**

## Требования

- Разблокированный загрузчик
- ПК

## Прошивка

1. Прошейте [эту версию](https://github.com/NightlyLI6/releases/releases/tag/fox_r12.0_1_knukima) OrangeFox:
   ```sh
   fastboot flash vendor_boot --slot=all recovery.img
   fastboot reboot recovery
   ```
2. Выберите **Меню → ADB и Sideload**.

    **ОБЯЗАТЕЛЬНО установите флажок "Reflash OrangeFox after flashing a ROM" (Переустановить OrangeFox после прошивки ROM). В противном случае система не сможет загрузиться. Если вы забыли установить этот флажок, прошейте recovery заново в оба слота, затем переключитесь на слот, в который была установлена прошивка.**

3. Установите ZIP-файл через Sideload:
   ```sh
   adb sideload <filename.zip>
   ```
4. Format data через Yes
5. Если вы хотите установить дополнительные пакеты (GApps, ядро), сначала перезагрузитесь в recovery, чтобы сменить слот!
6. Готово.
