## 通过系统调用 实现部分IO标准库函数

 参数及返回请参考标准IO库函数

-----

###  文件:

文件名 | 文件含义
---|---
mstdio.h mstdio.c | 头文件及函数库
test_xxx.c | xxx模式测试代码
makefile | makefile
in.txt out.txt |   要进行文件IO测试的文件
run.sh | shell脚本,包括编译及进行测试


### 已实现函数:
-----
* MFILE* mfopen(const char* const path, const char* const mode);
* int mfclose(MFILE *fp);

--------
* void mfflush(MFILE *fp);  
* MFILE* mfdopen(int fd, const char *mode);   //通过文件号创建文件指针 并返回

----------

* int mfgetc(MFILE *fp);
* int mfputc(int character, MFILE *fp);
* int mungetc(int character, MFILE *fp);    // 撤回一个字符

------

* char* mfgets(char *buff, int size, MFILE *fp); 
* int   mfputs(char *buff, MFILE *fp);

-----------
### 待完成:
* size_t mfread (void *buff, size_t size, size_t counter, MFILE *fp);
* size_t mfwirte(void *buff, size_t size, size_t counter, MFILE *fp);
* ......
