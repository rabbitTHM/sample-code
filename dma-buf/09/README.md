## 说明
exporter-ion.c - my ion 内核驱动
ion_test.c - userspace应用程序

## 驱动编译
1. 拷贝 exporter-ion.c 文件到 linux-4.14.143/drivers/dma-buf/ 目录下。
2. 修改 linux-4.14.143/drivers/dma-buf/Makefile，添加如下内容：
```bash
obj-m += exporter-ion.o
```
3. make

最终会在 linux-4.14.143/drivers/dma-buf 目录下生成 exporter-ion.ko 文件。



## 应用程序编译
1. 拷贝整个 dmabuf-test 文件夹到 linux-4.14.143/samples/ 目录下。
2. make headers_install
3. make -C samples/dmabuf-test

最终会在 linux-4.14.143/samples/dmabuf-test/ 目录下生成 ion_test 可执行程序。
