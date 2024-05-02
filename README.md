# Python-Hadoop

A pure Python [Hadoop SequenceFile](https://hadoop.apache.org/docs/stable/api/org/apache/hadoop/io/SequenceFile.html) Reader and Writer implementation with no Java dependency.

# Installation

From source
```bash
pip install .
```

# API Documentation

```bash
# install pdoc - https://pdoc3.github.io/pdoc/
pdoc --html hadoop --skip-errors # skip errors due to broken dependency on pydoop (see below)
open html/hadoop/index.html
```

# Reading and writing SequenceFiles

[hadoop/io/SequenceFile](https://github.com/opaque-systems/sequencefile/blob/master/hadoop/io/SequenceFile.py) provides Reader, Writer and Metadata interfaces. See the examples below for more details.

# HDFS Integration

**Is currently broken as the underlying pydoop library is unmaintained**

The goal of [hadoop.pydoop.reader.SequenceFileReader](https://github.com/opaque-systems/sequencefile/blob/master/hadoop/pydoop/reader.py) is to read sequence files from HDFS. This leveraged an extra dependency on [pydoop](http://crs4.github.io/pydoop/index.html).

# Examples

Several [examples](https://github.com/opaque-systems/sequencefile/tree/master/examples) are provideed to demonstrate API usage. With the exception of the [SequenceFileReader example](https://github.com/opaque-systems/sequencefile/blob/master/examples/SequenceFileReader.py), all examples are self contained.

# Credits

This source was originally cloned from the [matteobertozzi/Hadoop python-hadoop](https://github.com/matteobertozzi/Hadoop/blob/master/python-hadoop/README) source tree and then modified for Python3 compatibility.

# License

[Apache Licence v2](https://github.com/opaque-systems/sequencefile/blob/master/LICENSE) a copy of which ships with this codebase.
