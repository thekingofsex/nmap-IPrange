# nmapIPrange

nmapIPrange可以将输入的nmap格式的IPV4地址字符串转换成IP并且以string list的格式返回

##例如：
***
> 192.168.0.1 <br>
> 192.168.0.1/24 <br>
> 192.168.0.1-22 <br>
> 192.168.0.* <br>
> 192.168.0.1，192.168.2.1/24，192.168.3.1-100，192.168.4.* <br>
***

# usage：
```
package main

import (
	"fmt"
	"log"
	"test/nmapIPrange"
)

func main() {

	hosts, err := nmapIPrange.Handler("192.22.168.1,10.1.1.1/26,172.16.2.*,123.123.123.1-200")
	fmt.Println(hosts)
	log.Println(err)

}
```
