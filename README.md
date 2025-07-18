ИНСТРУКЦИЯ ПО СБОРКЕ И ЗАПУСКУ ПРОГРАММЫ
=======================================

Требования:
- Visual Studio 2022 с поддержкой C++/CLI
- .NET Framework 4.8 или выше
- Windows 10/11

Инструкция по сборке:
1. Откройте Visual Studio 2022
2. Создайте новый проект: File -> New -> Project
3. Выберите "CLR Empty Project (.NET Framework)" в разделе Visual C++
4. Назовите проект "FeatureSelectionApp"
5. Скопируйте файлы main.cpp и MainForm.h в папку проекта
6. Добавьте файлы в проект через Solution Explorer
7. В свойствах проекта установите:
   - Configuration Properties -> General -> CLR Support: Common Language Runtime Support (/clr)
   - Configuration Properties -> General -> Target Framework Version: v4.8
   - Configuration Properties -> Linker -> System -> SubSystem: Windows
   - Configuration Properties -> Linker -> Advanced -> Entry Point: main
8. Добавьте ссылки на System.Windows.Forms и System.Drawing
9. Соберите проект (Build -> Build Solution)

Функциональность программы:
- Загрузка CSV файлов с данными
- Отображение данных в таблице
- Выбор столбцов для анализа
- Настройка параметров алгоритма
- Выполнение алгоритма отбора признаков
- Отображение результатов
- Сохранение результатов в текстовый файл

Использование:
1. Нажмите "Загрузить" и выберите CSV файл
2. Выберите столбцы для анализа (по умолчанию выбраны все)
3. Настройте параметры: минимальное количество признаков и метрику оценки
4. Нажмите "Рассчитать" для запуска алгоритма
5. Просмотрите результаты в текстовом поле
6. Нажмите "Сохранить" для сохранения результатов в файл

Поддерживаемые форматы:
- CSV файлы с разделителем запятая
- Первая строка должна содержать заголовки столбцов
- Данные должны быть числовыми

Метрики оценки:
- Коэффициент корреляции: оценивает взаимосвязь между признаками
- Среднеквадратичная ошибка: оценивает ошибку предсказания
- Информационный выигрыш: оценивает информативность признаков
