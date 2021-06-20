![Github stars](https://img.shields.io/github/stars/gooderbrother/nmapIPrange.svg)
# :boom:nmapIPrange

*a liitle tool to convert nmap-ip format into string list* <br>
nmap-IPrange可以将输入的nmap格式的IPV4地址字符串转换成IP并且以string list的格式返回<br>

## :zap:例如:zap:：
***
> - 192.168.0.1 <br>
> - 192.168.0.1/24 <br>
> - 192.168.0.1-22 <br>
> - 192.168.0.* <br>
> - 192.168.0.1，192.168.2.1/24，192.168.3.1-100，192.168.4.* <br>
***

# :exclamation:usage：
```
package main

import (
	"fmt"
	"log"
	"github.com/gooderbrother/nmap-IPrange"
)

func main() {
	//注意导入的包名为nmap-IPrange，实际使用的包名为nmapIPrange
	hosts, err := nmapIPrange.Handler("192.22.168.1,10.1.1.1/26,172.16.2.*,123.123.123.1-200")
	fmt.Println(hosts)
	log.Println(err)

}
```
***
@2021-6-20  第一版本发布！！ :heart:<br>
刚学golang不久，算是个练手项目，目前更新到v0.1版本<br>
不同于隔壁大哥的iprange库，这个源码更适合人类阅读。。。 :blush:<br><br><br>
@2021-6-21  修复了一个处理星号处的小bug :heart:<br>
***

