# Повторное отправление 

 **Акторы:** 

 - Пользователь

 **Цель:** В случае попытки отправить сообщение без связи, сохранение сообщения для повторного отправления, при подключении к сети 

 **Предусловия:** Отсутствие связи, плохое соединение, разрыв связи.

 **Сценарий:**

 1. Пользователь пытается отправить сообщение без связи или во время отправки сообщения связь прерывается
    
    Если прерывание было кратковременным и время ответа сервера не превысило заданного значения, начинается сценарий [Отправка сообщения]
    
    {Сообщение успешно отправлено}
    
 2. Пользователь получает визульное уведомление, что отправка сообщения не удалась
 3. Пользователь, нажав на данное уведомление, может выбрать "Удалить сообщение" или "Повторить отправку"
   
   Если пользователь выбрал "Удалить сообщение", начинается сценарий [Удаление сообщения]
   
    {Сообщение успешно удалено}
    
 4. При получении пользователь доступа к сети, пользователь выбирает "Повторить отправку"
 5. Пользователь получание уведомление о успешном отправлении сообщения

 **Результат:**

 - Сообщение не отправлено и удалено
 - Сообщение не отправлено, но не удалено
 - Сообщение отправлено

 **Исключения:**

 4. Если доступ был кратковременным, пользователь вновь получает уведомление, что отправка не удалась.

