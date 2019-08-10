### schematics
---
https://github.com/schematics/schematics

```py
from schematics.models import Model
from schematics.types import StringType, URLType
class Person(Model):
  name = StringType(required=True)
  website = URLType()
person = Person({'name': u'Joe Strummer', 'website': 'http://soundcloud.com/joestrummer'})
person.name


import json
json.dumps(person.to_primitive())


person = Person()
person.website = 'http://www.amontobin.com/'
person.validate()

person = Person()
person.name = 'Amon Tobin'
person.website = 'http://www.amontobin.com/'
person.validate()
```

```sh
coverage run --source schematics -m py.test && coverage report
```

```
```


