#introduction -- inmobi ane for flash android and ios application
this is a free adobe native extention (ane) of inmobi ad network for flash air mobile developer.<br/>
it very easy to use,you can pack your air application or game on pc or mac,<br/>
with the same code just with as3,and not any java or objective-c need.<br/>

1.support all inmobi banner ad sizes and Interstitial<br/>
2.support ads on android and ios(iphone ,ipad ,ipad)<br/>
3.supportlandscape andportrait mode<br/>
4.supportauto Orients air application<br/>
<br/>
###inmobi 1.0.ane
flash air ane lib,contains lib for android and ios all in one file,<br/>
although there are 4m file size, but it does not increase the final release package size, ease of use.<br/>
###builds
base on inmobi network ios sdk 4.5.1 and inmobi android sdk 4.5.2<br/>
base on adobe air sdk 15,so your app air sdk version must be 15 or higher<br/>
ref:http://www.inmobi.com/<br/>
ref:http://labs.adobe.com/<br/>
download:https://github.com/lilili87222/inmobi-ad-adobe-native-extention<br/>
###  extention id
this extention id will been add in application-app.xml<br/>
```
<extensionID>so.cuo.platform.inmobi</extensionID>
```
###banner
how to show a banner ad in air mobile app?
```
if (Inmobi.getInstance().supportDevice)
{
	Inmobi.getInstance().setBannerKeys("app key"); //init inmobi
	Inmobi.getInstance().showBanner(Inmobi.BANNER, InmobiPosition.BOTTOM_CENTER);//show banner with posiction botton_center
}
```
###Interstitial###
1.how to show a Interstitial ad in flash ios or android game?
```
if (Inmobi.getInstance().supportDevice)
{
	Inmobi.getInstance().setBannerKeys("app key"); //init inmobi
	Inmobi.getInstance().addEventListener(InmobiEvent.onInterstitialReceive,onReceiveAd);
	Inmobi.getInstance().cacheInterstitial();//load insterstial ad
}
private function onReceiveAd(event:InmobiEvent):void
{
	Inmobi.getInstance().showInterstitial();//when load success ,display it
}
```
2.also you can do like follow to show inmobi Interstitial
```
Inmobi.getInstance().setBannerKeys("app key"); //init the inmobi
Inmobi.getInstance().cacheInterstitial();//start load interstitial ad
```
After some time
```
if (Inmobi.getInstance().isInterstitialReady())
{//check has load success
	Inmobi.getInstance().showInterstitial();//display ad
}
```
### for android 
for android user,must add inmobi activity to xxx-app.xml
```
<manifest android:installLocation="auto">
     <uses-sdk android:targetSdkVersion="11"/>
     <uses-sdk android:minSdkVersion="8"/>
    <uses-permission android:name="android.permission.INTERNET"/>
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
    <application>
    <activity android:name="com.inmobi.androidsdk.IMBrowserActivity" android:configChanges="keyboardHidden|orientation|keyboard|smallestScreenSize|screenSize" android:hardwareAccelerated="true" /> </application>
</manifest>
```
###more
if you enable analyst in www.inmobi.com ,you can view your app install info without do any thing<br/>
<br/>
if you create a app ,and not verify it,or your app not in activity state,you can not load ad,you will get a invalid app id error<br/>
###you may like
https://github.com/lilili87222/admob-for-flash<br/>
https://github.com/lilili87222/as3-air-ad-network-framework <br/>
  email:wohaosea@gmail.com
 
 if user like this lib,you can download and review our game <br/>
https://itunes.apple.com/us/artist/phonegame/id553087275?mt=8 <br/>
donate and download more ane  <br/>
http://www.cuo.so/ane-list/index.html  <br/>
