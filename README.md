# generate mongo models automatically with `mongoengine`

### Installation

```bash
python -m pip install mongo-dynamic-models
```

### Usage

```python
from mongo_dynamic_models import MongoModels

# 指定MongoDB数据库URI
uri = 'mongodb://USER:PASSWORD@HOST_OR_IR:PORT/DB'

# 实例化对象，自动生成动态模型
models = MongoModels(uri)

# 显示集合列表
print(models.collection_names)

# 以属性方式，引用动态模型
print(models.users.objects)

# 以索引方式，引用动态模型
print(models['users'].objects)
```