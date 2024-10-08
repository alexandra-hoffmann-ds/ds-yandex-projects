# Прогнозные модели для отбора бурёнок в поголовье
В IT-компанию, выполняющую на заказ проекты по машинному обучению, обратился фермер, владелец молочного хозяйства. Он хочет купить бурёнок, чтобы расширить поголовье стада коров, для этого он заключил выгодный контракт с некой ассоциацией пастбищ. Фермер определяет качество молока по своей строгой методике, при этом ему нужно выполнять свой план развития молочного хозяйства; он хочет, чтобы каждая бурёнка давала не менее 6000 кг молока в год, а надой был вкусным. Целью проекта является создание модели машинного обучения, которая поможет фермеру управлять рисками и принимать объективное решение о покупке

# Вывод 
Три модели линейной регрессии были обучены для предсказания годового удоя коров. Результаты представлены с помощью коэффициента детерминации (R2):
- `Первая модель`: R2 = 0.7844, что означает, что предсказания модели точнее, чем среднее значение целевого признака в 78,44% случаев. Однако, модель имеет тенденцию к завышенным предсказаниям
- `Вторая модель`: R2 = 0.818, с более равномерным распределением остатков после преобразования нелинейной зависимости между целевым признаком и признаком СПО (сахаро-протеиновое соотношение)
- `Третья модель`: R2 = 0.8247, с дополнительным признаком (имя папы-быка из таблицы ferma_dad) и преобразованием нелинейности, имеет наивысшее значение R2

Для решения задачи бинарной классификации — предсказания признака `is_tasty`, то есть, вкуса молока — была выбрана и успешно обучена модель логистической регрессии. Результаты обучения представлены с помощью метрик Accuracy, Precision и Recall
