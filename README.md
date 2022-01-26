# yandex-eat-hackathon

### The problem of predicting the proportion of multi-orders.

#### Description of the task.

In one of the cities, Яндекс.Еда decided to try to deliver orders from its restaurants not one by one, but by combining them together into a multi-order.
That is, a courier arriving at a restaurant could receive not one, but two orders in the same restaurant,
which had to be delivered to customers in turn.
How to combine orders is decided by an algorithm that is unknown to us.

We decided to test run with a sample of A restaurant brands in the same city and got the results.
For further scaling, we formed a sample of restaurant brands B,
but you need to evaluate the effect before starting the launch of such a scheme.

So, based on the data in sample A, estimate what proportion of orders in sample B could be delivered using multiorders in all cities where restaurants in sample B are represented?
A multi-order consists of a maximum of two orders.

Multiorder_Yandex.ipynb -
IPython notebook with the presented solution for predicting the proportion of multi-orders.
In the course of the solution, the analysis of samples A and B was carried out, a visual analysis of the parameters of samples with and without multi-orders was carried out.
A heuristic has been built to predict the possibility of combining two orders of the closest time in a multi-orders.
A classifier has been built,
predicting the possibility of combining items into one multi-order.
The total proportion of multiorders in group B is 32%.


### Задача предсказания доли мультизаказов.

#### Описание задачи.

В одном из городов Яндекс.Еда решила попробовать доставлять заказы из своих ресторанов не по одному, а объединяя их вместе в мультизаказ. 
То есть, курьер, приходя в какой-либо ресторан мог получить не один, а два заказа в одном и том же ресторане, которые должен был по очереди доставить клиентам.
Каким образом объединить заказы решает алгоритм, который нам неизвестен.

Мы решили тестово запуститься с выборкой брендов ресторанов A в одном городе и получили результаты.
Для дальнейшего масштабирования сформировали выборку брендов ресторанов B, но нужно оценить эффект перед стартом запуском такой схемы. 

Итак, по данным выборки А оцените какая доля заказов выборки B могла бы доставляться с помощью мультизаказов во всех городах, где представлены рестораны выборки B?
Мультизаказ состоит максимум из двух заказов.

Multiorder_Yandex.ipynb - ноутбук с представленным решением по предсказанию доли мультизаказов.
В ходе решения проведен анализ выборок А и В, проведен визуальный анализ параметров выборок с мультизаказами и без. 
Построена эвристика для предсказания возможности объединения двух ближайших по времени заказов в мультизака.
Построен классификатор, предсказывающий возможность объединения позиций в один заказ. 
Итоговая доля мультизаказов в группе В равна 32%.


data.xlsx - исходные данные со следующими полями:<br/>
order_created_datetime - дата создания заказа;<br/>
brand_name - группа ресторанов;<br/>
rest_id - уникальный идентификатор ресторана;<br/>
batched_with_order_id - идентификатор заказа, с которым объединяется текущий;<br/>
order_id - идентификатор заказа;<br/>
first_in_multiorder_flg - первый ли заказ в мультизаказе;<br/>
courier_id - идентификатор курьера;<br/>
order_item_cnt - кол-во позиций в заказе;<br/>
city_id - идентификатор города.<br/>

data.xlsx - data with the following fields:<br/>
order_created_datetime - order creation date;<br/>
brand_name - restaurant group;<br/>
rest_id - unique identifier of the restaurant;<br/>
batched_with_order_id - order ID,<br/>
with which the current is merged;<br/>
order_id - order identifier;<br/>
first_in_multiorder_flg - is the first order in a multiorder;<br/>
courier_id - courier identifier;<br/>
order_item_cnt - number of items in the order;<br/>
city_id - city identifier.
