# test
# Автоматизированные тесты для веб и мобильного приложения Wikipedia

## Описание проекта

Данный проект содержит набор автоматизированных UI-тестов для проверки:

- веб-версии сайта **ru.wikipedia.org**
- мобильного приложения **Wikipedia (Android)**

Проект демонстрирует навыки автоматизации тестирования веб- и мобильных пользовательских интерфейсов с использованием современных инструментов и подходов.

## Покрытие тестами

### Веб-тесты (ru.wikipedia.org)

- Проверка отображения главной страницы
- Проверка поиска статей
- Проверка открытия статьи
- Проверка элементов интерфейса

**Всего:** 4 теста

### Мобильные тесты (Wikipedia Android)

- Проверка отображения поля поиска на главном экране
- Поиск и открытие статьи
- Навигация назад после открытия статьи

**Всего:** 3 теста

## Используемые технологии

- Java 11
- Selenium WebDriver
- Appium
- TestNG
- Maven

## Требования для запуска

### Общие требования

- Установить **Java 11** или выше
- Установить **Maven**
- Установить браузер **Google Chrome**

### Требования для мобильных тестов

- Установить **Node.js**
- Установить **Appium**:
  ```bash
  npm install -g appium
- Установить **Android Studio**
- Создать и запустить **Android-эмулятор**
- Установить приложение **Wikipedia** на эмулятор

## Загрузка APK Wikipedia

Скачать APK приложения Wikipedia можно по официальной ссылке:

https://github.com/wikimedia/apps-android-wikipedia/releases

После скачивания APK необходимо:

1. Установить приложение на эмулятор:
   ```bash
   adb install app-alpha-universal-release.apk
   
2. Указать путь к APK в классе WebDriverFactory
(если используется запуск через APK):

caps.setCapability("app", "ПУТЬ_К_APK_ФАЙЛУ");

## Запуск тестов

mvn clean test

## Запуск только веб-тестов

mvn test -Dtest=WikipediaTests

## Запуск мобильных тестов

## Запустить Android эмулятор
(через Android Studio или командой):

emulator -avd Medium_Phone_API_36_1

## Запустить Appium сервер:

appium -p 4723

## Запустить мобильные тесты:

mvn test -Dtest=WikipediaMobileTests

### Скриншоты

<img width="758" height="207" alt="test" src="https://github.com/user-attachments/assets/ffa4851f-96e8-4a1a-b498-5e1d788a35b5" />
<img width="810" height="210" alt="mobtest1" src="https://github.com/user-attachments/assets/90ffa062-9166-4ce8-97c1-5e1ab53dd2c6" />
<img width="548" height="673" alt="mobtest" src="https://github.com/user-attachments/assets/ca998388-252f-4a11-9b7a-dd2dabae9c37" />
<img width="575" height="291" alt="appium" src="https://github.com/user-attachments/assets/d915886e-a6b9-4af8-80b3-b7589d285f0d" />

## Примечания
-Мобильные тесты запускаются на Android-эмуляторе через Appium

-Appium сервер должен быть запущен до старта мобильных тестов

-В проекте используется TestNG в качестве тестового фреймворка

