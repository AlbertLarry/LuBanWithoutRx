# LuBanWithOutRx
抽取[LuBan](https://github.com/Curzibn/Luban)的核心算法，
没有引入任何第三方的东西。
默认使用的是三级压缩，对图片进行压缩。
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

## 方法对应表

方法名|功能 ---|--- load(File file)|传入要压缩的文件 setFilename(String filename)|设置压缩后图片命名 putGear(int gear)|设置压缩档次

参考链接，大名鼎鼎的[LuBan](https://github.com/Curzibn/Luban) 链接：[https://github.com/Curzibn/Luban](https://github.com/Curzibn/Luban)