# Golang

<http://www.loongnix.cn/zh/toolchain/Golang/>

abi1.0 兼容Linux 4.19内核UAPI，适用于Loongnix 20、
Loongnix server 8.4、Anolis OS 8.4/8.8、UOS、
麒麟等操作系统

abi2.0 兼容Linux 5.10及以上内核UAPI，适用于
OpenEuler 22.03及以上操作系统

```bash
# 清空目录
rm -rf ./.tmp && \
mkdir -p ./.tmp && \
echo "github.com/open-beagle/loongnix-golang" > ./.tmp/README.md

# golang
# http://www.loongnix.cn/zh/toolchain/Golang/
# http://ftp.loongnix.cn/toolchain/golang/go-1.22/abi1.0/go1.22.9.linux-amd64.tar.gz
export GO_VERSION=1.22.9 && \
curl http://ftp.loongnix.cn/toolchain/golang/go-1.22/abi1.0/go$GO_VERSION.linux-amd64.tar.gz > ./.tmp/go$GO_VERSION.linux-amd64.tar.gz && \
mc cp ./.tmp/go$GO_VERSION.linux-amd64.tar.gz aliyun/vscode/loongarch64/go$GO_VERSION.linux-amd64.tar.gz

# gcc8
# https://www.loongnix.cn/zh/toolchain/GNU/
# http://ftp.loongnix.cn/toolchain/gcc/release/loongarch/gcc8/loongson-gnu-toolchain-8.3-x86_64-loongarch64-linux-gnu-rc1.6.tar.xz
export LOONGIX_GCC=gnu-toolchain-8.3
export LOONGIX_GCC_VERSION=rc1.6 && \
curl http://ftp.loongnix.cn/toolchain/gcc/release/loongarch/gcc8/loongson-$LOONGIX_GCC-x86_64-loongarch64-linux-gnu-$LOONGIX_GCC_VERSION.tar.xz > ./.tmp/loongson-$LOONGIX_GCC-x86_64-loongarch64-linux-gnu-$LOONGIX_GCC_VERSION.tar.xz && \
mc cp ./.tmp/loongson-$LOONGIX_GCC-x86_64-loongarch64-linux-gnu-$LOONGIX_GCC_VERSION.tar.xz aliyun/vscode/loongarch64/loongson-$LOONGIX_GCC-x86_64-loongarch64-linux-gnu-$LOONGIX_GCC_VERSION.tar.xz
```

## debug

```bash
tar -xvf ./.tmp/loongson-gnu-toolchain-8.3-x86_64-loongarch64-linux-gnu-rc1.6.tar.xz -C ./.tmp/
```
