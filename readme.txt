python py_innodb_page_info.py /var/lib/mysql/test/tt.ibd -v
page offset 00000000, page type <File Space Header>
page offset 00000001, page type <Insert Buffer Bitmap>
page offset 00000002, page type <File Segment inode>
page offset 00000003, page type <B-tree Node>, page level <0000> ---叶子节点
page offset 00000000, page type <Freshly Allocated Page>
page offset 00000000, page type <Freshly Allocated Page>
Total number of page: 6: 
Freshly Allocated Page: 2
Insert Buffer Bitmap: 1
File Space Header: 1
B-tree Node: 1
File Segment inode: 1




解释：
Total number of page: 总页数
Freshly Allocated Page:可用页
Insert Buffer Bitmap:插入缓存位图页
Insert Buffer Free List:插入缓存空闲列表页
B-tree Node:数据页
Uncompressed BLOB Page:二进制大对象页，存放溢出行的页，即溢出页
上面得到的信息是表初始化大小为96K，他是有 Total number of page * 16 得来的。1个数据页，2个可用页面。