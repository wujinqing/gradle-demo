## 如何将jar包安装到本地仓库

方法一：
```
apply plugin: 'maven'

uploadArchives {
    repositories {
        mavenDeployer {
            repository(url: "file://localhost/tmp/myRepo/")
        }
    }
}
```

执行命令:
> gradle uploadArchives

方法二:
```
apply plugin: 'maven'
```

执行命令:
> gradle install

方法三：
```
plugins {
  id 'maven-publish'
}

publishing {
    repositories {
        maven {
            url "file://C:\\Users\\wujq\\.m2\\repository"
        }
    }
}
```

执行命令:
> gradle publishing













































