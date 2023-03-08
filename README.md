Big Data
========

This project aims to predict video game sales using machine learning algorithms in MLlib. 
The prediction models are trained using historical video game sales data, and the predictions are made based on the features of the games, such as their genre, platform, and publisher. The data is streamed using Kafka server and managed using Zookeeper. The goal is to develop a predictive model that can accurately predict video game sales and provide insights into the factors that influence video game sales. This project can be useful for game developers, publishers, and investors who want to make data-driven decisions based on sales predictions.

## Install & Dependencies
- xgboost
- pyarrow
- pyspark
- confluent_kafka

## Dataset
| Dataset | Download |
| ---     | ---   |
| Kaggle - Video Games Sales Dataset | https://rb.gy/z0syad |

## Use

  Launch Kafka server and zookeeper:

  1. All tasks in this exercise are performed from Kafka home directory. You may want to define an alias for the quick jump to this directory each time you start a Terminal: 
  ```
  alias cdk='cd /usr/local/kafka/kafka_2.13-3.2.1
  ```
  2. From a new Terminal: Start ZooKeeper
  ```
  bin/zookeeper-server-start.sh   config/zookeeper.properties &
  ```
  3. From a new Terminal: Start Kafka server
  ```
  bin/kafka-server-start.sh   config/server.properties &
  ```
  4. run main program
  ```
  python Big_Data.ipynb
  ```

## Directory Hierarchy
```
|—— data
|    |—— Video_Games_Sales.csv
|    |—— Video_Games_Sales_Fixed.csv
|—— Big Data.ipynb
|—— results
|    |—— 1981.csv
|    |—— 1982.csv
|    |—— 1983.csv
|    |—— 1984.csv
|    |—— 1985.csv
|    |—— 1986.csv
|    |—— 1987.csv
|    |—— 1988.csv
|    |—— 1989.csv
|    |—— 1990.csv
|    |—— 1991.csv
|    |—— 1992.csv
|    |—— 1993.csv
|    |—— 1994.csv
|    |—— 1995.csv
|    |—— 1996.csv
|    |—— 1997.csv
|    |—— 1998.csv
|    |—— 1999.csv
|    |—— 2000.csv
|    |—— 2001.csv
|    |—— 2002.csv
|    |—— 2003.csv
|    |—— 2004.csv
|    |—— 2005.csv
|    |—— 2006.csv
|    |—— 2007.csv
|    |—— 2008.csv
|    |—— 2009.csv
|    |—— 2010.csv
|    |—— 2011.csv
|    |—— 2012.csv
|    |—— 2013.csv
|    |—— 2014.csv
|    |—— 2015.csv
|    |—— 2016.csv
```
## Code Details

### Tested Platform
- software
  ```
  OS: Ubuntu
  Python: 3.10.0
  XGBoost: 1.7.0
  ```
- hardware
  ```
  CPU: Intel(R) Xeon(R) CPU E5-2687W v4 @ 3.00GHz
  GPU: NVIDIA TESLA P40-2Q (2GB)
  ```

## References
- paper-1: MLlib: Machine Learning in Apache Spark, [https://www.jmlr.org/papers/volume17/15-237/15-237.pdf]
- paper-2: XGBoost: A Scalable Tree Boosting System, [https://arxiv.org/pdf/1603.02754.pdf]
