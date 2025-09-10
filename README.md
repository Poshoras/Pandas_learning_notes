# 保持文件地址统一
Vscode和jupyter不完全一样，并不是把代码和表格放到一起就可以运行，要手动将代码的地址调整到表格的文件夹中。

下面是一个调整代码地址的示例：


import os
os.chdir(os.path.dirname(__file__))

import pandas as pd
df = pd.read_excel('plan.xlsx')
print(df.head())



那如何自主调整筛选范围呢？
```python
import pandas as pd
df  = pd.read_excel('plan.xlsx',sheet = '****',header = 1)<br>
header=1意为把第二行当作读取的第一行（原因可能是第一行有太多废话了）
