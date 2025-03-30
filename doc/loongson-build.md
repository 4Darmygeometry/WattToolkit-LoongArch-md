龙芯版Watt Toolkit仅支持在含**LSX**、[**LASX**](https://github.com/loongson-community/dotnet-unofficial-build/issues/9)扩展指令的64位龙架构(LoongArch64)CPU或用X86 Linux的.net 9交叉编译构建，构建原则遵循[Software Development and Build Convention for LoongArch™ Architectures](https://github.com/loongson/la-softdev-convention)。
龙芯版构建仅构建新世界版本。
- 系统要求
	- [AOSC OS 12 或更高版本](https://aosc.io/download)
	- [Loongnix 25 或更高版本](https://pkg.loongnix.cn/loongnix/25/isos/)
	- [Loongnix server 23.1 或更高版本](http://pkg.loongnix.cn/loongnix-server/23.1/isos/)
	- [Deepin 23 或更高版本](https://www.deepin.org/zh/download/)
	- [Yongbao 2.10 或更高版本](https://mirrors.wsyu.edu.cn/fedora/linux/Yongbao/2.10/)
	- [Alpine Linux 3.21.0 或更高版本](https://alpinelinux.org/downloads/)
	- [GXDE OS 15.14.2 或更高版本](https://www.gxde.top/)
	- [Debian 13 或更高版本](https://www.debian.org/)
- 工作负荷
	- .NET版本
		- [.NET 9.0及以上](https://github.com/loongson-community/dotnet-unofficial-build)
	- vscodium
		- [vscodium 1.96.2.24355及以上](https://github.com/VSCodium/vscodium)
	- Web 和云
		- ASP.NET 和 Web 开发
	- 桌面应用
		- .NET 桌面开发

### [SkiaSharp、HarfBuzzSharp龙架构新世界支持已经上游化](https://github.com/mono/SkiaSharp/pull/3198)，可以通过如下命令下载预览包：
```nuget install SkiaSharp.NativeAssets.Linux -Version 3.119.0-preview.0.38 -Source https://pkgs.dev.azure.com/xamarin/public/_packaging/SkiaSharp/nuget/v3/index.json```

```nuget install HarfBuzzSharp.NativeAssets.Linux -Version 8.3.1-preview.0.38 -Source https://pkgs.dev.azure.com/xamarin/public/_packaging/SkiaSharp/nuget/v3/index.json```
### 由于SkiaSharp、HarfBuzzSharp尚未发布添加龙架构新世界支持的nuget正式包，Avalonia UI尚未更新到3.119.0，需自行更改版本号并手动编译Avalonia UI。
### 由于龙架构新世界原生库尚未上架nuget.org，本项目龙芯版本使用[龙芯官方提供的nuget源](https://nuget.loongnix.cn)以提供cb等。
### 龙架构旧世界用户可以在[龙芯开源社区](https://www.loongnix.cn/zh/api/dotnet/)自行下载.net 9及以上版本编译此项目。常见问题可以看[参考文档](https://docs.loongnix.cn/dotnet/support/list/01.%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98-FAQ.html#%E9%BE%99%E8%8A%AFnuget%E6%BA%90%E7%9A%84%E9%85%8D%E7%BD%AE%E6%96%B9%E6%B3%95)。
### 龙架构新世界用户编译此项目时，可能会混入旧世界二进制文件，建议装[liblol旧世界兼容工具](https://liblol.aosc.io)以保证正常编译和运行。AOSC OS、Deepin 23、Yongbao一般自带liblol,无需额外安装。
### 若不想混入旧世界二进制文件，须参考[移花接木 —— 在其它平台上为 LoongArch 架构打包 .NET 程序](https://driver1998.github.io/posts/dotnet-cross-publish-loongarch/)手动移动运行时并停止使用龙芯nuget源。
