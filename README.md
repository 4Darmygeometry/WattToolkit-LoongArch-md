# WattToolkit-LoongArch-md
提供Watt Toolkit（Steam++）龙架构版所依赖的so文件以及nuget包
# 使用方法
在构建项目中创建WattToolkit/native/linux-loongarch64/文件夹，将libe_sqlite3.so、libHarfBuzzSharp.so、libonigwrap.so、libSkiaSharp.so全部移入，然后在[龙架构新世界.net](https://github.com/loongson-community/dotnet-unofficial-build)中下载SDK，提取出运行时，放入WattToolkit/dotnet/文件夹，即可构建出完整的龙架构Watt Toolkit。
# 这些so是否为开源项目所构建
这些so通过[SkiaSharp](https://github.com/mono/SkiaSharp)、[harfbuzz](https://github.com/harfbuzz/harfbuzz)等开源项目通过代码适配龙架构，再添加[龙芯nuget源](https://nuget.loongnix.cn)构建而成。构建教程及注意事项参考[常见问题](https://docs.loongnix.cn/dotnet/support/list/01.%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98-FAQ.html#%E9%BE%99%E8%8A%AFnuget%E6%BA%90%E7%9A%84%E9%85%8D%E7%BD%AE%E6%96%B9%E6%B3%95)。
# 构建注意事项
构建这些so时，须遵循[Software Development and Build Convention for LoongArch™ Architectures](https://github.com/loongson/la-softdev-convention)，构建机GCC需在13.2及以上且支持LSX。
构建完这些so后，须用sha256sum生成对应sha256文件，与so一并通过pull request的形式上传至此处。
# 构建旧世界是否可以使用这些so
由于这些so为新世界版本so，旧世界不可直接使用，需自行编译对应so。
