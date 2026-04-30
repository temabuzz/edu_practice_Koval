# 1. zero.sh
Код:
```
#!/bin/bash

group="321"
name="Артем"
surname="Коваль"
stipendia=778
usd_rate=75
usd_sum=$((stipendia / usd_rate))

echo "Я учусь в $group, зовут меня $name $surname. В этом месяце мне пришла стипендия размером в $stipendia рублей, это $usd_sum $."
```
Делаем файл исполняемым и запускаем:

<img width="970" height="59" alt="изображение" src="https://github.com/user-attachments/assets/c368d1f5-3e82-4d75-a220-906c8c6430a3" />

*Рис.1 Вывод zero.sh*

# 2. start.sh
Код:
```
#!/bin/bash

echo "Привет, $1!"
```
Делаем файл исполняемым и запускаем:

<img width="302" height="57" alt="изображение" src="https://github.com/user-attachments/assets/5de109dc-d56b-4579-a850-34633b29ac36" />

*Рис.2 Вывод start.sh*

# 3. start_2.sh
Код:
```
#!/bin/bash

if [ -n "$1" ]; then
    echo "Привет, $1!"
else
    echo "Имя не передано."
fi
```
Делаем файл исполняемым и запускаем:

<img width="319" height="78" alt="изображение" src="https://github.com/user-attachments/assets/cc3f9bea-e9ce-4812-8c4a-25c16fcbed37" />

*Рис.3 Вывод start_2.sh*

# 4. file.sh
Код:
```
#!/bin/bash

if [ -e "$1" ]; then
    echo "Файл '$1' существует."
else
    echo "Файл '$1' не найден."
fi
```
Делаем файл исполняемым и запускаем:

<img width="345" height="96" alt="изображение" src="https://github.com/user-attachments/assets/a9878f43-e6ef-4a62-8bf0-f2f88bf49cfb" />

*Рис.4 Вывод file.sh*

# 5. my_dir.sh
Код:
```
#!/bin/bash

if [ -d "$1" ]; then
    ls "$1"
else
    echo "Директория '$1' не найдена."
fi
```
Делаем файл исполняемым и запускаем:

<img width="316" height="96" alt="изображение" src="https://github.com/user-attachments/assets/adf55fea-dc1b-4c19-81b3-47ab17496e19" />

*Рис.5 Вывод my_dir.sh*

# 6. dir_m.sh
Код: 
```
#!/bin/bash

if [ -d "$1" ]; then
    echo "Директория '$1' уже существует."
else
    mkdir "$1"
    echo "Директория '$1' создана."
fi
```
Делаем файл исполняемым и запускаем:

<img width="307" height="95" alt="изображение" src="https://github.com/user-attachments/assets/4f0cc252-d8f7-4b8c-bfaf-f1c77c202a46" />

*Рис.6 Вывод dir_m.sh*

# 7. user_light.sh
```
#!/bin/bash

my_user=$(whoami)
if grep -q "^$my_user:" /etc/passwd; then
    echo "Поздравляю! Пользователь '$my_user' найден в системе."
fi
```
Делаем файл исполняемым и запускаем:

<img width="458" height="62" alt="изображение" src="https://github.com/user-attachments/assets/1f944709-b889-4415-8dde-ac57b6bf0b21" />

*Рис. 7 Вывод user_light.sh*

# 8. user_f.sh
Код:
```
#!/bin/bash

if grep -q "^$1:" /etc/passwd; then
    echo "Пользователь '$1' найден."
else
    echo "Пользователь '$1' не найден."
fi
```

Делаем файл исполняемым и запускаем:

<img width="311" height="97" alt="изображение" src="https://github.com/user-attachments/assets/750f63fe-8504-41b9-8003-5e3b051e142d" />

*Рис.8 Вывод user_f.sh*

# 9. user_f2.sh
Код:
```
#!/bin/bash

if [ -z "$1" ]; then
    echo "Укажите имя пользователя!"
    exit 1
fi

if grep -q "^$1:" /etc/passwd; then
    echo "Пользователь '$1' найден в системе!"
else
    echo "Пользователь '$1' не найден!"
    filename="don't_be_sad_user_${1}_will_be_there_soon.txt"
    touch "$filename"
    echo "Создан файл: $filename"
fi
```
Делаем файл исполняемым и запускаем:

<img width="538" height="76" alt="изображение" src="https://github.com/user-attachments/assets/81fc0653-3ef4-47da-9105-1610004a8311" />

*Рис.8 Вывод user_f2.sh*

# 10. finder_light.sh
Код:
```
#!/bin/bash

if [ -f "$1" ]; then
    echo "'$1' — обычный файл."
elif [ -d "$1" ]; then
    echo "'$1' — директория."
elif [ -L "$1" ]; then
    echo "'$1' — символическая ссылка."
else
    echo "'$1' — не существует или другой тип."
fi
```
Делаем файл исполняемым и запускаем:

<img width="416" height="134" alt="изображение" src="https://github.com/user-attachments/assets/8fa37e52-bd5f-4d90-aa1d-508727df9a2f" />

*Рис.10 Вывод finder_light.sh*

# 11. math.sh
Код:
```
#!/bin/bash

a=$1
b=$2

echo "Сумма: $((a + b))"
echo "Разность: $((a - b))"
echo "Произведение: $((a * b))"
```
Делаем файл исполняемым и запускаем:

<img width="290" height="96" alt="изображение" src="https://github.com/user-attachments/assets/631ab7b8-d9e9-4c81-877d-884274db24b4" />

*Рис.11 Вывод math.sh*

# 12. sort.sh
Код:
```
#!/bin/bash

for arg in "$@"; do
    echo "$arg"
done
```
Делаем файл исполняемым и запускаем:

<img width="326" height="114" alt="изображение" src="https://github.com/user-attachments/assets/15625fb7-c5dc-4b17-a104-72f8d88045d6" />

*Рис.12 Вывод sort.sh*

# 13. io.sh
Код:
```
#!/bin/bash

case "$1" in
    start) echo "Starting..." ;;
    stop)  echo "Stopping..." ;;
    *)     echo "Используй: $0 {start|stop}" ;;
esac
```
Делаем файл исполняемым и запускаем:

<img width="298" height="139" alt="изображение" src="https://github.com/user-attachments/assets/61f2a4cd-32f5-4ce8-9a85-f250b43ce558" />

*Рис.13 Вывод io.sh*

# 14. user_use.sh
Код:
```
#!/bin/bash

du -sk /home/* 2>/dev/null | sort -nr | while read size dir; do
    user=$(basename "$dir")
    echo "$user — $size КБ"
done
```
Делаем файл исполняемым и запускаем:

<img width="347" height="77" alt="изображение" src="https://github.com/user-attachments/assets/68369d92-9e0d-45de-b8dc-b773f666530f" />

*Рис. 14 Вывод user_use.sh*

# 15. sort_du.sh
Код:
```
#!/bin/bash

dir="${1:-.}"
find "$dir" -type f -printf '%T@ %p\n' 2>/dev/null | sort -n | head -3 | while read timestamp path; do
    date=$(date -d "@$timestamp" "+%Y-%m-%d %H:%M:%S")
    echo "$path — $date"
done
```
Делаем файл исполняемым и запускаем:

<img width="346" height="78" alt="изображение" src="https://github.com/user-attachments/assets/cd6b4f72-76bd-47c0-a359-a9352d86129d" />

*Рис.15 Вывод sort_du.sh*

# 16. dir_info.sh
Код:
```
#!/bin/bash

dir="${1:-.}"
size=$(du -sk "$dir" | awk '{print $1}')
echo "Общий размер: $size КВ"
```
Делаем файл исполняемым и запускаем:

<img width="339" height="57" alt="изображение" src="https://github.com/user-attachments/assets/cdf35a4b-6d86-47d1-8f64-9e6a5eec3053" />

*Рис.16 Вывод dir_info.sh*

# 17. bash_history.sh
Код::
```
#!/bin/bash

hist_file="$HOME/.bash_history"
if [ -f "$hist_file" ]; then
    awk '{print $1}' "$hist_file" | sort | uniq -c | sort -nr | head -5
else
    echo "Файл .bash_history не найден."
fi
```
Делаем файл исполняемым и запускаем:

<img width="368" height="138" alt="изображение" src="https://github.com/user-attachments/assets/78ac6b38-5f26-4897-b18a-b4b33874642c" />

*Рис. 17 Вывод bash_history.sh*

















