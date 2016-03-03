 sysstat
 - sudo apt-get -y install sysstat
 - cat /etc//etc/cron.d/sysstat     开发环境修改每分钟一次。

 [Reference](http://www.leonardoborda.com/blog/how-to-configure-sysstatsar-on-ubuntudebian/)
- sar -q   (CPU任务书和繁重程度)
- sar -p  (CPU)

- sar -r (内存占用百分比)
- sar -B (内存)
- sar -W  （swap 进出， 交换程度）

- sar -b (IO, 每秒IO请求次数，块的读取）
- sar -d  (IO))
- sar -n DEV (network)

# fio
磁盘IO极限性能
iops, 高的，作为mysql服务器
[Reference](http://www.pubyun.com/blog/announce/%E6%B5%8B%E8%AF%95%E4%BA%91%E4%B8%BB%E6%9C%BA%E7%9A%84%E7%A3%81%E7%9B%98io%E6%80%A7%E8%83%BD/)
下面是我使用fio测试我的硬盘结果：

1. 顺序读 bw = 90.26 Mb/s, iops = 90
2. 顺序写 bw = 60.77 Mb/s, iops = 60
3. 随机读 bw = 679 kb/s, iops = 169
4. 随机写 bw = 775.28 kb/s, iops = 193

- bw: 磁盘的吞吐量，这个是顺序读写考察的重点
- iops: 磁盘的每秒读写次数，这个是随机读写考察的重点

