### Carthage使用介绍

---
* [Carthage 在Github上的位置](https://github.com/Carthage/Carthage)
* 使用注意事项 `适用于iOS8+`
<br>

---
### 安装&使用
	
* 第一步: 安装 & 使用简介

	```
	brew update && brew upgrade --all && brew install carthage
	carthage version	
	carthage help  # 基本功能的简要说明 
 	```
 	
 	<br>
 	
 	```
 	$ carthage help
Available commands:

   archive           Archives built frameworks into a zip that Carthage can use 
   bootstrap         Check out and build the project's dependencies
   build             Build the project's dependencies
   checkout          Check out the project's dependencies
   copy-frameworks   In a Run Script build phase, copies each framework specified by a SCRIPT_INPUT_FILE environment variable into the built app bundle
   fetch             Clones or fetches a Git repository ahead of time
   help              Display general or command-specific help
   outdated          Check for compatible updates to the project's dependencies
   update            Update and rebuild the project's dependencies
   version           Display the current version of Carthage
   ```
 	
* 第二步: 增加Bash自动完成配置(确保第一步安装成功)
 
 	`点击Tab键, 快速补全 carthage后面的参数`
 	
 	```
 	echo -n "source " >> ~/.bash_profile
 	CARTHAGE_VERSION=`carthage version`
 	find /usr/local/Cellar/carthage/${CARTHAGE_VERSION} -type f -name *bash* >> ~/.bash_profile
 	source ~/.bash_profile
 	```
 	
* 第三步: 在你的Project文件夹下面(其它文件夹也可以, 因为Carthage不会改变你工程的任何设置)创建`Cartfile`文件, 假设你的工程中需要使用[Charts](https://github.com/danielgindi/Charts)
 
 	```
 	# 绘图库  这行是注释  
 	# 第一个: 来源  第二个: 名称  第三个:版本
	github "danielgindi/Charts"  == 2.2.4

 	```
* 第四步: 下载
 
 	```
 	carthage update --platform iOS --use-ssh --no-use-binaries --no-build 
 	```
 	
 	这一步有很多参数, 不过我们可以使用第二步配置好的自动完成功能, 准确高效的输入, 不用硬记. 比如输入 carth\Tab --p\Tab --u\Tab. <br><br>
 	参数说明 :<br>
 	* update 更新并重新编译
 	* --platform 目标平台 后面的输入i\Tab
 	* --use-ssh  是否使用ssh://xxx格式,默认使用https 如Https://github....
 	* --no-use-binaries 不使用已有的binaries, 意思就是下载好后,自己再编译
 	* --no-build  只下载不编译
 	
 	<br>
* 第五步: 外部Framework使用方法
	[How to use ios framework](https://www.bing.com/search?q=how+to+use+ios+framework)
 	
===

### 附常用功能 & 参数 


`这种样式表示常用参数`

*  常用功能
	* update 
	* bootstrap 
	* build 
	* help
	
<br>

* 参数介绍

	* build 不更新代码, 直接编译 可选参数 --color              --derived-data       `--platform`          `--verbose`            
--configuration      --no-skip-current    --project-directory  
	* checkout 检查依赖  --color              `--no-use-binaries`    --project-directory  `--use-ssh`            `--use-submodules`
	* fetch	   更新代码 --color              `--no-use-binaries`    --project-directory  `--use-ssh`            `--use-submodules`
	* update   更新代码并重新编译或下载 `--color`              `--no-build`           `--platform`           `--use-submodules`     
--configuration      --no-checkout        --project-directory  --verbose            
--derived-data       `--no-use-binaries`    `--use-ssh`            
	* bootstrap  `--color`	              `--no-build`           `--platform`           `--use-submodules`     
--configuration      `--no-checkout`        --project-directory  --verbose            
--derived-data       `--no-use-binaries`    `--use-ssh`            
 	
 	
 	
