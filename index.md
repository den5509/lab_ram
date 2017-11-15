# Проектирование облачной файловой системы
## Построение общего хранилища для контейнеров

Сначала был создан том AllVolume при помощи команды:
```bash
docker volume create --name AllVolume
```
Потом был создан и запущен первый контейнер 1, с примонтированным к нему томом AllVolume.
Использованная команда:
```bash
docker run -ti --name=Container1 -v AllVolume:/allvolume alpine
```
В томе AllVolume был создан файл, содержащий строку с идентификатором контейнера.
Примененная команда:
```bash
echo "write test from " + $HOSTNAME > /allvolume/file.txt
```
![alt-текст](https://github.com/den5509/lab_ram/blob/master/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202017-11-15%2010-06-13.png)

---
## Вывод
