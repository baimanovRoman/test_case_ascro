### Предисловие к Тест-кейсам

Для успешного функционирования и проверки работы функций сайта, связанных с использованием криптовалютных кошельков, необходимо убедиться в правильности интеграции и работы с двумя основными кошельками: TronLink и WalletConnect. TronLink используется для управления транзакциями и взаимодействия с сетью Tron, а WalletConnect обеспечивает подключение кошельков к децентрализованным приложениям через мобильные устройства.

Тест-кейсы направлены на проверку следующих ключевых сценариев:

1. **Подключение кошелька TronLink/WalletConnect к сайту:**
   - Убедиться, что пользователь может успешно подключить свой кошелек TronLink/WalletConnect к сайту.
   - Проверить, что процесс подключения интуитивно понятен и без ошибок.
   - Проверить отображение информации о подключенном кошельке (адрес кошелька, баланс и т.д.).

2. **Создание сделки от Buyer:**
   - Удостовериться, что пользователь может успешно создать сделку от имени Buyer после подключения кошелька TronLink/WalletConnect.
   - Проверить, что все обязательные поля для Buyer заполнены корректно и соответствуют данным кошелька пользователя.

3. **Создание сделки от Seller:**
   - Проверить, что пользователь может создать сделку от имени Seller после подключения кошелька TronLink/WalletConnect.
   - Убедиться, что информация о Seller корректно заполнена и совпадает с данными кошелька пользователя.

4. **Подтверждение сделки от Seller:**
   - Проверить процесс подтверждения сделки от Seller через кошелек TronLink/WalletConnect.
   - Удостовериться, что Seller может успешно подтвердить свое участие в сделке.

5. **Открытие диспута между Buyer и Seller:**
   - Убедиться, что пользователи могут успешно открыть диспут по сделке через свои кошельки TronLink/WalletConnect.
   - Проверить, что диспут отображается корректно и информация о нем доступна для всех участников сделки.

6. **Заявление об исполнении сделки от Seller:**
   - Проверить возможность Seller заявить об исполнении сделки через свой кошелек TronLink/WalletConnect.
   - Удостовериться, что информация о статусе сделки обновляется корректно после заявления об исполнении.

7. **Подтверждение участия в сделке от Guarantor:**
   - В случае участия Guarantor в сделке, проверить процесс подтверждения участия через кошелек TronLink/WalletConnect.
   - Убедиться, что Guarantor может успешно подтвердить свое участие в сделке и его роль корректно отображается.
8. **Cозание сделки с агентами:**
   - Убедится что после исполнения сделки деньги попали на счет агентам (выполнить пункты 4-7)

#### Для проверки правильности выполенения всех кейсов необходимо смотреть транзакции в контракте
#### Детальнее все тест-кейсы описаны ниже. Повторить все операции для TronLonk и WolletConnect несколько раз на разных кошельках

----



### Тест-кейс 1: Подключение через кошелек TronLink при отсутствии расширения в браузере

**Название**: Проверка подключения через кошелек TronLink при отсутствии расширения в браузере

**Предусловия**:
1. Расширение TronLink не установлено в браузере.
2. Пользователь находится на странице сайта, где необходимо подключение через TronLink.

**Шаги**:
1. Открыть браузер и перейти на сайт.
2. Нажать кнопку "Connect Wallet" на сайте.
3. Выбрать TronLink в списке доступных кошельков.

**Ожидаемый результат**:
- Сайт проверяет наличие расширения TronLink в браузере.
- При отсутствии расширения TronLink появляется уведомление с предложением установить расширение.
- Уведомление содержит ссылку на страницу установки расширения TronLink.

**Постусловия**:
- Пользователь должен увидеть четкое и информативное сообщение о необходимости установки расширения TronLink.
- Сообщение должно содержать ссылку, ведущую на страницу установки расширения в магазине расширений браузера (например, Chrome Web Store).

### Возможные уточнения и дополнения:
1. **Дополнительные шаги для пользователя**:
   - Переход по ссылке и установка расширения TronLink.
   - После установки, возвращение на сайт и повторное нажатие на кнопку "Connect Wallet".

2. **Варианты проверки**:
   - Проверка работы уведомления в различных браузерах (Chrome, Firefox, Edge и т.д.).
   - Проверка работы уведомления на различных операционных системах (Windows, macOS, Linux).
---

### Тест-кейс 2: Подключение через кошелек TronLink с компьютера

**Название**: Тестирование подключения через кошелек TronLink с компьютера

**Предусловия**:
1. Установлено расширение TronLink в браузере.
2. Кошелек TronLink создан и имеет необходимое количество средств.
3. Пользователь находится на странице сайта, где необходимо подключение через TronLink.

**Шаги**:
1. Открыть браузер и перейти на сайт.
2. Нажать кнопку "Подключить кошелек" на сайте.
3. Выбрать TronLink в списке доступных кошельков.
4. В всплывающем окне TronLink подтвердить подключение кошелька к сайту.

**Ожидаемый результат**:
- Всплывающее окно TronLink появляется с запросом на подтверждение подключения.
- После подтверждения сайт успешно подключается к кошельку TronLink.
- На сайте отображается информация о подключенном кошельке (например, адрес кошелька и баланс).

**Постусловия**:
- Подключение должно быть успешным и сайт должен иметь доступ к необходимой информации кошелька.
---


### Тест-кейс 3: Подключение через кошелек TronLink с телефона

**Название**: Тестирование подключения через кошелек TronLink с телефона

**Предусловия**:
1. Установлено мобильное приложение TronLink.
2. Кошелек TronLink создан и имеет необходимое количество средств.
3. Пользователь находится на странице сайта, где необходимо подключение через TronLink, используя мобильный браузер.

**Шаги**:
1. Открыть мобильный браузер и перейти на сайт.
2. Нажать кнопку "Подключить кошелек" на сайте.
3. Выбрать TronLink в списке доступных кошельков.
4. Приложение TronLink должно автоматически открыться или предложить перейти к приложению.
5. В приложении TronLink подтвердить подключение кошелька к сайту.

**Ожидаемый результат**:
- Приложение TronLink открывается с запросом на подтверждение подключения.
- После подтверждения сайт успешно подключается к кошельку TronLink.
- На сайте отображается информация о подключенном кошельке (например, адрес кошелька и баланс).

**Постусловия**:
- Подключение должно быть успешным и сайт должен иметь доступ к необходимой информации кошелька.

---


### Тест-кейс 4: Создание сделки от Buyer

**Название**: Тестирование создания сделки от Buyer через кошелек TronLink

**Предусловия**:
1. Установлено расширение TronLink в браузере.
2. Кошелек TronLink подключен и активен.
3. Пользователь авторизован на сайте через кошелек TronLink.

**Шаги**:
1. Перейти на сайт и войти через кошелек TronLink.
2. Нажать на кнопку "Create a Deal".
3. Выбрать роль "Buyer" и нажать "Continue".
4. Убедиться, что информация о Buyer автоматически заполнена и соответствует информации из кошелька пользователя.
5. Ввести кошелек продавца (Seller).
6. Ввести информацию о гаранте (Guarantor):
   - Кошелек гаранта.
   - Комментарий, если гарант не участвует.
   - Комиссию, если гарант участвует.
7. Ввести стоимость сделки.
8. Ввести условия сделки.
9. Нажать на кнопку "Create" для создания сделки.

**Ожидаемый результат**:
- Сделка успешно создается.
- Пользователь получает подтверждение о создании сделки.
- Вся введенная информация корректно отображается и совпадает с введенными данными.
- Сделка отображается в списке активных сделок пользователя.

**Постусловия**:
- Сделка должна быть видна в профиле пользователя Buyer.
- Вся информация о сделке должна быть доступна для дальнейших действий (например, подтверждение, изменение условий и т.д.).

### Примерный ход выполнения тест-кейса:

1. **Переход на сайт и вход через TronLink**:
   - Перейти на сайт и войти через кошелек TronLink.
   - Убедиться, что пользователь авторизован.

2. **Создание сделки**:
   - Нажать кнопку "Create a Deal".
   - Выбрать роль "Buyer" и нажать "Continue".

3. **Проверка информации о Buyer**:
   - Убедиться, что информация о Buyer автоматически заполнена и совпадает с данными кошелька TronLink.

4. **Заполнение информации о Seller**:
   - Ввести кошелек продавца.

5. **Заполнение информации о Guarantor**:
   - Ввести кошелек гаранта.
   - Ввести комментарий, если гарант не участвует.
   - Ввести комиссию, если гарант участвует.

6. **Заполнение стоимости сделки и условий**:
   - Ввести стоимость сделки.
   - Ввести условия сделки.

7. **Создание сделки**:
   - Нажать кнопку "Create".
   - Подтвердить создание сделки в всплывающем окне TronLink, если требуется.

**Ожидаемые результаты**:
- Пользователь видит подтверждение успешного создания сделки.
- Введенные данные отображаются корректно.
- Сделка отображается в списке активных сделок пользователя.
---


### Тест-кейс: Подтверждение сделки от имени Seller

**Название**: Тестирование подтверждения сделки от имени Seller через кошелек TronLink

**Предусловия**:
1. Установлено расширение TronLink в браузере.
2. У пользователя есть доступ к кошельку, указанному в сделке как Seller.
3. Сделка уже создана и ожидает подтверждения от Seller.

**Шаги**:
1. Переключить кошелек TronLink на нужный кошелек Seller.
2. Перейти на сайт и войти через кошелек TronLink.
3. Перейти к списку сделок.
4. Найти и выбрать нужную сделку, в которой данный пользователь указан как Seller.
5. Нажать на кнопку для подтверждения участия в сделке.
6. Подтвердить транзакцию в всплывающем окне TronLink.

**Ожидаемый результат**:
- Пользователь успешно подтверждает участие в сделке.
- Пользователь получает уведомление о подтверждении сделки.
- Сделка обновляется и отображает статус "подтверждена" или аналогичный статус.
- Вся введенная информация корректно отображается и совпадает с данными сделки.

**Постусловия**:
- Сделка должна быть видна в профиле пользователя Seller с обновленным статусом.
- Вся информация о сделке должна быть доступна для дальнейших действий (например, выполнение условий сделки).

### Примерный ход выполнения тест-кейса:

1. **Переключение кошелька TronLink на нужный кошелек Seller**:
   - Открыть приложение TronLink.
   - Переключить кошелек на нужный кошелек, указанный в сделке как Seller.

2. **Вход на сайт через TronLink**:
   - Перейти на сайт и войти через подключенный кошелек TronLink.

3. **Переход к списку сделок**:
   - Перейти в раздел, где отображаются активные сделки пользователя.

4. **Выбор нужной сделки**:
   - Найти в списке сделок ту, которая требует подтверждения от Seller.
   - Выбрать эту сделку.

5. **Подтверждение участия**:
   - Нажать на кнопку для подтверждения участия в сделке.
   - Подтвердить транзакцию в всплывающем окне TronLink.

**Ожидаемые результаты**:
- Пользователь видит уведомление об успешном подтверждении сделки.
- Статус сделки обновляется и отображается как "подтверждена" или аналогично.
- Вся информация о сделке отображается корректно и совпадает с введенными данными.
---


### Тест-кейс: Подтверждение сделки от имени Guarantor

**Название**: Тестирование подтверждения сделки от имени Guarantor через кошелек TronLink

**Предусловия**:
1. Установлено расширение TronLink в браузере.
2. У пользователя есть доступ к кошельку, указанному в сделке как Guarantor.
3. Сделка уже создана и ожидает подтверждения от Guarantor.

**Шаги**:
1. Переключить кошелек TronLink на нужный кошелек Guarantor.
2. Перейти на сайт и войти через кошелек TronLink.
3. Перейти к списку сделок.
4. Найти и выбрать нужную сделку, в которой данный пользователь указан как Guarantor.
5. Нажать на кнопку для подтверждения участия в сделке.
6. Подтвердить транзакцию в всплывающем окне TronLink.

**Ожидаемый результат**:
- Пользователь успешно подтверждает участие в сделке.
- Пользователь получает уведомление о подтверждении сделки.
- Сделка обновляется и отображает статус "подтверждена" или аналогичный статус.
- Вся введенная информация корректно отображается и совпадает с данными сделки.

**Постусловия**:
- Сделка должна быть видна в профиле пользователя Guarantor с обновленным статусом.
- Вся информация о сделке должна быть доступна для дальнейших действий (например, выполнение условий сделки).

### Примерный ход выполнения тест-кейса:

1. **Переключение кошелька TronLink на нужный кошелек Guarantor**:
   - Открыть приложение TronLink.
   - Переключить кошелек на нужный кошелек, указанный в сделке как Guarantor.

2. **Вход на сайт через TronLink**:
   - Перейти на сайт и войти через подключенный кошелек TronLink.

3. **Переход к списку сделок**:
   - Перейти в раздел, где отображаются активные сделки пользователя.

4. **Выбор нужной сделки**:
   - Найти в списке сделок ту, которая требует подтверждения от Guarantor.
   - Выбрать эту сделку.

5. **Подтверждение участия**:
   - Нажать на кнопку для подтверждения участия в сделке.
   - Подтвердить транзакцию в всплывающем окне TronLink.

**Ожидаемые результаты**:
- Пользователь видит уведомление об успешном подтверждении сделки.
- Статус сделки обновляется и отображается как "подтверждена" или аналогично.
- Вся информация о сделке отображается корректно и совпадает с введенными данными.
---


### Тест-кейс: Заявление об исполнении сделки от имени Seller

**Название**: Тестирование заявления об исполнении сделки от имени Seller через кошелек TronLink

**Предусловия**:
1. Установлено расширение TronLink в браузере.
2. У пользователя есть доступ к кошельку, указанному в сделке как Seller.
3. Сделка уже создана и подтверждена участниками, включая Guarantor (если применяется).

**Шаги**:
1. Переключить кошелек TronLink на нужный кошелек Seller.
2. Перейти на сайт и войти через кошелек TronLink.
3. Перейти к списку сделок.
4. Найти и выбрать нужную сделку, в которой данный пользователь указан как Seller.
5. Нажать на кнопку для заявления об исполнении сделки.
6. Подтвердить заявление об исполнении сделки в всплывающем окне TronLink, если требуется.

**Ожидаемый результат**:
- Пользователь успешно заявляет об исполнении сделки.
- Пользователь получает уведомление о том, что заявление об исполнении сделки принято.
- Сделка обновляется и отображает статус "исполнена" или аналогичный статус.
- Вся введенная информация корректно отображается и совпадает с данными сделки.

**Постусловия**:
- Сделка должна быть видна в профиле пользователя Seller с обновленным статусом.
- Вся информация о сделке должна быть доступна для дальнейших действий (например, подтверждение от других участников сделки).

### Примерный ход выполнения тест-кейса:

1. **Переключение кошелька TronLink на нужный кошелек Seller**:
   - Открыть приложение TronLink.
   - Переключить кошелек на нужный кошелек, указанный в сделке как Seller.

2. **Вход на сайт через TronLink**:
   - Перейти на сайт и войти через подключенный кошелек TronLink.

3. **Переход к списку сделок**:
   - Перейти в раздел, где отображаются активные сделки пользователя.

4. **Выбор нужной сделки**:
   - Найти в списке сделок ту, которая требует заявления об исполнении от Seller.
   - Выбрать эту сделку.

5. **Заявление об исполнении сделки**:
   - Нажать на кнопку для заявления об исполнении сделки.
   - Подтвердить действие в всплывающем окне TronLink, если требуется.

**Ожидаемые результаты**:
- Пользователь видит уведомление об успешном заявлении об исполнении сделки.
- Статус сделки обновляется и отображается как "исполнена" или аналогично.
- Вся информация о сделке отображается корректно и совпадает с введенными данными.
---

### Тест-кейс: Заявление об исполнении сделки от имени Seller

**Название**: Тестирование заявления об исполнении сделки от имени Seller через кошелек TronLink

**Предусловия**:
1. Установлено расширение TronLink в браузере.
2. У пользователя есть доступ к кошельку, указанному в сделке как Seller.
3. Сделка уже создана и подтверждена участниками, включая Guarantor (если применяется).

**Шаги**:
1. Переключить кошелек TronLink на нужный кошелек Seller.
2. Перейти на сайт и войти через кошелек TronLink.
3. Перейти к списку сделок.
4. Найти и выбрать нужную сделку, в которой данный пользователь указан как Seller.
5. Нажать на кнопку для заявления об исполнении сделки.
6. Подтвердить заявление об исполнении сделки в всплывающем окне TronLink, если требуется.

**Ожидаемый результат**:
- Пользователь успешно заявляет об исполнении сделки.
- Пользователь получает уведомление о том, что заявление об исполнении сделки принято.
- Сделка обновляется и отображает статус "исполнена" или аналогичный статус.
- Вся введенная информация корректно отображается и совпадает с данными сделки.

**Постусловия**:
- Сделка должна быть видна в профиле пользователя Seller с обновленным статусом.
- Вся информация о сделке должна быть доступна для дальнейших действий (например, подтверждение от других участников сделки).

### Примерный ход выполнения тест-кейса:

1. **Переключение кошелька TronLink на нужный кошелек Seller**:
   - Открыть приложение TronLink.
   - Переключить кошелек на нужный кошелек, указанный в сделке как Seller.

2. **Вход на сайт через TronLink**:
   - Перейти на сайт и войти через подключенный кошелек TronLink.

3. **Переход к списку сделок**:
   - Перейти в раздел, где отображаются активные сделки пользователя.

4. **Выбор нужной сделки**:
   - Найти в списке сделок ту, которая требует заявления об исполнении от Seller.
   - Выбрать эту сделку.

5. **Заявление об исполнении сделки**:
   - Нажать на кнопку для заявления об исполнении сделки.
   - Подтвердить действие в всплывающем окне TronLink, если требуется.

**Ожидаемые результаты**:
- Пользователь видит уведомление об успешном заявлении об исполнении сделки.
- Статус сделки обновляется и отображается как "исполнена" или аналогично.
- Вся информация о сделке отображается корректно и совпадает с введенными данными.
---

### Тест-кейс: Открытие диспута между Buyer и Seller

**Название**: Тестирование открытия диспута между Buyer и Seller через кошелек TronLink

**Предусловия**:
1. Установлено расширение TronLink в браузере.
2. У пользователя есть доступ к кошельку, указанному в сделке как Buyer или Seller.
3. Сделка уже создана и находится в статусе "исполнена" или "завершена".
4. Возникла необходимость в разрешении спора между Buyer и Seller.

**Шаги**:
1. Переключить кошелек TronLink на нужный кошелек (Buyer или Seller).
2. Перейти на сайт и войти через кошелек TronLink.
3. Перейти к списку завершенных или активных сделок.
4. Найти и выбрать нужную сделку, по которой возник спор между Buyer и Seller.
5. Нажать на кнопку для открытия диспута или аналогичного действия.
6. Заполнить форму для открытия диспута с необходимыми подробностями.
7. Подтвердить отправку формы или действия в всплывающем окне TronLink, если требуется.

**Ожидаемый результат**:
- Пользователь успешно открывает диспут по сделке между Buyer и Seller.
- Пользователь получает уведомление о создании диспута.
- Сделка обновляется и отображает статус "диспут открыт" или аналогичный статус.
- Вся информация о диспуте и сделке корректно отображается и сохраняется.

**Постусловия**:
- Диспут должен быть виден в профиле пользователя (Buyer или Seller) с обновленным статусом сделки.
- Стороны могут начать процесс разрешения спора на основе открытого диспута.

### Примерный ход выполнения тест-кейса:

1. **Переключение кошелька TronLink на нужный кошелек (Buyer или Seller)**:
   - Открыть приложение TronLink.
   - Переключить кошелек на нужный кошелек, указанный в сделке как Buyer или Seller.

2. **Вход на сайт через TronLink**:
   - Перейти на сайт и войти через подключенный кошелек TronLink.

3. **Переход к списку завершенных или активных сделок**:
   - Перейти в раздел, где отображаются завершенные или активные сделки пользователя.

4. **Выбор нужной сделки**:
   - Найти в списке сделок ту, по которой возник спор между Buyer и Seller.
   - Выбрать эту сделку.

5. **Открытие диспута**:
   - Нажать на кнопку для открытия диспута или аналогичного действия.
   - Заполнить форму с подробностями спора.

6. **Подтверждение отправки формы**:
   - Подтвердить отправку формы или действия в всплывающем окне TronLink, если требуется.

**Ожидаемые результаты**:
- Пользователь видит уведомление о успешном открытии диспута.
- Статус сделки обновляется и отображается как "диспут открыт" или аналогично.
- Вся информация о диспуте и сделке отображается корректно и сохраняется для дальнейшего разрешения спора.
---


### Тест-кейс: Создание сделки от Buyer/Seller с участием агентов

**Название**: Тестирование создания сделки от Buyer/Seller с участием агентов через кошелек TronLink/WalletConnect

**Предисловие**:
Для успешного создания сделки от Buyer или Seller с участием агентов необходимо убедиться в корректной работе функций сайта, связанных с использованием кошельков TronLink и WalletConnect. Эти кошельки позволяют пользователям взаимодействовать с криптовалютными сетями и выполнять транзакции на сайте без необходимости в регистрации.

**Предусловия**:
1. Установлено расширение TronLink/WalletConnect в браузере.
2. Пользователь имеет доступ к кошельку TronLink/WalletConnect.
3. Информация о Buyer/Seller, агентах и Guarantor должна быть доступна и подтверждена в системе.
4. Пользователь авторизован через кошелек TronLink/WalletConnect на сайте.

**Шаги для пользователя Buyer/Seller**:
1. Переключить кошелек TronLink/WalletConnect на нужный кошелек Buyer/Seller.
2. Перейти на сайт и войти через кошелек TronLink/WalletConnect.
3. Найти и нажать на кнопку "Create a Deal".
4. Выбрать роль Buyer или Seller в зависимости от целей тестирования и нажать "Continue".
5. Удостовериться, что информация о Buyer/Seller уже заполнена и совпадает с данными кошелька пользователя.
6. Заполнить информацию о Buyer/Seller путем ввода его кошелька, если это требуется.
7. Добавить агентов в сделку путем ввода их кошельков и суммы, которую они получат от сделки.
8. Заполнить информацию о Guarantor (кошелек, комиссия в случае его участия или отсутствия).
9. Указать стоимость сделки и условия сделки.
10. Нажать на кнопку "Create" и создать сделку.

**Ожидаемый результат для пользователя Buyer/Seller**:
- Пользователь успешно создает сделку от Buyer или Seller с участием агентов.
- Все данные о Buyer/Seller, агентах и Guarantor корректно отображаются и сохраняются в системе.
- Сделка отображается с указанием всех участников и условий сделки.

**Постусловия**:
- Созданная сделка должна быть видна в профиле пользователя Buyer/Seller с указанием всех участников и условий сделки.
- Сделка должна быть готова к дальнейшему выполнению и участию всех вовлеченных сторон.

### Примерный ход выполнения тест-кейса:

1. **Для пользователя Buyer/Seller**:
   - Переключить кошелек TronLink/WalletConnect на нужный кошелек Buyer/Seller.
   - Войти на сайт и перейти в раздел создания сделок.
   - Выбрать роль Buyer или Seller и нажать "Continue".
   - Подтвердить или заполнить информацию о Buyer/Seller и добавить агентов с указанием их кошельков и вознаграждений.
   - Заполнить информацию о Guarantor и указать стоимость и условия сделки.
   - Нажать на кнопку "Create" для создания сделки.

2. **Ожидаемые результаты**:
   - Сделка успешно создана с указанием всех участников и условий.
   - Информация о сделке корректно отображается в профиле Buyer/Seller.
   - Все данные сохранены и доступны для дальнейших действий и управления сделкой.

#### Повторить все шаги для сделки по тест-кейсам выше
---
