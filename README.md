# Project (partA)
**Тема: Відношення між класами: асоціація, агрегація, композиція, реалізація.**

## ПОСТАНОВКА ЗАВДАННЯ

1.	Обрати і коротко описати нову предметну область.
2.	Для обраної предметної області з використанням https://www.lucidchart.com за два етапи побудувати модель предметної області у вигляді діаграми класів, на якій класи/інтерфейси мають бути пов’язані різними типами відношень: асоціація, агрегація, композиція, реалізація. До тест-проєкту додати тест-клас, який буде тестувати методи з п.3.
3.	Засобами середи розробки (IDE) створити каркас проєкту, для цього необхідно визначити в окремих файлах *.cs всі спроєктовані у п.2 інтерфейси, класи, перелічення. Коректно реалізувати відношення між класами! Реалізовувати властивості, конструктори і методи у класах не потрібно! Замість реального коду вони мають містити заглушки throw new NotImplementedException().
4.	Для тестування спроєктованих класів додати проєкт з тест-класами, які повинні містити достатній для повноцінного тестування набір реалізованих unit-тестів.
5.	Використання GitHub-репозиторію з коммітами є обов’язковим! Репозиторій повинен мати Readme.md файл, в який необхідно:
- додати красивий опис предметної області, для цього використовуйте заголовки, списки, рисунки та ін.);
- вставити розроблену діаграму класів.

7.	Оформити звіт:
-	Титульний аркуш
-	Завдання
-	Опис предметної області
-	Проєктування діаграми класів (аналог рис. 1 і рис. 2)
-	Реалізація класів 
-	Реалізація тест-класів
-	Результати запуску unit-тестів
-	Посилання на GitHub-репозиторій

## Опис предметної області

Основна тема: магазин.
Предметна область представляє собою деяку модель для взаємодії з магазином та постачальником товару, вона включає в себе деякі аспекти роботи магазину та постачання товарів до нього.
-	Store: представляє собою основну сутність, може виконувати дії такі як: додавання товару до інвентарю (AddProductToInventory), виведення інформації про інвентар магазину (PrintInventory), продаж товарів(SellProduct).
-	Supplier: постачальник товарів, який може постачати товар до магазину (SupplyProductsToStore).
-	Product: представляє товари, які представлені в магазині.
-	ProductStatus: перерахування статусу товару.
-	InventoryItem: представляє собою каталог товарів, які є в магазині.
-	Isellable: представляє собою об’єкти, які можна продавати. 
-	IInventoryManager: управляє інвентарем товарів у магазині, може додавати товар до магазину зі вказаною його кількістю (AddProductToInventory) та повертати інформацію про товар та його кількість (PrintInventory).

**Відношення між класами**

___Асаціація___

Класи  _Store_  та  _Supplier_  через метод SupplyProductsToStore, де умовно постачальник постачає товати до магазину.

Класи _Store_ та _Product_ через методи AddProductToInventory та SellProduct, де товари додаються до інвентарю та продаються.

Клас _Product_ та перелічення _ProductStatus_.

___Агрегація___

Клас  _Store_  та  _InventoryItem_, що передбачає собою колекцію товарів в інвентарі. Але товар може існувати незалежно.

___Реалізація___

Клас _Product_ реалізує інтерфейс _ISellable_.

Клас _Store_ реалізує інтерфейс _IInventoryManager_.






