## 概述
oslo.config 是用于从命令行或配置文件解析配置参数的框架，来自于 OpenStack社区。作为 oslo 项目的子项目，可以通用在任何 python 程序中。

```
#!/usr/bin/python
# test_oslo_config.py
from oslo_config import cfg
from oslo_config import types

PortType = types.Integer(1, 65535)

common_opts = [
    cfg.StrOpt('bind_host',
            default='0.0.0.0',
            help='IP address to listen on.'),
    cfg.Opt('bind_port',
            type=PortType,
            default=9292,
            help='Port number to listen on.')
]
```

##快速开始
###1.安装
```
# pip install oslo.config
```
###2. 定义参数
```

#!/usr/bin/python
# test_oslo_config.py
from oslo_config import cfg
from oslo_config import types


PortType = types.Integer(1, 65535)


common_opts = [
    cfg.StrOpt('bind_host',
            default='0.0.0.0',
            help='IP address to listen on.'),
    cfg.Opt('bind_port',
            type=PortType,
            default=9292,
            help='Port number to listen on.')
]
```

