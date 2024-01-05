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

# 1.20
export GO_VERSION=1.21.5 && \
curl http://ftp.loongnix.cn/toolchain/golang/go-1.20/abi1.0/go$GO_VERSION.linux-amd64.tar.gz > ./.tmp/go$GO_VERSION.linux-amd64.tar.gz && \
# gcc
curl hhttp://ftp.loongnix.cn/toolchain/gcc/release/loongarch/gcc8/loongson-gnu-toolchain-8.3-x86_64-loongarch64-linux-gnu-rc1.2.tar.xz > ./.tmp/loongson-gnu-toolchain-8.3-x86_64-loongarch64-linux-gnu-rc1.2.tar.xz

# 上传至S3存储
mc cp --recursive ./.tmp/ cache/vscode/loongarch64
```
