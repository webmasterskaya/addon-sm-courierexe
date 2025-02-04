# JoomShopping - "Курьерская служба 2008"

## Установка

1. Скачать zip архив, с установочным пакетом
2. Перейти, в панели управления сайтом, к установке расширений (Панель управления->Расширения->Менеджер расширений->Установка `https://ваш.сайт/administrator/index.php?option=com_installer`)
3. Загрузит, скчанный ранее, пакет и дождаться окончания установки
4. Перейти в менеджер плагинов (Панель управления->Расширения->Плагины `https://ваш.сайт/administrator/index.php?option=com_plugins&view=plugins`) и ввести в поиске фразу `Курьер`
5. В результатах поиска проверить, что плагин `JoomShopping - "Курьерская служба 2008"` опубликован (слева от названия установлена зелёная галочка)
6. Перейти к настройкам способов доставки JoomShopping (Панель управления->Компоненты->JoomShopping->Опции->Список способов доставки `https://ваш.сайт/administrator/index.php?option=com_jshopping&controller=shippings`)
7. Нажать кнопку `Создать` и заполнить поля. **Внимание!** В поле `Псевдоним` необходимо вписать значние `sm_courierexe_form`
8. После сохранения способа доставки, необходимо перейти к настройке расширения для расчета цен (кнопка `Расширения для расчета цены` вверху экрана)
9. В настройках расширения для расчёта цен выберите ```"Курьерская служба 2008" ``` и заполните обязательные поля:
  * `Длина`, `Ширина`, `Высота` - выберите характеристики, в которых указаны габаритные размеры товара
  * `Логин`, `Пароль`, `Код` - введите данные, полученные от вашего оператора, для подключения к системе
  * Свяжите ваши методы оплаты с методами службы доставки (инструкция доступна на странице настроек)
  * `Доставка` - отметьте способы доставки, у которых расчёт будет вестись через выбранное расширений
10. Созраните настройки расширения для расчёта цен и перейдите к настройке цен на доставку (Панель управления->Компоненты->JoomShopping->Опции->Цены на доставку `https://ваш.сайт/administrator/index.php?option=com_jshopping&controller=shippingsprices`)
11. Нажмите кнопку "Создать" и заполните необходимые поля
  * `Название` - выберите способ доставки, к которому будут применяться условия расчёта стоимости доставки
  * `Страна` - выберите `Russian Federation` и нажмите `Сохранить`
  * `Город отправления` - обязательно заполните это поле. При вводе будут доступны выпадающие подсказки. Название города необходимо выбрать из этого списка
  * `Способ доставки` - выберите тариф, по которому ведётся расчёт стоимости
  * `Показывать список ПВЗ`, `Параметры фильтрации ПВЗ`, `Параметры отображения списка ПВЗ` - Настройки отображениясписка ПВЗ (все подсказки доступны в настройках)
  * `Параметры расчёта доп. услуг` - учитывает комиссию за передачу денег, комиссию службы доставки и стоимость погрузочно-разгрузочных работ
12. Сохраните настройки. Расширение готово для использования

## Дополнительные рекомендации

### Поля в заказе
Система расчёта передаёт информацию о заказе, через стандартные поля JoomShopping! Включить их отображение можно настранице настроек JoomShopping (`/administrator/index.php?option=com_jshopping&controller=config&task=fieldregister`)

### Комиссия за передачу денег
Т.к. сервис взымает комиссию, в зависимости от выбранного способа оплаты - рекомендуем создать разные способы доставки для вариантов оплаты `Картой при получении`, `Наличными при получении`, `Предоплата 100%`
