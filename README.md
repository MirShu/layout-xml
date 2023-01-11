# Android Studio 中 layout xml界面布局目录分类

在Android 项目开发的时候，往往会遇到需要建立很多很多xml layout 布局文件等等....，

一些大一点的项目xml layout布局文件和图片以及各种资源文件全放main/res路劲地底下，这时就会有点庞大，凌乱。
这时候急需有序，按类型分类到不同类别里面，这样就会显得很清晰有条理不凌乱了。
那如何在res分类不同xml layout以及各种资源文件呢。

# 第一步、找到 res/layout文件夹，在此文件夹地下点击建立自己想要分类的文件名。

![2781551-3c5d8e073c9fc6b4](https://user-images.githubusercontent.com/13359093/211716719-a46d0a57-bf8f-4d73-901b-06fd780e9875.png)

# 第二步、在自己建立分类文件地下再建layout文件夹，是放xml.layout 布局文件的，这个和创建项目时候默认生成的layout是一样的

![2781551-885df0311ea7448a](https://user-images.githubusercontent.com/13359093/211716756-0d81cd4a-51ab-4715-868b-4d7280f63acb.png)

# 第三步，也是最后一步，重要的一步，就是在app gradle android{ } 文件中去设置引入自己创建的文件路劲,要不然项目是找不到自定义的文件路径的，所以说也是重要的一步。

![2781551-5874c433d82de768](https://user-images.githubusercontent.com/13359093/211716801-b4daa963-f0f3-45bc-95a1-33017ca2c3d6.png)


# 最后一步
当然不仅仅是xml layout 布局文件可以按类型分别放置，其他资源类文件也是可以的，
图片资源，values文件底部的资源文件等等...都是可以自定义放置自己目录下的，
注意点就是自定义放置好后记得在app gradle android{ } 进行引用就可以了。

```
sourceSets {
   main {
            res.srcDirs =
                    [
                            'src/main/res/main_layout',
                            'src/main/res/item_layout',
                            'src/main/res/other_layout',
                    ]
        }
    }

```
