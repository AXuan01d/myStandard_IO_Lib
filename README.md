## 通过系统调用 实现部分IO标准库函数
参数及返回请参考标准IO库函数
###已实现函数:

* MFILE* mfopen(const char* const path, const char* const mode);
* int mfclose(MFILE *fp);

--------
* void mfflush(MFILE *fp);  
* MFILE* mfdopen(int fd, const char *mode);   //通过文件号创建文件指针 并返回

----------
* int mfgetc(MFILE *fp);
* int mfputc(int character, MFILE *fp);
* int mungetc(int character, MFILE *fp);

------
* char* mfgets(char *buff, int size, MFILE *fp); 
* int   mfputs(char *buff, MFILE *fp);

-----------
### 待完成:
* size_t mfread (void *buff, size_t size, size_t counter, MFILE *fp);
* size_t mfwirte(void *buff, size_t size, size_t counter, MFILE *fp);

