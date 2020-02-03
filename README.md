Keychain
====

1. 使用[react-native-keychain](https://github.com/oblador/react-native-keychain)
-------     
yarn add react-native-keychain                              
import * as Keychain from 'react-native-keychain'; 
```
const username = 'zuck';           
const password = 'poniesRgr81';           
Keychain.setSharedWebCredentials('www.XXXXXXXX.com',username,password).then(e=>{           
console.log('0:',e)         
}).catch(e=>{        
console.log('1:',e)         
})            
```  

2. 在工程中开启Associated Domains， 填写需要在哪个domain中保存的账户密码。
-------
![](https://github.com/Bing619/Keychain/blob/master/img/Domains.png)  

3. 创建文件：apple-app-site-association，填写以下内容。2XXXXXXXX是你证书的Team。然后放到你上面domain根目录下。
-------
        {
            "webcredentials": {
                    "apps": ["2XXXXXXXX.com.yourapp.demo"]
            }
        }

4. 最后效果
-------
![](https://github.com/Bing619/Keychain/blob/master/img/1.png)  
![](https://github.com/Bing619/Keychain/blob/master/img/2.jpeg)  

5. 备注
-------
        这是测试功能，实际效果不用这个代码，自动保存。
