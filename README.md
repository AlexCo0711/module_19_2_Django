Цель: сделать первые записи в БД при помощи QuerySet запросов, закрепив знания о них.

Задача "Я буду устанавливать все игры!":
Для выполнения вам понадобится решение предыдущей задачи, а именно модели Buyer и Game из приложения task1.

При помощи QuerySet запросов необходимо создать 3 записи Buyer и 3 записи Game в вашу базу данных.
Все значения для полей этих записей выберите самостоятельно со следующими условиями:
Только один Buyer должен быть младше 18. (age)
Только одна Game должна быть без ограничения возраста. (age_limited)
После создания всех объектов свяжите их полем buyer у записей Game. Просто присвоить значение при создании объектов не получится. Для присвоения используйте метод set(objects), который принимает коллекцию объектов, например:
Game.objects.get(id=1).buyer.set((first_buyer, second_buyer)) - здесь игра c id=1 приобретается покупателями first_buyer и second_buyer.
При назначении покупателей для игр соблюсти следующие правила:
Только один из Buyer должен обладать всеми Game.
Buyer с возрастом меньше 18 не выдавать игры с ограничением по возрасту.
По итогу должны получится похожие записи на эти:
1.task1_buyer


2.task1_game


3.task1_game_buyer
