# ZRCheckVersion
## 原理
 
* 获取本地版本号、与APPStore版本号
* 以“.”来拆分版本号位
* 通过while循环来比对版本号大小
* 如果本地版本号>=APPStore版本号，为开发或者提交审核阶段，不进行提示更新；如果本地版本号<AppStore版本号，表示APPStore中有新版本，需要提示更新
## 相关API

 1、检查版本更新并弹框提示更新(默认：判断、更新、弹框、跳转)
 
 	+ (void)checkAppVersionAlertWithAppId: (NSString *)appId;


 检查版本更新（可以自定义弹框）

	+ (void)checkAppVersionWithAppId: (NSString *)appId result: (void(^)(BOOL))result;

 2、判断是否需要更新版本
 
	+ (BOOL)isUpdateWithCurrVer: (NSString *)currVer appStoreVer: (NSString *)appStoreVer;

3、获取APPStore的版本

	+ (void)getAppStoreVersionWithAppId: (NSString *)appID complete: (void(^)(NSString *appStoreVersion))complete err: (void(^)())err;

 4、打开APPStore中的应用
	
	+ (void)openAppStoreWithAppId: (NSString *)appId;

## 预览
<img src="/updateVersion.png" height="413" width="202">

