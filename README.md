SimpleXML - encoder/decoder
======================

SimpleXML is a simple and fast XML encoder/decoder for Python.

# Basic usage

# dictionary to XML

```python
import simplexml
person = {'person':{'name':'joaquim','age':15,'cars':[{'id':1},{'id':2}]}}
simplexml.dumps(person)
'<?xml version="1.0" ?><person><cars><car><id>1</id></car><car><id>2</id></car></cars><age>15</age><name>joaquim></name></person>'
simplexml.dumps(person, pretty=True)
'<?xml version="1.0" ?>\n<person>\n\t<name>joaquim</name>\n\t<age>15</age>\n\t<cars>\n\t\t<car>\n\t\t\t<id>1</id>\n\t\t</car>\n\t\t<car>\n\t\t\t<id>2</id>\n\t\t</car>\n\t</cars>\n</person>\n'

```

# XML to dictionary

```python
import simplexml
person = simplexml.loads('<?xml version="1.0" ?><person><cars><car><id>1</id></car><car><id>2</id></car></cars><age>15</age><name>joaquim</name></person>')
person['person']['name']
u'joaquim'
```

# Contributing

Fell free to contribute and send me a pull request.
