# CorporationX

Это проект над которым я работал вместе со своей командой из 8 человек. Писали проект на микросервисной архитектуре. Т.к. над проектом работали разные команды, то для изучения всего кода моей команды необходимо смотреть сервисы в ветке unicorn-master. Фичи реализованные мной будут указаны ниже.

# Мои фичи

Создал публикатор для топика в Redis, который будет реагировать на все начала менторства. https://github.com/CorporationX/user_service/blob/unicorn-master/src/main/java/school/faang/user_service/publisher/MentorshipStartEventPublisher.java

Разработал систему достижений в соответствующем сервисе. Создал достижение, настроил RedisConfig, а также создал слушатель достижений который будет реагировать на события в других сервисах.
Слушатель (абстрактный класс также написан мной): https://github.com/CorporationX/achievement_service/blob/unicorn-master/src/main/java/faang/school/achievement/messaging/listener/MentorshipStartListener.java
Обработчик: https://github.com/CorporationX/achievement_service/blob/unicorn-master/src/main/java/faang/school/achievement/handler/AbstractAchievementHandler.java

С нуля написал телеграм бота и использовал его в сервисе нотификаций, для отправки всех событий пользователю:
https://github.com/CorporationX/notification_service/blob/unicorn-master/src/main/java/faang/school/notificationservice/service/telegram/TelegramService.java

Написал систему проектов в характерном сервисе. Также создал фильтры по которым эти проекты можно искать: https://github.com/CorporationX/project_service/blob/unicorn-master/src/main/java/faang/school/projectservice/controller/ProjectController.java

В сервисе работы с пользователями, я разработал систему подписчиков. Конкретная реализация здесь: https://github.com/CorporationX/user_service/blob/unicorn-master/src/main/java/school/faang/user_service/controller/SubscriptionController.java

