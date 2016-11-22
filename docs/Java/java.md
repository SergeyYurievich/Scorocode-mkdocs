## Подключение SDK

Дистрибутив Scorocode SWIFT SDK можно скачать [тут](https://github.com/Scorocode/scorocode-SDK-JS).

Исходный код Scorocode Java SDK опубликован в репозитории (https://github.com/Scorocode/scorocode-sdk-java).

Подключить библиотеку к проекту можно при помощи Gradle добавив в dependencies:

```java
dependencies {
   compile 'ru.prof-itgroup:scorocode_sdk:1.0.15-beta'
}
```

Убедитесь, что gradle ищет библиотеки в рекомендуемом Google репозитории jcenter (который включает в себя библиотеки maven):

```java
repositories {
   jcenter()
}
```
