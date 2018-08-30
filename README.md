# ls-cpuinfo
显示CPU信息



## 查看CPU型号
```sh
cat /proc/cpuinfo | grep name | cut -f2 -d: | uniq -c
```

## 查看物理CPU个数
```sh
cat /proc/cpuinfo| grep "physical id"| sort| uniq| wc -l
```

## 查看每个物理CPU中core的个数(即核数)
```sh
cat /proc/cpuinfo| grep "cpu cores"| uniq
```

## 查看逻辑CPU的个数
```sh
cat /proc/cpuinfo| grep "processor"| wc -l
```
