# Задача №1

Дайте письменые ответы на следующие вопросы:<br>

- В чём отличие режимов работы сервисов в Docker Swarm кластере: replication и global?<br>
- Какой алгоритм выбора лидера используется в Docker Swarm кластере?<br>
- Что такое Overlay Network?<br>

## Ответ

1. В ``global`` режиме выполняется одна реплика службы на узел роя. Количество глобальных реплик равно количеству узлов swarm.<br> 
В ``replicaрежиме`` вы можете запускать любое количество экземпляров службы.<br>

2. В Docker Swarm кластере используется так называемый алгоритм поддержания распределенного консенсуса — Raft.<br>
Выбор лидера происходит следующим образом: если ноды-фолловеры не слышат лидера, они переходят в статус кандидата,<br>
кандидат на лидера отправляет остальным нодам запрос на голосование и, большинством голосов, выбирается лидером.<br>

3. Overlay network - это внутренняя виртуальная сеть кластера docker swarm,<br>
которая упрощает взаимодействие узлов кластера между собой.<br>

_____________________________ 

# Задача №2

Создать ваш первый Docker Swarm кластер в Яндекс.Облаке<br>

Для получения зачета, вам необходимо предоставить скриншот из терминала (консоли), с выводом команды:<br>

`` docker node ls

## Ответ

[node](https://github.com/davlyatov-ts/virt-5/blob/master/node.png)<br>
________________________

# Задача №3

Создать ваш первый, готовый к боевой эксплуатации кластер мониторинга, состоящий из стека микросервисов.<br>

Для получения зачета, вам необходимо предоставить скриншот из терминала (консоли), с выводом команды:<br>

``docker service ls``

## Ответ

[service](https://github.com/davlyatov-ts/virt-5/blob/master/service.png)<br>
___________________________

# Задача №4

Выполнить на лидере Docker Swarm кластера команду (указанную ниже) и дать письменное описание её функционала,<br>
что она делает и зачем она нужна<br>

```
см.документацию: https://docs.docker.com/engine/swarm/swarm_manager_locking/
docker swarm update --autolock=true
```

## Ответ

Включает автоблокировку на существующем рое


