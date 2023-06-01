# Golang

http://www.loongnix.cn/zh/toolchain/Golang/

2022-12-27 Golang 1.20.2 版本发布

龙芯发布的1.20.2版本Golang，专门用于编译Linux内核低于5.19的应用

```bash
# 清空目录
rm -rf ./.tmp && \
mkdir -p ./.tmp && \
echo "gitlab.wodcloud.com/kubernetes/golang:release-loongnix" > ./.tmp/README.md

# 1.20
export GO_VERSION=1.20.2 && \
curl http://ftp.loongnix.cn/toolchain/golang/go-1.20/abi1.0/go$GO_VERSION.linux-amd64.tar.gz > ./.tmp/go$GO_VERSION.linux-amd64.tar.gz

# gcc
curl http://ftp.loongnix.cn/toolchain/gcc/release/loongarch/gcc8/loongson-gnu-toolchain-8.3.novec-x86_64-loongarch64-linux-gnu-rc1.1.tar.xz > ./.tmp/loongson-gnu-toolchain-8.3.novec-x86_64-loongarch64-linux-gnu-rc1.1.tar.xz

# 上传至S3存储
mc cp --recursive ./.tmp/ cache/vscode/loongarch64
```