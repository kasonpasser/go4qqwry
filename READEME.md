# QQWRY-go

QQWRY 纯真 IP 库 golang 版

## 使用

- 下载

```bash
go get github.com/kasonpasser/go4qqwry
```

- 下载纯真的 IP 库放在 data 目录下面

通过 http://www.cz88.net/fox/ipdat.shtml 下载数据库程序（Windows 环境），执行完毕后，即可在程序安装目录找到数据库文件 qqwry.dat 即把 qqwry.dat 放到 data 目录下面为 ./data/qqwry.dat

注: qqwry.dat 需要不时的更新 因为 IP 会有变化

- 在项目中引入

```go
import (
	"github.com/kasonpasser/qqwry-go"
	"fmt"
)

func main() {

    ipinfo := qqwry.IpData.Find("223.247.9.0")
	fmt.Printf("IP:%v, Localtion:%v, Owner:%v", ipinfo.IP, ipinfo.Loc, ipinfo.Owner)
    //  IP:223.247.9.0, Localtion:安徽省池州市青阳县, Owner:电信
}
```

- TODO LIST

1、IP 库的自动更新
