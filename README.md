# Проект "Построение модели для прогнозирования ухода клиента из банка"

## Краткое описание
Построенная модель прогнозирует, уйдёт клиент из банка в ближайшее время или нет. Вам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.<br/>
### Данные, которые подаются на вход модели:<br/>
RowNumber — индекс строки в данных<br/>
CustomerId — уникальный идентификатор клиента<br/>
Surname — фамилия<br/>
CreditScore — кредитный рейтинг<br/>
Geography — страна проживания<br/>
Gender — пол<br/>
Age — возраст<br/>
Tenure — сколько лет человек является клиентом банка<br/>
Balance — баланс на счёте<br/>
NumOfProducts — количество продуктов банка, используемых клиентом<br/>
HasCrCard — наличие кредитной карты<br/>
IsActiveMember — активность клиента<br/>
EstimatedSalary — предполагаемая зарплата<br/>

### *На выходе* модель выдает значение **0 или 1**: где 0 - клиент не уйдет из банка, 1 - клиент уйдет из банка.

## Содержание проекта
<div class="toc"><ul class="toc-item"><li><span><span class="toc-item-num">1&nbsp;&nbsp;</span>Подготовка данных</span><ul class="toc-item"><li><span><span class="toc-item-num">1.1&nbsp;&nbsp;</span>Описание данных</span></li><li><span><span class="toc-item-num">1.2&nbsp;&nbsp;</span>Заполнение пропусков</span></li><li><span><span class="toc-item-num">1.3&nbsp;&nbsp;</span>Подготовка данных</span></li><li><span><span class="toc-item-num">1.4&nbsp;&nbsp;</span>Вывод</span></li></ul></li><li><span><span class="toc-item-num">2&nbsp;&nbsp;</span>Исследование задачи</span><ul class="toc-item"><li><span><span class="toc-item-num">2.1&nbsp;&nbsp;</span>Вывод</span></li></ul></li><li><span><span class="toc-item-num">3&nbsp;&nbsp;</span>Борьба с дисбалансом</span><ul class="toc-item"><li><span><span class="toc-item-num">3.1&nbsp;&nbsp;</span>Уменьшение выборки</span></li><li><span><span class="toc-item-num">3.2&nbsp;&nbsp;</span>Увеличение выборки</span></li><li><span><span class="toc-item-num">3.3&nbsp;&nbsp;</span>Изменение порога классификации</span></li><li><span><span class="toc-item-num">3.4&nbsp;&nbsp;</span>Вывод</span></li></ul></li><li><span><span class="toc-item-num">4&nbsp;&nbsp;</span>Тестирование модели</span><ul class="toc-item"><li><span><span class="toc-item-num">4.1&nbsp;&nbsp;</span>Вывод</span></li></ul></div>

## Рассматриваемые модели
RandomForestClassifier, LogisticRegression, DecisionTreeClassifier

## Результаты

Лучшая модель-Случайное дерево с гиперпараметрами: max_depth=9, n_estimators=96 (random_state=12345)<br/>
Метод борьбы с дисбалансом - изменение порога классификации - 0.35<br/>

Результаты модели на валидационной выборке: точность = 0.66; полнота = 0.55; f1 = 0.6<br/>
Результаты модели на тестовой выборке: точность = 0.7; полнота = 0.59; f1 = 0.64<br/>

AUC-ROC = 0.87 - на 0.37 больше случайном модели (0.5). Является показателем очень хорошего качества модели<br/>
