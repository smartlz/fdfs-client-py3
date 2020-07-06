# fdfs-client-py3 Package

## 1. Installation

```python
pip install fdfs-client-py3==1.0.0
```

## 2. Getting Started

**upload file**：

1）upload file by name

```python
from fdfs_client.client import Fdfs_client
client = Fdfs_client('/path/to/fdfs/client.conf')
res = client.upload_by_filename('/path/to/upload_file')

# res：
# {
#   'Status': 'Upload successed.', 
#   'Local file name': '', 
#   'Storage IP': '192.168.19.131', 
#   'Group name': 'group1', 
#   'Remote file_id': 'group1/M00/00/02/wKgTg18Bnz2ASFgeAAAswnVEUA47566649', 
#   'Uploaded size': '11.19KB'
# }
```

2）upload file by content

```python
from fdfs_client.client import Fdfs_client
client = Fdfs_client('/path/to/fdfs/client.conf')
file = open('/path/to/upload_file')
res = client.upload_by_filename(file.read())

# res：
# {
#   'Status': 'Upload successed.', 
#   'Local file name': '', 
#   'Storage IP': '192.168.19.131', 
#   'Group name': 'group1', 
#   'Remote file_id': 'group1/M00/00/02/wKgTg18Bnz2ASFgeAAAswnVEUA47566649', 
#   'Uploaded size': '11.19KB'
# }
```

### 3. Author

the author is smarli，if you has some question，you can contact us by email to smartli_it@163.com。
