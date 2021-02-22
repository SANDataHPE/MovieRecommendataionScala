# Movie Recommendation System
Movie Rating with Collaborative Filtering.   

### Spark Submit
```shell
spark-submit --master yarn-client --class org.apache.spark.examples.MovieRecommendation movie-recommendation-1.0-SNAPSHOT-jar-with-dependencies.jar  ratings.csv movies.csv batch_2.csv 999 <path-to-store-model>
```

### Result example
```
Got 22884377 ratings from 247753 users on 33670 movies.
Training: 13729614, validation: 4580902, test: 4573861
RMSE (validation) = 0.8258453994610284 for the model trained with rank = 8, lambda = 0.1, and numIter = 10.
RMSE (validation) = 0.8214951299457715 for the model trained with rank = 8, lambda = 0.1, and numIter = 20.
RMSE (validation) = 3.681021156174323 for the model trained with rank = 8, lambda = 10.0, and numIter = 10.
RMSE (validation) = 3.681021156174323 for the model trained with rank = 8, lambda = 10.0, and numIter = 20.
RMSE (validation) = 0.8205171634436613 for the model trained with rank = 12, lambda = 0.1, and numIter = 10.
RMSE (validation) = 0.818235041472173 for the model trained with rank = 12, lambda = 0.1, and numIter = 20.
RMSE (validation) = 3.681021156174323 for the model trained with rank = 12, lambda = 10.0, and numIter = 10.
RMSE (validation) = 3.681021156174323 for the model trained with rank = 12, lambda = 10.0, and numIter = 20.
The best model was trained with rank = 12 and lambda = 0.1, and numIter = 20, and its RMSE on the test set is 0.8185896948127657.
The best model improves the baseline by 77.77%.

============>>>> Movies recommended for User... <<<<=================
 1: 21 Up (1977)
 2: 12 Years a Slave (2013)
 3: Sympathy for Mr. Vengeance (Boksuneun naui geot) (2002)
 4: "Magic Flute
 5: Grand Illusion (La grande illusion) (1937)
 6: 28 Up (1985)
 7: Cold Fish (Tsumetai nettaigyo) (2010)
 8: Symbol (Shinboru) (2009)
 9: Never Sleep Again: The Elm Street Legacy (2010)
10: Cowboy Bebop (1998)
11: Dolls (2002)
12: Hud (1963)
13: Black Dynamite (2009)
14: "Education
15: House of Sand and Fog (2003)
16: Fireworks (Hana-bi) (1997)
17: "Old Man and the Sea
18: Joyeux Noël (Merry Christmas) (2005)
19: 35 Up (1991)
20: Red Road (2006)
21: "Queen of Versailles
22: Blue Jasmine (2013)
23: "Help
24: Garden State (2004)
25: Evil Dead II (Dead by Dawn) (1987)
26: "Apartment
27: Batman Beyond: Return of the Joker (2000)
28: "OSS 117: Cairo
29: Fist of Legend (Jing wu ying xiong) (1994)
30: Schizopolis (1996)
31: Land and Freedom (Tierra y libertad) (1995)
32: Holy Motors (2012)
33: Wallace & Gromit: The Best of Aardman Animation (1996)
34: Kids Return (Kizzu ritân) (1996)
35: Getting Any? (Minnâ-yatteruka!) (1994)
36: Adrift in Tokyo (Tenten) (2007)
37: Achilles and the Tortoise (Akiresu to kame) (2008)
38: Crawlspace (1986)
39: "Killer Inside Me
40: Starman (1984)
41: 2001: A Space Odyssey (1968)
42: "Dead Zone
43: D.A.R.Y.L. (1985)
44: My Favorite Year (1982)
45: Being There (1979)
46: Koyaanisqatsi (a.k.a. Koyaanisqatsi: Life Out of Balance) (1983)
47: "Wicker Man
48: Stardust Memories (1980)
49: Of Mice and Men (1992)
50: Batman: Mask of the Phantasm (1993)
```

### Reference  ###
* [Collaborative Filtering - spark.mllib](http://spark.apache.org/docs/latest/mllib-collaborative-filtering.html)




