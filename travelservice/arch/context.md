# Контекст решения
<!-- Окружение системы (роли, участники, внешние системы) и связи системы с ним. Диаграмма контекста C4 и текстовое описание. 
-->
```plantuml
@startuml
skinparam defaultFontName Helvetica
skinparam roundcorner 20
left to right direction
skinparam shadowing<<System>> true

!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml

Person(admin, "Администратор") #Teal
Person(moderator, "Модератор") #Teal
Person(user, "Пользователь") #Teal

System(travel, "Поехали!", "Веб-сайт поиска попутчиков с личной страницей, маршрутами и поездками") #LightSeaGreen/TECHNOLOGY


Rel(admin, travel, "Просмотр, добавление и редактирование пользователей, добавление ролей, просмотр логов")
Rel(moderator, travel, "Модерация контента")
Rel(user, travel, "Регистрация и поиск пользователей, создание и просмотр маршрутов, создание и просмотр поездок")

@enduml

```
## Назначение систем
|Система| Описание|
|-------|---------|
| Сайт поиска попутчиков| Веб-интерфейс, обеспечивающий доступ к информации по маршрутам и поездкам. Бэкенд сервиса реализован в виде микросервисной архитектуры |

