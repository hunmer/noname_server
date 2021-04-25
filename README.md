
#免费搭建无名杀服务器方法:

* 1.修改game.js ( 27985 行左右 )
```javascript
if(!withport){
	ip=ip + (ip.indexOf('wss://') == 0 ? ':443' : ':8080');
}
_status.connectCallback=callback;
try{
	if(game.ws){
		game.ws._nocallback=true;
		game.ws.close();
		delete game.ws;
	}
	game.ws=new WebSocket((ip.indexOf('//') == -1 ? 'ws://' : '') + ip);
}
```
* 2.在 https://glitch.com 注册账号并新建项目->从github导入->https://github.com/hunmer/noname_server.git

* 3.项目左下角->Tools->Terminal->输入 npm install --dependencies

* 4.App Status 显示OK后，Share按钮 -> 复制 Live site 地址，把开头的 https:// 换成 wss://

* 5.尝试联机