# Pyspark_Massive_Data_Analysis

## Massive Data Analysis for 500000+ data using pyspark api

## 1. page rank algorithm
![Variable Declaration](/pyspark_img/pagerank.jpeg)
## 2. Kmeans clustering algorithm
* c1:randomly choose center 
* c2:choose long-distance points
* k = 10 keep iteration
![Variable Declaration](/pyspark_img/kmeans_algo.png
)
![Variable Declaration](/pyspark_img/kmeanss.png)
## Result
## i.Euclidean distance
![Variable Declaration](/pyspark_img/Euclidean.png)
以cost來來看，c2選擇「互相距離遠」的點為中⼼心點的⽅方式比c1隨機選擇中⼼心點的⽅方法好，因為 Euclidean distance是受平⽅方影響，在多維的資料中若若有某⼀一維離中⼼心點偏差值特別⼤大，容易易造成 distance與cost值特別⼤大，因此對c1⽅方法來來說，若若沒有盡量量選互相距離⼤大的點座為中⼼心點，在圖中 會很容易易有些點附近都沒有中⼼心點(中⼼心都距離他們很遠)，偏差值會太⼤大⽽而主導距離跟cost值 ; c2的⽅方法較不會有極端值的出現，因此cost會較⼩小。 還有如果⼀一開始使⽤用c1⽅方法選擇的中⼼心點之間距離較近，在分類時容易易把離他們較近、本該在同⼀一 群的點分散到這些距離較近的中⼼心點之中。若若⼀一開始就選擇互相距離遠的中⼼心點，能確保他們周圍 較近的點⼀一開始可分進同⼀一類，這影響到了了後續分類表現以及percentage improvement，由此可觀 察到c2的表現較好。
## ii.Manhattan distance
![Variable Declaration](/pyspark_img/manhattan.png)
以cost來來看，c1隨機選擇中⼼心點的⽅方法比c2選擇「互相距離遠」的點為中⼼心點的⽅方式好。c1⽅方法⼀一 開始的cost就比c2⽅方法⼩小，因為在多維資料中，Manhattan distance是受各維度影響，不會有偏差 值被特別放⼤大的問題，算出的是各維度差的總和，離中⼼心近的點跟遠的點的影響⼒力力是同等的。 比起c1周圍有可能有許多距離和較⼩小的點，⽤用c2可能會導致中⼼心點太過分散，雖然可能沒有偏差特 別⼤大的點，導致c2⽅方法的distance跟cost比較⼤大。
## 3.matrix product
![Variable Declaration](/pyspark_img/matrix-multiplication.png)
