# B-scan Viewer / Просмотрщик B-сканов
*RU 

*Назначение программы*
 — настольное приложение на Qt для визуализации *B-scan* данных (2D-изображение), полученных из бинарного файла.  

Приложение позволяет:
- загрузить файл с данными (*.bin*, *.binary*);
- выбрать индекс *TX (0–63)* с помощью слайдера;
- просмотреть соответствующую B-scan-картинку (оси: *RX* по ширине, *Sample* по высоте).

*Что происходит с данными*
- Из файла читаются две части сигналов размерности 64 x 64 x 8192.
- Для каждой точки считается модуль комплексного сигнала:
res = sqrt(part0^2 + part1^2)
- Далее результат нормализуется по глобальным *min/max* и окрашивается по градиенту (от синего к красному).

*Стек технологий*
- *C++17*
- *Qt 5.15* (модули: *core*, *gui*, *widgets*)
- Qt Designer (*.ui*)
- Ресурсы Qt (*.qrc*) — иконки/картинки

*Просмотр исходного кода*
1. Откройте *Qt Creator*.
2. Откройте проект.
3. В исходной папке выберите папку *Code*.
4. Откройте файл проекта *Program.pro*.
   
*Инструкция по запуску приложения*
1. В исходной папке зайдите в папку *Release*.
2. Затем откройте *release*.
3. Запустите *Program.exe*.

---
*EN 

*Program* is a Qt desktop application for visualizing *B-scan* data as a 2D image loaded from a binary file.  

The application allows you to:
- load a data file (*.bin*, *.binary*);
- select a *TX index (0–63)* using a slider;
- view the corresponding B-scan image (axes: *RX* as image width, *Sample* as image height).

*Data processing summary*
- The file contains two signal parts with dimensions 64 x 64 x 8192.
- For each point, the magnitude is computed:
res = sqrt(part0^2 + part1^2)
- The result is normalized using global *min/max* values and mapped to a color gradient (blue → red).

*Technology stack*
- *C++17*
- *Qt 5.15* (modules: *core*, *gui*, *widgets*)
- Qt Designer (*.ui*)
- Qt Resource System (*.qrc*) — icons/images

*Viewing the source code*
1. Open *Qt Creator*.
2. Open the project.
3. In the source directory, select the *Code* folder.
4. Open *\Program.pro\*.

*How to run the application*
1. In the source directory, open the *Release* folder.
2. Then open *release*.
3. Run *Program.exe*.
