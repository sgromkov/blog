---
layout: default
title: Упаковка npm-модулей, которую мы заслужили
description: 'Делюсь своими мыслями от просмотра доклада Дениса Красновского «Упаковка npm-модулей»'
parent: Видео
---

# Упаковка npm-модулей, которую мы заслужили

<div class="video">
    <iframe width="966" height="543" src="https://www.youtube.com/embed/vhHrHdtv7Po?start=746" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

Денис Красновский рассказал, как уменьшить весь бандла и сэкономить место в `node_modules`.

В результате просмотра доклада я создал несколько задач в рабочем проекте на matchtv.ru нацеленных на снижение веса бандла и ускорение его выполнения:
1. Убрать `propTypes` из продакшен-мода через `babel-plugin-transform-react-remove-prop-types` включив еще в нем опцию `removeImport: true`;
2. Проверить можем ли мы в `babel-preset-env` использовать `loose: true`? Не сломается ли IE11?
3. Проверить можем ли мы во всех остальных бабель-плагинах включить `loose: true`? Не сломается ли IE11?
4. Проверить размер наших скриптов через `import-cost`.
