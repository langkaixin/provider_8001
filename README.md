打包后，使用以下命令运行jar包

`nohub java -jar -Dloader.path=${lib_dir} xxxx.jar --spring.config.location=${config_dir} > 2>&1 & `

**assembly插件打包注意事项：**

1.assembly 插件所在模块必须最后被加载，即父工程中，给model要处于列表中的最后一个

2.主模块的pom中必须要有`spring-boo-maven-plugin`插件

3.使用`maven-jar-plugin`将模块打包时，要排除配置文件（否则使用assembly就没有意义了）


