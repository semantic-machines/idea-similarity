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
```json
{
"v-s:actualState": [
    {
      "data": "Текст, описывающий текущую ситуацию на производстве",
      "type": "String"
    }
  ]
}
```

### Выходные данные
Эмбеддинги можно хранить и передавать в форме строки, упакованной в JSON-объекты:
```json
{
"mnd-s:IdeaStateEmbedding": [
    {
      "data": "0.543, -0.678, 0.712",
      "type": "String"
    }
  ]
}
```
