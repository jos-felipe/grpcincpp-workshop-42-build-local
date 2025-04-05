```
apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install build-essential cmake cppcheck valgrind clang lldb llvm gdb \
    && apt-get -y install autoconf automake libtool m4 autoconf-archive clang-format

# Setup ENV vars for vcpkg
export VCPKG_ROOT=/usr/local/vcpkg \
export VCPKG_DOWNLOADS=/usr/local/vcpkg-downloads
export PATH="${PATH}:${VCPKG_ROOT}"
export USERNAME=vscode

chmod +x ./install-vcpkg.sh && ./tmp/install-vcpkg.sh ${USERNAME} \
    && rm -f /tmp/install-vcpkg.sh
```