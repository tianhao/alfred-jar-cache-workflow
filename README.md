# Java Jar 包缓存管理
(Alfred Jar Cache workflow）
---

**场景:**

* 查看本地是否有缓存 jar 包;
* maven 或 gradle 下载jar包出错时(jar 包大小 0K)用来删除错误的jar包;
* 想重新下载指定版本的jar包，要先删除本地缓存，使用 nexus 私服可以不修改版本号发布新版本，这时要删除本地缓存才会重新下载。

**查找缓存功能:**

* `jarm 关键字...` 查找Maven jar包缓存
* `jarg 关键字...` 查找Gradle jar包缓存
* `jara 关键字...` 查找Gradle 和 Maven jar包缓存
* `jars 关键字...` 浏览器打开 http://mvnrepository.com/search?q=关键字

**操作:**

* `Enter` 打开对应指定jar包缓存的目录
* `CTRL + Enter` 浏览器打开 http://mvnrepository.com/search?q=包名
* `CMD + Enter` 删除指定jar包缓存(不区分版本)

注意以上操作只会针对类型的缓存，例如通过 `jarm` 查出来的缓存，`CMD + Enter`只会删除 maven 的缓存，通过 `jara` 的删除操作会删除 maven 和 gradle 的缓存

**修正缓存路径**
我本机的 gradle 缓存路径时是 `~/.gradle/caches/modules-2/files-2.1`，如果你的路径不是这个，可以自己修改脚本中的路径

