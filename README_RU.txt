NEXAGRAM ANDROID — первая версия оболочки

Что это:
- Android-приложение на WebView, открывающее https://web.nexagram.site/
- Сохраняет cookies и DOM/local storage между запусками приложения.
- Включает JavaScript, загрузку файлов, запросы камеры/микрофона для сайта.
- Сохраняет состояние WebView при пересоздании Activity.

Важно:
Это исходный Android Studio проект, а не уже собранный APK.
Для сборки нужен Android Studio с Android SDK 35 и JDK 17:
1. Откройте папку NexagramAndroid в Android Studio.
2. Дождитесь Gradle Sync.
3. Build -> Build Bundle(s) / APK(s) -> Build APK(s).
4. APK появится в app/build/outputs/apk/debug/app-debug.apk.

Ограничения первой версии:
- Для первого открытия и обновления сайта нужен интернет.
- WebView-кеш не равен полноценному офлайн-кешу сообщений.
- Push-уведомления и надёжные входящие звонки в фоне ещё не подключены.
- Камера/микрофон будут доступны только если сайт запросит их и Android выдаст разрешение.

АВТОСБОРКА APK С ТЕЛЕФОНА ЧЕРЕЗ GITHUB:
1. Создайте новый репозиторий на github.com (например, nexagram-android).
2. Распакуйте ZIP проекта и загрузите ВСЕ файлы и папки проекта в корень репозитория, включая скрытую папку .github.
3. Откройте вкладку Actions -> Build Nexagram APK.
4. Нажмите Run workflow (или сборка начнётся после загрузки файлов в main).
5. После завершения откройте запуск workflow, внизу Artifacts -> Nexagram-APK и скачайте ZIP.
6. Распакуйте скачанный ZIP и установите app-debug.apk на Android.

Это debug APK для личного тестирования. Для публикации в Google Play нужна отдельная release-сборка и подпись.
