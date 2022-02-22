# Практическая работа ADB
Отобразить подключённый девайс в консоли
```
adb devices
```
Получить серийный номер подключенного мобильного телефона
```
adb get-serialno
```
Установить .apk файл приложениия Tourist Pass на телефон с компьютера через ADB
```
adb install D:\Documents\Test\Tourist_Pass.apk
```
Вывести адрес приложения Tourist Pass в системе Android
```
adb shell pm list packages | findstr TouristPass
```
Сделать скриншот запущенного приложения Tourist Pass и сразу скопировать на компьютер в одной команде
```
adb shell screencap /storage/emulated/0/DCIM/Screenshots/tourist.png && adb pull screencap /storage/emulated/0/DCIM/ Screenshots/tourist.png D:\Documents\Test
```
Вывести в консоль логи приложения Tourist Pass;
```
adb logcat | findstr -rnw "TouristPass"
```
Скопировать логи приложения Tourist Pass на компьютер;
```
adb logcat | findstr -rnw "TouristPass" > D:\Documents\Test\TouristPass.log	
```
Удалить приложение Tourist Pass с телефона через ADB.
```
adb uninstall com.android.TouristPass
```
