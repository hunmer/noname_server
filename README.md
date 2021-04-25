
#免费搭建无名杀服务器方法:

* 1.修改game.js ( 27985 行左右 )
```javascript
if(!withport){
    ip=ip+'';
}
_status.connectCallback=callback;
try{
	if(game.ws){
		game.ws._nocallback=true;
		game.ws.close();
		delete game.ws;
	}
	game.ws=new WebSocket('wss://'+ip+'');
}
```
* 2.在 https://glitch.com 注册账号并新建项目->从github导入->https://github.com/hunmer/noname_server.git

* 3.项目左下角->Tools->Terminal->输入 npm install --dependencies

* 4.App Status 显示OK后，Share按钮 -> 复制 Live site 地址，把开头的 https:// 去掉

* 5.完成