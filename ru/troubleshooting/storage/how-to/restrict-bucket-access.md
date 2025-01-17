# Как ограничить доступ к бакету для пользователя


## Описание сценария {#case-description}

Необходимо ограничить другому пользователю или сервисному аккаунту доступ к бакету.

## Решение {#case-resolution}

Пользователи с сервисными ролями `storage.viewer`, `storage.configViewer`, `storage.configurer`, `storage.editor` или `storage.admin` иимеют разные полномочия и права доступа к бакетам:
* роли `storage.viewer`, `storage.editor` и `storage.admin` дают доступ на просмотр или редактирование файлов в бакетах; 
* роль `storage.configViewer` позволяет только лишь просматривать настройки  безопасности бакетов и объектов в них (без доступа к объектам);
* роль `storage.configurer` позволяет изменять эти настройки. 
  
Подробнее о сервисных ролях в Object Storage пишем в [документации](../../../storage/security/).

Можно [настроить доступ к бакету через ACL](../../../storage/concepts/acl), удалив при этом сервисные роли у нужных пользователей, или настроить политики доступа к каждому бакету — подробнее [пишем здесь](../../../storage/concepts/policy).
 