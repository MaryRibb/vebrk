# vebrk1
## Определение
REST (от англ. Representational State Transfer — «передача состояния представления») — архитектурный стиль взаимодействия компонентов распределённого приложения в сети.  
REST - то архитектура, т.е. принципы построения распределенных гипермедиа систем, того что другими словами называется World Wide Web, включая универсальные способы обработки и передачи состояний ресурсов по HTTP. Автор идеи и термина Рой Филдинг 2000г.  
## Ответ на первый вопрос
Моя разработанная API является RESTfull.  
1.Во первых существуют различные методы,которые описывают тип операции,которую будет осуществлять API.
⋅⋅⋅* Get-для получения ресурса   
⋅⋅⋅* Post – для создания ресурса  
⋅⋅⋅* Put – для обновления существующего ресурса.  
⋅⋅⋅* Delete – для удаления уже существующего ресурса.  
2.Во вторых использованы правильные HTTP коды  
⋅⋅⋅* 200 OK - самый часто используемый код, свидетельствующий об успехе операции;   
⋅⋅⋅* 201 CREATED - используется, когда с помощью метода POST создается ресурс;  
⋅⋅⋅* 400 BAD REQUEST - используется, когда со стороны клиента допущена ошибка в вводе    
⋅⋅⋅* 401 UNAUTHORIZED / 403 FORBIDDEN - используются, если для выполнения операции требуется аутентификация пользователя или системы;    
⋅⋅⋅* 404 NOT FOUND - используется, если в системе отсутствуют искомые ресурсы;  
⋅⋅⋅* 403 Forbidden – установлены неверные права доступа  
3.В третьих .Client-Server. Система разделена на клиентов и на серверов.Потому что мы запускаем на сервере ,а храним данные на локальном.  
4.В четвертых .	Сервер не хранит информацию о клиентах. В запросе должна храниться вся необходимая информация для обработки запроса и если необходимо, идентификации клиента.  
_______________________________________________________________________________________________________________________________________________________________________

### CRUD — акроним, обозначающий четыре базовые функции, используемые при работе с базами данных: создание (create), чтение (read), модификация (update), удаление (delete).
В качестве запроса возьмём get.  
http://tutorial-api.local:8081/api/v1/animal/60cdbe07cdaa71546655ee43  
```
{
	“animal_name”: “Степа”,
	“person_name”:”qqq”

}
```
Выводит:
```
{
	“id”:”60cdb345cdaa71546655tt42”,
	“animal_name”: “Степа”,
	“person_name”:”qqq”
}
```
В качестве запроса возьмём put.  
http://project-symfony.local:8081/api/v1/users/60cdbe07cdaa71546655ee43
```
{
	“animal_name”: “Борька”,
	“person_name”:”qqq”

}
```
Выводит:
```
{
	“id”:”60cdb345cdaa71546655tt42”,
	“animal_name”: “Борька”,
	“person_name”:”qqq”
}
```


## Ответ на второй вопрос
Два запроса ,представленные выше, являются идемпонентными
Запросы являются идемпонентными,потому что повторный идентичный запрос, сделанный один или несколько раз подряд, имеет один и тот же эффект, не изменяющий состояние сервера. 
Другими словами, идемпотентный метод не должен иметь никаких побочных эффектов (side-effects), кроме сбора статистики или подобных операций. Корректно реализованные методы GET,  PUT и DELETE идемпотентны, но не метод POST.   
С помощью get мы будем видеть выведенные одни те же данные,которые не будут меняться.Результат будет одним и тем же ,но ответ может быть разным.  
С помощью put будет создаваться и выводиться один и тот же компонент.  


## Ссылки
https://ru.wikipedia.org/wiki/Список_кодов_состояния_HTTP 
https://ru.wikipedia.org/wiki/REST
https://developer.mozilla.org/ru/docs/Glossary/Idempotent  







