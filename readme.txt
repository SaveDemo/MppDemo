/***************************目录*********************************/

	*	build		---Makefile脚本和sh脚本
	*	PATH_Build	---测试使用，可以随意更改
	*	Demo		---主程序代码路径
	*	output		---生成文件的路径
	*	third_lib	---静态库和头文件路径

/*****************************************************************/

/***********************添加，修改，生成**************************/

	添加新的平台
		在build目录添加相应的sh脚本，模仿其他脚本书写
		在build/Makefile文件中添加：相应的  ifeq  分支
		在third_lib目录创建相应的平台名称，并在该文件夹下创建extdrv,include,lib三个文件夹
			在include目录放置所有的头文件（SDK包里面有）
			在lib目录放置所有的.a静态库
	
	修改程序代码
		在Demo目录下，修改或者添加需要的文件即可（main程序在Demo_Sample.c文件中）

	生成文件介绍
		在Demo目录下，会生成每一个.c文件相应的.o文件
		在output目录下会生成一个名为Demo_Sample的可执行文件	

/*****************************************************************/

/******************************编译*******************************/

	编译当前工程
		默认编译：
			在build路径下执行make编译
			在build路径下执行make clean清空编译
			默认编译Hi3519DV500_010平台
		
		清空编译:
			在MppDemo目录下执行sh build/build_clean.sh

		指定编译：
			在MppDemo目录下执行sh build/build_xxxxxxx.sh
			例如编译SS928V00_022平台：sh build/build_SS928V100_022.sh

/*****************************************************************/

/******************************记录*******************************/

	当前移植使用记录
		Hi3519DV500_010:	移植测试使用，没有实际使用
		SS928V100_022:		移植测试使用，没有实际使用
/*****************************************************************/
