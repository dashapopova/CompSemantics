## Домашнее задание 1

**Дедлайн: 26 февраля 14.40**

Работы присылайте на daria.ryzhova@mail.ru, daschapopowa@gmail.com и sashonet23.00@gmail.com

Постройте взвешенный граф, узлами которого будут все гипонимы синсета X (выберите такой Х, у которого не меньше 30 гипонимов, но не синсет ‘travel.v.01’), а ребра между ними будут отражать частоту колексификации, т.е. будут устанавливаться в том случае, если хотя бы в одном языке из MultiWordNet найдется слово, которое относится к обоим синсетам; толщина ребра должна отражать количество таких слов. (Иными словами, получится граф, аналогичный графам в CLICS, но на другом материале). 


| баллы        | задачи          |
| ------------- |-------------| 
| 2| извлечены все гипонимы синсета Х (выберите такой Х, у которого не меньше 30 гипонимов, и НЕ travel.v.01)| 
| 1.5| построен граф, где узлы -- гипонимы синсета X, а рёбра отражают колексификацию узлов|   
| 1| толщина ребра отражает частоту колексификации|   
| 0.5       | сколько получилось связных компонент?         |
| 1        | определён коэффициент ассортативности и плотность графа          |
| 2        | как распределились (взвешенные) степени узлов? какие узлы оказались центральными (попробуйте несколько метрик, например, degree centrality и eigencentrality)? прокомментируйте результаты           |
| 2       | разбейте граф на сообщества (поиграйте с несколькими алгоритмами) и прокомментируйте результаты         |
