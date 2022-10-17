
In this project, we created a suggestion system that recommends similar movies to users when they enter the movie title. 
Suggestion systems have been used by many companies and organizations especially recently and are integrated into systems in a very useful way.

### Import
```Python
import pandas as pd
import numpy as np
```
```Python
credits = pd.read_csv("input/tmdb_5000_credits.csv")
movies = pd.read_csv("input/tmdb_5000_movies.csv")
```

![image](https://user-images.githubusercontent.com/63750425/196157513-206db7e0-efaf-4bb4-abe9-ab82085c769c.png)

```Python
def give_recomendations(title, sig=sig):
    # Get the index corresponding to original_title
    idx = indices[title]

    # Get the pairwsie similarity scores
    sig_scores = list(enumerate(sig[idx]))

    # Sort the movies
    sig_scores = sorted(sig_scores, key=lambda x: x[1], reverse=True)

    # Scores of the 10 most similar movies
    sig_scores = sig_scores[1:11]

    # Movie indices
    movie_indices = [i[0] for i in sig_scores]

    # Top 10 most similar movies
    return movies_cleaned['original_title'].iloc[movie_indices]
```
    
### Testing our content-based recommendation system with the seminal film Spy Kids
    
 ```Python
    print(give_recomendations('Avatar'))
 ```
    
![image](https://user-images.githubusercontent.com/63750425/196157863-df1144c6-fd55-4388-adc3-af0a3cbc59c6.png)
```Python
print(give_recomendations('The Dark Knight'))
```
![image](https://user-images.githubusercontent.com/63750425/196157984-16918277-c227-4f0c-b5c2-a0a587c3befd.png)
