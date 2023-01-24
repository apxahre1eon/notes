# notes
Ошибка 1cv8 libstdc++.so.6: version `GLIBCXX_3.4.29' not found. Сначала проверяем что есть в системе 
strings /usr/lib/x86_64-linux-gnu/libstdc++.so.6 | grep GLIBCXX

Затем текущую версию переименовываем\удаляем
mv /opt/1cv8/x86_64/$version/libstdc++.so.6 /opt/1cv8/x86_64/${version}/libstdc++.so.6.back
Линкуем
ln -s /usr/lib/x86_64-linux-gnu/libstdc++.so.6 /opt/1cv8/x86_64/{version}/libstdc++.so.6
