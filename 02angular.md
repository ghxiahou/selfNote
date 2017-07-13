###1.angular1.5和angular1.6版本的变化
- 网络请求发生了变化: <br>
  success改为then <br>
  error改为catch <br>
  返回数据里面有一个data

- 路由锚点发生变化: <br>
  1.5版本:#/music <br>
  1.6版本:#!/music(添加了一个叹号)
- 跨域需要设置白名单

		app.config(['$sceDelegateProvider',function ($sceDelegateProvider) {
	     $sceDelegateProvider.resourceUrlWhitelist([
	            'self',
	            'http://www.douban.com/**'  
	        ])
	    }]);
		//1.一个 * 代表当前文件夹下面的所有文件都可以访问,不包括子文件夹下的文件
		//2.二个 ** 站点文件夹下面的所有文件都可以访问

###2.自定义服务的命名有个不成文的规定,名称前不要加$符号

###3.controller和link的区别:
- controller:程序已启动就会调用,不管dom有没有加载完毕,就会调用
  一般在控制器里面做一些业务逻辑的处理, 数据处理
- link:当dom加载完毕的时候调用,一般在这里面做dom操作

###4.template:需要导入的html模块

###5.
   