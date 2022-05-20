# Projekt z NLP na ZUM

## Dane

Wykorzystany zbiór: https://www.kaggle.com/datasets/edqian/twitter-climate-change-sentiment-dataset?resource=download

Są to tweety na temat zmiany klimatu. Dane są podzielone na 4 kategorie (neutralny, negatywny, pozytywny, news bez sentymenyu) 
z czego do projektu użyte zostały tylko tweety o sentymencie pozytywnym lub negatywnym.

Dane znajdują się w pliku: twitter_sentiment_data.csv

## Modele

W projekcie użyte zostały następujące modele:
* Bernoulli Naive Bayes
* Linear Support Vector Classification
* Regresja Logistyczna
* Sieć neuronowa o strukturze:
    - Embedding
    - Bidirectional LSTM
    - Dense

Sieć neuronowa była trenowana z różnymi wartościami parametrów - zmieniana była ilość epok (5, 10, 15) oraz ilość neuronów 
w warstwie LSTM (10, 20, 30).

Najlepsza sieć miała 30 neuronów LSTM, była trenowana przez 15 epok oraz osiągnęła wartość kosztu 0.214 i 92% dokładności. 
Zapisany model znajduje się w pliku best_model.h5.
