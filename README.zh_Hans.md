# HITSC-Template

## 模板介绍

这个模板配置了`gradle`与`GitHub Actions`，能够开箱即用，适应实验硬性规定的目录结构，还能在远端编译完成之后下载编译出的`Jar`。由于这个模板采用的是`WTFPL`开源协议，所以其是不受任何限制的。

## 使用方法

要是用这个模板非常简单，只要做下面几步：

首先，将这个模板克隆到本地：

``` Shell
git clone https://github.com/mahoshojoHCG/HITSC-Template.git
```

让后将远程端换成你的实验仓库地址，后面的地址要填写你的仓库地址，不要直接复制这个：

``` shell
git remote set-url origin https://github.com/XXX/Labn-123456789.git
```

然后看一下远端是否换成功了：

``` shell
git remote -v
```

看列出来的远端里有没有你的仓库地址，要是没有怎么办？如果前面有错误信息，把这个错误复制到搜索引擎里面搜索，实在解决不了就开[Issuse](https://github.com/mahoshojoHCG/HITSC-Template/issues)。

然后进行`push`：

``` shell
git push -u origin master
```

这时候，你的远程仓库也就变成了这个模板的样子。

接下来，安照你的需求对这个模板的一些细节进行修改。这个模板对应的是三个任务，如果不足三个任务，或者多余三个任务，打开`build.gradle`，看到

``` groovy
sourceSets {
    main {
        java {
            srcDir 'src/P1'
            srcDir 'src/P2'
            srcDir 'src/P3'
        }
    }
    test {
        java {
            srcDir 'test/P1'
            srcDir 'test/P2'
            srcDir 'test/P3'
        }
    }
}
```

按照上面的格式依葫芦画瓢，增加或删除源代码目录。

接着看到上面，修改`com.example`为你想要的包名。

``` groovy
group 'com.example'
```

然后打开`settings.gradle`，将项目名改为你要的项目名：

``` groovy
rootProject.name = 'Labn'
```

最后，大功告成，使用你喜欢的IDE打开文件夹或者导入项目，就能使用了！

远程编译好的`jar`文件，在你的仓库里面`Actions`可以下载。
