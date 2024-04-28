**1. Przegląd danych:**

 * **Podaj liczbę filmów Sci-Fi**
        <br>
        `980`
  ***    
 * **Pokaż rozkład ocen komedii**
      <br>
     ![obraz](https://github.com/kkarolina71/ML_2024/assets/58952087/2935848a-3215-4f6a-81ae-8f33c6b51087)
***
 * **Podaj średnią ocen wszystkich filmów akcji oraz 3 filmy najwyżej ocenianych**
      <br>
      *Średnia ocen wszystkich filmów akcji: 3.45*


   ***Najwyżej oceniane 3 filmy*** 
   
|             Title              | Bayesian Average |
|--------------------------------|------------------|
| Shawshank Redemption, The (1994) |       4.39       |
|       Godfather, The (1972)      |       4.24       |
|         Fight Club (1999)        |       4.23       |



***Najwyżej oceniane 3 filmy akcji*** 
| Title | Bayesian Average |
|-----------------------------|------------------|
| Fight Club (1999) | 4.19 |
| Star Wars: Episode IV - A New Hope (1977) | 4.16 |
| Star Wars: Episode V - The Empire Strikes Back (1980) | 4.13 |

***
**2. System rekomendacyjny**

   * **Zbuduj system na podstawie algorytmu SVD oraz kNNwithMeans**
   * **Czym różni się algorytm kNN with means od standardowego kNN?**<br>

        **Standardowy kNN:** Standardowy algorytm kNN klasyfikuje nowy punkt danych na podstawie etykiety klasy większościowej jego k najbliższych sąsiadów w szkoleniowym zbiorze danych. Wykorzystuje metrykę odległości do pomiaru podobieństwa między nowym punktem danych a istniejącymi punktami danych. Wartość k jest hiperparametrem, który możemy wybrać na podstawie charakterystyki danych i danego problemu
        
        **kNN ze średnimi:** Jest to odmiana algorytmu kNN często używanego w filtrowaniu kolaboracyjnym w systemach rekomendacji. Kluczową różnicą jest to, że uwzględnia on średnią ocenę każdego użytkownika (lub elementu) podczas dokonywania prognozy. Pomaga to skorygować użytkowników, którzy zawsze wystawiają wysokie lub niskie oceny. Na przykład, jeśli użytkownik ma tendencję do surowego oceniania filmów, 4-gwiazdkowa ocena od niego może być równoważna 5-gwiazdkowej ocenie od bardziej łagodnego użytkownika. Odejmując średnią ocenę użytkownika przed dokonaniem prognozy, a następnie dodając ją z powrotem, algorytm kNN ze średnimi może tworzyć dokładniejsze rekomendacje.
        
        **Podsumowując** , podczas gdy oba algorytmy opierają się na koncepcji znajdowania "sąsiadów" w danych, standardowy algorytm kNN jest zwykle używany do zadań klasyfikacji lub regresji, podczas gdy kNN ze średnimi jest często używany w systemach rekomendacji w celu uwzględnienia stronniczości użytkownika. 


   * **Wykorzystaj metodę hiperparametryzacji GridSearch do wyboru liczby sąsiadów od 2-6** <br>
     Hiperparametryzacja wskazała na 6 sąsiadów.
   * **W ocenie metod wykorzystaj walidację krzyżową** <br>
     Algorytm `SVD` uzyskał lepsze wyniki.

**3. Podaj rekomendacje po obejrzeniu filmu: Jumanji  oraz Flint**


### SVD

| Rekomendacje dla Jumanji (1995) (Adventure, Children, Fantasy): | |
|---|---|
| Casper (1995) | Adventure, Children |
| Mrs. Doubtfire (1993) | Comedy, Drama |
| Santa Clause, The (1994) | Comedy, Drama, Fantasy |
| Hudsucker Proxy, The (1994) | Comedy |
| Mask, The (1994) | Action, Comedy, Crime, Fantasy |
| Mr. Holland's Opus (1995) | Drama |


| Rekomendacje dla Flint (2017) (Drama): | |
|---|---|
| Fly, The (1986)| Drama, Horror, Sci-Fi, Thriller |
| Glory Daze (1995) | Drama |
| Extreme Days (2001) | Action, Adventure, Comedy, Drama |
| Fur: An Imaginary Portrait of Diane Arbus (2006) | Drama, Fantasy, Romance |
| Twilight Saga: Eclipse, The (2010) | Fantasy, Romance, Thriller, IMAX |
| Phantasm III: Lord of the Dead (1994) | Horror |


***
### kNNWithMeans

| Rekomendacje dla Jumanji (1995) (Adventure, Children, Fantasy): 	 | |
|---|---|
| Mrs. Doubtfire (1993) | Comedy, Drama |
| Mask, The (1994) | Action, Comedy, Crime, Fantasy |
| Back to the Future (1985) | Adventure, Comedy, Sci-Fi |
| Liar Liar (1997) | Comedy |
| True Lies (1994) | Action, Adventure, Comedy, Romance, Thriller |
| Casper (1995) | Adventure, Children |



| Rekomendacje dla Flint (2017) (Drama): | |
|---|---|
| Toy Story (1995) | Adventure, Animation, Children, Comedy, Fantasy |
| Grumpier Old Men (1995) | Comedy, Romance |
| Heat (1995) | Action, Crime, Thriller |
| Seven (a.k.a. Se7en) (1995) | Mystery, Thriller |
| Usual Suspects, The (1995) | Crime, Mystery, Thriller |
| From Dusk Till Dawn (1996) | Action, Comedy, Horror, Thriller |
