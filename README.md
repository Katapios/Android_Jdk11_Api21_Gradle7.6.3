# MyFirstApp

Простой Android проект на Java с минимальной конфигурацией.

## Характеристики проекта

### Технические параметры
- **Язык программирования**: Java 11
- **Минимальная версия SDK**: Android 5.0 (API 21)
- **Целевая версия SDK**: Android 14 (API 34)
- **Версия компиляции SDK**: Android 14 (API 34)
- **Версия приложения**: 1.0 (versionCode: 1)

### Инструменты сборки
- **Gradle**: 7.6.3
- **Android Gradle Plugin**: 7.4.2
- **JDK**: 11 (Temurin)

### Зависимости
- AndroidX AppCompat: 1.6.1
- Material Design Components: 1.9.0
- ConstraintLayout: 2.1.4

### Структура проекта
```
MyFirstApp/
├── app/
│   ├── build.gradle          # Конфигурация модуля приложения
│   ├── proguard-rules.pro    # Правила ProGuard
│   └── src/
│       └── main/
│           ├── AndroidManifest.xml
│           ├── java/
│           │   └── com/example/myfirstapp/
│           │       └── MainActivity.java
│           └── res/
│               ├── layout/
│               │   └── activity_main.xml
│               └── values/
│                   └── strings.xml
├── build.gradle              # Корневой build.gradle
├── settings.gradle           # Настройки проекта
├── gradle.properties         # Свойства Gradle
└── gradlew                   # Gradle Wrapper скрипт
```

## Требования

### Системные требования
- **JDK**: 11 или выше
- **Android SDK**: API 34 (Android 14)
- **Gradle**: 7.6.3 (включен через wrapper)

### Настройка окружения
1. Установите JDK 11
2. Установите Android SDK через Android Studio или командную строку
3. Настройте переменную окружения `ANDROID_HOME` (опционально)

**Примечание**: Если Gradle не находит JDK 11 автоматически, раскомментируйте и укажите путь в `gradle.properties`:
```properties
org.gradle.java.home=/path/to/jdk11
```

## Инструкции по сборке

### Сборка через командную строку

#### Очистка проекта
```bash
./gradlew clean
```

#### Сборка Debug APK
```bash
./gradlew assembleDebug
```
APK будет создан в: `app/build/outputs/apk/debug/app-debug.apk`

#### Сборка Release APK
```bash
./gradlew assembleRelease
```
APK будет создан в: `app/build/outputs/apk/release/app-release.apk`

#### Полная сборка проекта
```bash
./gradlew build
```
Выполняет сборку, тесты и проверки (lint).

#### Установка на устройство
```bash
./gradlew installDebug
```
Требует подключенное устройство или эмулятор с включенной отладкой.

### Сборка через Android Studio

1. Откройте проект в Android Studio
2. Дождитесь синхронизации Gradle
3. Выберите конфигурацию сборки (Debug/Release)
4. Нажмите **Build > Make Project** или используйте горячие клавиши

### Настройка JDK в Android Studio

Если проект не собирается, убедитесь, что в Android Studio выбран JDK 11:

1. **File > Project Structure > SDK Location**
2. Укажите путь к JDK 11 в поле **JDK location**
3. Или используйте встроенный JDK из Android Studio

## Конфигурация

### Изменение минимальной версии SDK
Отредактируйте `app/build.gradle`:
```gradle
defaultConfig {
    minSdk 21  // Измените на нужное значение
}
```

### Изменение версии компиляции
Отредактируйте `app/build.gradle`:
```gradle
android {
    compileSdkVersion 34  // Измените на нужное значение
}
```

### Настройка Java версии
В `app/build.gradle`:
```gradle
compileOptions {
    sourceCompatibility JavaVersion.VERSION_11
    targetCompatibility JavaVersion.VERSION_11
}
```

## Примечания

- Проект использует Java 11 для сборки (настроено в `gradle.properties`)
- Android Gradle Plugin 7.4.2 совместим с Java 11
- Для использования более новых версий AGP потребуется Java 17+
- Иконка приложения использует системную иконку по умолчанию

## Лицензия

Этот проект создан в образовательных целях.

