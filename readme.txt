# Программа для генерации XML Sitemap

Этот скрипт позволяет создавать XML Sitemap и XML Sitemap Index на основе данных из CSV файла.

## Установка

Для запуска программы необходим Python 3.x. Вам также потребуется установить модули `csv` и `xml.etree.ElementTree`. Вы можете установить их с помощью pip:

pip install csv xml.etree.ElementTree

markdown
Копировать код

## Использование

1. Подготовьте CSV файл с данными. В файле должен быть столбец с URL.

2. Запустите программу, укажите путь к CSV файлу, и программа сгенерирует XML файлы Sitemap и Sitemap Index.

```python
python main.py

Пример использования программы:

python
Копировать код
# Подготовка данных
urls = ['https://example.com/page1', 'https://example.com/page2', 'https://example.com/page3']

# Создание XML Sitemap
sitemap = generate_sitemap(urls)
save_sitemap(sitemap, 'sitemap.xml')

# Генерация ссылки на созданный файл
sitemap_urls = ['https://example.com/sitemap.xml']

# Создание XML Sitemap Index
sitemap_xml = generate_sitemapindex(sitemap_urls)

# Сохранение Sitemap Index
save_sitemap(sitemap_xml, 'sitemapindex.xml')
Функции
generate_sitemap(urls)
Функция принимает список URL и создает XML Sitemap.

save_sitemap(urlset, filename)
Функция принимает XML элемент urlset и имя файла, и сохраняет XML в файл.

generate_sitemapindex(urls)
Функция принимает список URL и создает XML Sitemap Index.

Структура данных
Программа предполагает следующую структуру данных в CSV файле:

Столбец с URL
Программа также использует словари для классификации URL по категориям.
Дополнительные сведения
Программа также содержит код для распределения URL по различным категориям и генерации отдельных XML Sitemap файлов для каждой категории.