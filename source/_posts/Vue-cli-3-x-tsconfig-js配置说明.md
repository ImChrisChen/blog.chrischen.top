---
title: Vue-cli-3.x tsconfig.js配置说明
date: 2019-06-12 17:29:49
tags: 
- Vue
- Typescript
---
<!--# tsconfig.js 配置详情-->

~~~json
//tsconfig.json指定了用来编译这个项目的根文件和编译选项
{
  //compilerOptions:编译选项,可以被忽略，这时编译器会使用默认值
  "compilerOptions": {
	
	//允许从没有设置默认导出的模块中默认导入。这并不影响代码的显示，仅为了类型检查。
	"allowSyntheticDefaultImports": true,
	
	//解析非相对模块名的基准目录
	"baseUrl": "./src",
	
	//给源码里的装饰器声明加上设计类型元数据
	"emitDecoratorMetadata": true,
	
	//启用实验性的ES装饰器
	"experimentalDecorators": true,
	
	//指定生成哪个模块系统代码
	"module": "commonjs",
	
	//决定如何处理模块。或者是"Node"对于Node.js/io.js，或者是"Classic"（默认）
	"moduleResolution": "node",
	
	//不再输出文件中生成用户自定义的帮助函数代码，如__extends。
	"noEmitHelpers": true,
	
	//在表达式和声明上有隐含的any类型时报错
	"noImplicitAny": false,
	
	//用于debug ,生成相应的.map文件
	"sourceMap": true,
	
	//在严格的null检查模式下，null和undefined值不包含在任何类型里，只允许用它们自己和any来赋值（有个例外，undefined可以赋值到void）。
	"strictNullChecks": false,
	
	//目标代码类型
	"target": "es5",
	
	"paths": {
	  //模块名到基于baseUrl的路径映射的列表
	},
	
	"lib": [
	  //编译过程中需要引入的库文件的列表
	  "dom",
	  "es6"
	],
	
	"types": [
	  //要包含的类型声明文件名列表；如果指定了types，只有被列出来的包才会被包含进来
	  "hammerjs",
	  "node",
	  "source-map",
	  "uglify-js",
	  "webpack"
	]
  },
  
  "exclude": [
	//如果"files"和"include"都没有被指定，编译器默认包含当前目录和子目录下所有的TypeScript文件（.ts, .d.ts 和 .tsx），排除在"exclude"里指定的文件。
	"node_modules",
	"dist"
  ],
  
  //Typescript加载选项
  "awesomeTypescriptLoaderOptions": {
	"forkChecker": true,
	"useWebpackText": true
  },
  
  "compileOnSave": false,
  
  "buildOnSave": false,
  
  "atom": {
	"rewriteTsconfig": false
  }
}
~~~


