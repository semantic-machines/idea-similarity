# **Нейросетевой модуль с языковой моделью *LLM***
## Описание работы модуля

Нейросетевой модуль на основе энкодера. Принимает от модуля ***Queue Idea Handler*** на вход текст. Далее этот текст оцифровывается, проходит несколько слоёв (свёрточных), в результате чего нейросеть учится определять характерные для текста паттерны, тематику, контекст. На выходе модели получается численный вектор, описывающий исходный текст и имеющий заданную размерность — **эмбеддинг**. Полученное векторное представление передаётся в ***Queue Idea Handler***.

<p align="center">
  <img  src="" alt='Здесь должна быть модель сети'>
</p>

## Описание архитектуры сети:

В разработке (описание слоёв, алгоритма обработки входных данных)

## Описание входных и выходных данных;

### Входные данные

Объекты такого рода поступают на вход модулю LLM:
```
v-s:actualState "Текст, описывающий текущую ситуацию на производстве" ;
```

### Выходные данные
Эмбеддинги можно хранить и передавать в форме строки, упакованной в JSON-объекты:
```
 d:emb_element_2
    rdf:type v-s:Embedding ;
    v-s:associatesWith v-s:actualState ;
    v-s:data "0.134, 0.476, -0.795" ;
  .
```

