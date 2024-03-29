# Домашнее задание 2. Кластеризация векторного пространства

## Входные данные
Глагол и список существительных, которые часто занимают позицию субъекта или объекта при этом глаголе. При каждой паре "глагол + существительное" указано, сколько раз они встретились вместе в основном подкорпусе НКРЯ.
> Существительные подбирались следующим образом: в автоматически размеченном и дизамбигуированном основном подкорпусе НКРЯ выделялись случаи, когда за существительным в номинативе или аккузативе непосредственно следует искомый глагол и, наоборот, когда за искомым глаголом непосредственно следует существительное в номинативе или аккузативе; все такие существительные собраны в единый частотный список, из которого в итоговый набор попали первые 100.  

У каждого участника НИСа свой глагол со своим набором существительных. [Здесь](https://docs.google.com/spreadsheets/d/1l9qsuL3HiSM67qFEmj1z8vrUBmdINy_4V_lIRGzI5Vc/edit?ts=603e9827#gid=821448885) (вкладка Дз 2) 
можно посмотреть, какой датасет ваш, а сами датасеты лежат [тут](https://github.com/dashapopova/CompSemantics/tree/main/HWs/hw2_input%20data).

## Задача
1. Взять любую предобученную векторную модель с rusvectores.org и извлечь оттуда вектор для глагола и каждого существительного из своего списка.
2. На основе этих векторов построить репрезентацию для каждой пары «глагол + существительное» с помощью простой аддитивной модели композиции.
> Примечание. Если каждый вектор – это объект типа array в модуле numpy, то можно просто сложить эти два объекта, используя оператор «+».
3. Собрать все векторные представления пар в единую матрицу и кластеризовать их двумя способами:
* методом иерархической кластеризации;
* методом К-средних, см. [хендаут](https://github.com/dashapopova/CompSemantics/blob/main/Clustering/CompSemClustering.ipynb).<br/>
В первом случае количество кластеров определяется автоматически (но задается значение порога t), во втором случае количество кластеров нужно задать вручную.
Возьмите то значение каждого из этих параметров, которое вам кажется наиболее удачным и обоснуйте свое решение (одного-двух предложений будет вполне достаточно).
Все остальные параметры в обоих случаях можно не менять и использовать настройки по умолчанию.
4. Для каждого кластера определите центр и выберите по три элемента, наиболее к нему близких (по метрике косинусной близости).
Центр можно определить как среднее арифметическое среди всех элементов кластера по каждому измерению (например, с помощью метода numpy.mean).
Кластеры, размер которых не превышает двух элементов, не учитывайте совсем.
7. Оформите результат в виде набора групп из трех словосочетаний, например:  

идти_дождь, идти_снег, идти_град <br/>
идти_часы, идти_время, идти_урок <br/>
…  

6. Подготовьте очень краткий (буквально на абзац) анализ результатов. Однородные ли, на ваш взгляд, получились группы? Все ли значения глагола удалось «поймать» и проиллюстрировать?

## NB!
На основе этого задания можно написать итоговое эссе. Для этого можно пойти по одному из следующих путей: обсудить возможные варианты строгой оценки качества полученных результатов; предложить свою модификацию алгоритма; обсудить варианты выбора количества кластеров для алгоритма К-средних; поэкспериментировать с различными параметрами (взять другие модели с rusvectores; попробовать другие модели композиции; поменять настройки алгоритма кластеризации и т.п.) и обсудить результат. А можно предложить свой вариант развития сюжета. 

## Как и когда сдавать
Выполненную работу нужно прислать Саше К. (sashonet23.00@gmail.com), Даше П. (daschapopowa@gmail.com) и Даше Р. (daria.ryzhova@mail.ru) - всем троим! - **до 23:59 6 апреля**. После дедлайна работу можно будет сдать, но со штрафом: каждый день после дедлайна отнимает 2 балла от итоговой оценки. По уважительной причине дедлайн можно перенести в индивидуальном порядке. Для этого напишите нам, и мы с вами обо всем договоримся.  

## Критерии оценивания
Каждый элемент задания имеет свой вес:
* пункт 1 - 1 балл
* пункт 2 - 1 балл
* пункт 3 - 4 балла (по одному за метод и по одному за обоснование выбора порогового значения для иерархической кластеризации и числа кластеров для метода К-средних)
* пункт 4 - 2 балла (1 балл - определение центров, 1 балл - выбор трех элементов, наиболее к ним близких)
* пункт 5 - 1 балл
* пункт 6 - 1 балл
