---
layout: page
title:  Spark
menu: Spark
---

{% include link_definitions.md %}

## PRESENTATION

[Spark](http://spark.apache.org){:target="_spark_doc"} est un système généraliste de parallélisation de données et de calculs.
 Héritier du paradigme de programmation MapReduce exploité dans [Hadoop](http://hadoop.apache.org){:target="_hadoop_doc"}, il est conçu pour être capable de traiter efficacement de très grands volumes de données.
A la différence de MapReduce, le  modèle d’exécution 
de Spark conserve les jeux de données en mémoire (distribuée), ce qui améliore massivement les performances des workflows. 
Les cas d’usage sont en conséquence beaucoup plus larges que ceux de MapReduce.

Les problèmes traités par Spark peuvent être de toute taille, en fonction de la taille du cluster qui l’exécute :

* parallélisation généraliste de codes R et Python via respectivement les modules SparkR et pySpark. 
* analyse interactive de données en quasi temps-réel, au travers de notebooks
* traitement de grands graphes de données (par exemple l’algorithme PageRank) via sa bibliothèque intégrée GraphX.

## INFRASTRUCTURE
Le cluster Spark actuel comprend 9 machines de 18 coeurs chacune, avec au total 35 TO de stockage HDFS. 

Un projet de R&D spécifique consiste à créer des clusters Spark à la demande, 
sous forme de machines virtuelles, à l’intérieur de Cloud@VD. Ces machines
virtuelles seront pré-configurées de façon à être génériques et pouvoir être 
utilisées par tous. Le projet a été financé en partie par le programme ERM 2017. 

## PROJETS SCIENTIFIQUES
Plusieurs projets de R&D sont menés sur le cluster Spark.

* Expérience d’astrophysique LSST :
connecteur Spark-[FITS](https://fits.gsfc.nasa.gov){:target="_fits_standard"} en Scala; analyse de
[données orientées 2D ou 3D](http://geospark.datasyslab.org/){:target="_geospark"} (GeoSpark, Spark3D)
; [connexion](https://www.mongodb.com/products/spark-connector){:target="_mongo_spark_connector"} entre Spark et
MongoDb

* Génomique : expérimentation sur l'analyse du génome complet.

* Informatique : déploiement de bases de données à la volée sur le
cloud via notebook Jupyter-Scala

* Ecologie : Utilisation de Spark-shell pour la parallélisation facile 
de calculs en R ; réalisation d'un cluster Spark à coût très réduit pour des conditions d'exploitation minimales.

## UTILISATION
En fonction des besoins, elle peut se faire :
* sur le cluster Spark existant
* par déploiement d'un cluster dédié.
Il faut d'abord [obtenir un compte Cloud][ServCloud], puis prendre contact pour évaluer la solution la mieux adaptée.

