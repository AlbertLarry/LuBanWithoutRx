# LuBanWithOutRx
没有引入任何第三方框架的LuBan的library，默认使用的是三级压缩
## Step 1. Add the JitPack repository to your build file

    Add it in your root build.gradle at the end of repositories:

      allprojects {
        repositories {
          ...
          maven { url 'https://jitpack.io' }
        }
      }
## Step 2. Add the dependency

      dependencies {
              compile 'com.github.AlbertLarry:LuBanWithOutRx:1.0'
      }
 
## Used
    Luban.get(this).load(mFile).putGear(Luban.THIRD_GEAR)
                .setCompressListener(new OnCompressListener() {
                    @Override
                    public void onStart() {
                    }

                    @Override
                    public void onSuccess(final File file) {
                       //doSomething with file
                    }

                    @Override
                    public void onError(Throwable e) {
                        Log.i("way", "error");
                    }
                }).launch();
