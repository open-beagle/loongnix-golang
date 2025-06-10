# Golang

<http://www.loongnix.cn/zh/toolchain/Golang/>

abi1.0 兼容 Linux 4.19 内核 UAPI，适用于 Loongnix 20、
Loongnix server 8.4、Anolis OS 8.4/8.8、UOS、
麒麟等操作系统

abi2.0 兼容 Linux 5.10 及以上内核 UAPI，适用于
OpenEuler 22.03 及以上操作系统

```bash
# 清空目录
rm -rf ./.tmp && \
mkdir -p ./.tmp && \
echo "github.com/open-beagle/loongnix-golang" > ./.tmp/README.md

# golang
# http://www.loongnix.cn/zh/toolchain/Golang/
# https://ftp.loongnix.cn/toolchain/golang/go-1.23/abi1.0/go1.23.9.linux-amd64.tar.gz
export GOLANG_MAJOR_VERSION=1.23 && \
export GOLANG_VERSION=1.23.9 && \
echo "https://ftp.loongnix.cn/toolchain/golang/go-${GOLANG_MAJOR_VERSION}/abi1.0/go${GOLANG_VERSION}.linux-amd64.tar.gz" && \
curl -sL "https://ftp.loongnix.cn/toolchain/golang/go-${GOLANG_MAJOR_VERSION}/abi1.0/go${GOLANG_VERSION}.linux-amd64.tar.gz" > ./.tmp/go${GOLANG_VERSION}.linux-amd64.tar.gz && \
mc cp ./.tmp/go${GOLANG_VERSION}.linux-amd64.tar.gz aliyun/vscode/loongarch64/go${GOLANG_VERSION}.linux-amd64.tar.gz

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
