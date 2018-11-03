# We_SpeakAndroidSDK
使用说明
1、工程gradle文件添加maven url
allprojects {
    repositories {
        google()
        jcenter()
        maven { url 'https://github.com/StanWeedu/We_SpeakAndroidSDK/raw/master'}
    }
}
2、app gradle 添加依赖

api 'com.github.bumptech.glide:glide:3.7.0'
api('com.github.bumptech.glide:okhttp3-integration:1.4.0') {
        exclude group: 'glide-parent'
}
api 'com.android.support:support-v4:25.4.0'
api 'com.android.support:design:25.4.0'
api 'com.android.support:appcompat-v7:25.4.0'
api 'com.squareup.okhttp3:okhttp:3.4.1'
api 'com.squareup.okio:okio:1.9.0'

api 'com.we:wespeak:1.0.0'

3、工程Application onCreate中添加初始化
@Override
public void onCreate() {
    super.onCreate();
    WeApplication.initialize(this);
}

4、使用时调用
WeApplication.startWonderEnglish(context, "");
