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


---
## Вывод
