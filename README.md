<p align="center">
  <a href="" rel="noopener">
 <img width=500px height=100px src="https://docs.delta.io/latest/_static/delta-lake-logo.png" alt="Project logo"></a>
</p>

<h3 align="center">Delta lake is an open-source project that enables building a Lakehouse architecture on top of existing storage systems such as S3, ADLS, GCS, and HDFS.</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

## 📝 Table of Contents

- [About](#about)
- [Upserts Delta Lake](#deltalake)
- [Usage](#usage)
- [Built Using](#built_using)
- [Authors](#authors)

## 🧐 About <a name = "about"></a>

This project aims to make a simple etl processing, using pyspark with the deltalake framework. The work of pyspark will consume a filesystem titled landing-zone with files in json format. We will use some time travel techniques, writing in delta format for table management control and much more.

## 🔧 Upserts Delta Lake <a name = "deltalake"></a>

![image](https://i.ytimg.com/vi/R4f6SKOetB4/maxresdefault.jpg)

### Prerequisites

```
Spark: 3.1.2 https://spark.apache.org/downloads.html
```

## 🎈 Usage <a name="usage"></a>

## notebook/deltalake-example.ipynb

This project comes with the objective of clarifying, in a practical way, how the Delta Lake Upserts logic works and how we can "kill" Data WareHouse with the new and modern Lake House Architecture, for this I have made available a jupyter notebook, in which we read data in json format, which is related to users of a system. Our main goal is to read these files in Json format and convert them to a Delta Table. After that we can access metadata that is generated inside a directory called _delta_log, which we can access through the DeltaTable.forPath method. After instantiating the Delta Table, we managed to merge the new data using whenMatchedUpdateAll using the condition that we are going to compare and finally update our Delta Table.

![image](https://miro.medium.com/max/1400/0*5XnRRdbrbuuNGFzJ.png)

## ⛏️ Built Using <a name = "built_using"></a>

- [Pyspark](https://spark.apache.org/docs/latest/api/python/index.html) - 3.1.2
- [Deltalake](https://docs.delta.io/latest/quick-start.html) - 1.0.0

## ✍️ Authors <a name = "authors"></a>

- [@carlosbpy](https://github.com/carlosbpy) - Idea & Initial work