# MD5Encrypt
一行代码搞定MD5加密、base64加密、aes加密、与base64解密和aes解密 

# PhotoShoot
![image](https://github.com/Zws-China/WSCycleScrollView/blob/master/WSCycleScrollView/WSCycleScrollView/scroll.gif)


# How To Use

```ruby

使用注意事项:
1. 在build phases中的GTMBase64.m需要设置 -fno-objc-arc
2. 在#import "NSString+Base64.m”文件中导入   #import <Foundation/Foundation.h>
3.在#import "GTMBase64.m”文件中添加          #import <CommonCrypto/CommonCrypto.h>


//md5加密
NSString *strEnRes = [CusMD5 md5String:@"需要加密的内容"];





//base64加密
NSData *dataEn = [@"需要加密的内容" dataUsingEncoding:NSUTF8StringEncoding];
NSData *dataEnRes = [GTMBase64 encodeData:dataEn];
//把加密结果转成string
NSString *base64EnRes = [[NSString alloc] initWithData:dataEnRes encoding:NSUTF8StringEncoding];


//base64解密
NSData *resDeBase64 = [GTMBase64 decodeData:@"需要解密的密文"];
NSString *strDeBase64 = [[NSString alloc] initWithData:resDeBase64 encoding:NSUTF8StringEncoding];





//aes 加密
NSString *strAESEnRes = [AESCrypt encrypt:@"需要加密的内容" password:@"secret"];

//aes 解密
NSString *strAESDeRes = [AESCrypt decrypt:@"需要解密的密文" password:@"secret"];




```