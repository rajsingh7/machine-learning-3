
# Notes

## Definição de **Naive Predictor**

O Naive Predictor deve funcionar como um benchmark na avaliação dos modelos e para a comparação com outros modelos.
Em nosso caso, o Naive Predictor pode ser assumir que os indivíduos ganham menos que 50K, dado que a maior parte dos indivíduos se encontra nessa classificação.
Dessa maneira, temos uma referência em acurácia para este preditor.

## Fórmula da acurácia

$$ F_{\beta} = (1 + \beta^2) \cdot \frac{precision \cdot recall}{\left( \beta^2 \cdot precision \right) + recall} $$

onde

**acurácia**: mede o quão frequentemente um preditor faz uma previsão correta

**precisão**: mede a proporção de indivíduos que foram classificados como >50K e que ganham >50K

`[True Positives/(True Positives + False Positives)]`

**recall** *(senitivity)*: mede a proporção de indivíduos que ganham acima de 50K e que foram classificados como >50K

`[True Positives/(True Positives + False Negatives)]`

Quando a classe que se deseja classificar os indivíduos não é representativa na população, por exemplo, representa 5%, a utilização de precisão e recall é importante porque a precisão seria alta, pois a maior parte seria classificada corretamente, mas o recall seria baixo e usando ambos no score F atacamos este problema.

## Dataset

https://archive.ics.uci.edu/ml/datasets/Census+Income