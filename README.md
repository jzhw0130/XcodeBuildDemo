# XcodeBuildDemo


//AppStore  
xcodebuild -scheme AutoDemo -archivePath Release/appstore/AppStore.xcarchive -sdk iphoneos -configuration Release  PROVISIONING_PROFILE=milo archive

xcodebuild -exportArchive -archivePath Release/appstore/AppStore.xcarchive -exportPath Release/appstore/ -exportOptionsPlist   Release/export-appstore.plist  
altool --upload-app -f  Release/appstore/AutoDemo.ipa -u jingzhiwei@ihealthlabs.com.cn -p *********
  

  
//Enterprise  
xcodebuild -scheme AutoDemo -archivePath Release/enterprise/Enterprise.xcarchive  -sdk iphoneos -configuration EnterPrise PROVISIONING_PROFILE=MiloProfile archive

xcodebuild -exportArchive -archivePath Release/enterprise/Enterprise.xcarchive -exportPath Release/enterprise/ -exportOptionsPlist  Release/export-enterprise.plist
