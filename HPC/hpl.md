# 比较方便但性能应该不好的方法
## 下载源码
```
wget https://www.netlib.org/benchmark/hpl/hpl-2.3.tar.gz
```

## 下载依赖的mpi和blas库，源里自带的包可能性能不会很好，但安装起来会很方便
```
sudo apt install libopenblas-dev
sudo apt install libopenmpi-dev
```
## 配置和编译
```
cd hpl-2.3
./configure --prefix=<the directory that you want to install>
make -j<num_threads that you compile>
make instal
```

## 运行
```
cd <the directory that you want to install>/bin
mpirun -np <PxQ> ./xhpl
```



