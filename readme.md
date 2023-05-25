# Genre annotations for movies

The file genre2movies.csv contains genre-movie tuples based on Wikidata annotations (https://www.wikidata.org/).

## Data

* Each line in genre2movies.csv represents one genre-movie tuple.
* The first entry is the genre.
* The second entry of each line is the movie name.
* There are 83,670 genre-movie tuples.

## Joining with the Movielens 20M dataset

* The movies considered are from the Movielens 20M corpus: https://grouplens.org/datasets/movielens/20m/
* The movie names in genre2movies.csv match the movie 'titles' in Movielens 20M.

## Compositions

The directory "compositions" contains movies assigned to compositions of genres. The compositions are of the form: "genre A and genre B", "genre A and not genre B", "genre A and genre B and genre C", "genre A and genre B and not genre C". These assignments have been automatically generated from genre2movies.csv. We try to generate genre-compositions that are useful, e.g., for a "genre A and genre B" composition we ensure that genre B is not a subgenre of genre A, because an interesection of a superset with a subset is identical to the subset and does not form a new concept. 

## License

This data is licensed by Google LLC under a [Creative Commons Attribution 4.0
International License](http://creativecommons.org/licenses/by/4.0/).
Users will be allowed to modify and repost it, and we encourage them to analyze
and publish research based on the data.