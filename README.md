# translate-encode-guide
from YukinoAi/FansubbingAndEncoding.GuidesIndex.markdown
*注意：如果有任何链接损坏或您知道任何更有用的指南，请通过[联系我](//yukisubs.wordpress.com/about)提供建议。

*最后更新：2020年9月28日

*Markdown和白色版本[在此处提供](//gist.github.com/YukinoAi/acea024631a2585aa592b16b4bde959f)，[备用](//gist.github.com/zeriyu/e6c171f6224d6134d79996c11de02995)，单击“原始”即可。

#### 做字幕和编码的指南目录：

* [做字幕的概述](#fansubbing-overview)

* [抓取](#capping)

* [编码](#encoding)

    * 音频

    * 播放（电脑/HTPC）

* [复用和解复用](#muxing-and-demuxing)

* [过滤](#filtering)

    * 情景过滤

* [翻译](#translating-tl--translate-check-tlc)

* [编辑+质量检查（QC）](#editing--quality-check-qc)

* [时轴](#timing)

* [排版](#typesetting)

* [分发（Distro）](#distribute-distro)

    * 种子

    * HTTP / S

    * IRC

    * [其他分发工具](#random-distro-tools)

    * [团队博客](#the-group-blog)

    * [适用于DIY人群的分发](#distro-for-do-it-yourself-diy-people)

* [混流](#remux)

* [模拟](#in-service-of-chaos-analog)

#### 做字幕的概述

* 理论：[动漫做字幕的历史](//en.wikipedia.org/wiki/Fansub)和[做字幕的现状：已死](http://www.crymore.net/2015/05/15/the-state-of-fansubbing-its-dead)。

* 各种指南索引或概述：

    * 此指南索引。备选方案：

    * Doki的[做字幕的流程概览](//doki.co/support/the-fansubbing-process)，[便携式文档格式（PDF）](//yukisubs.files.wordpress.com/2016/10/the_fansubbing_process_doki_fansubs.pdf)。

* unanimated的[指南目录](//unanimated.github.io/guides.htm)

     * 排版指南[Guide](//unanimated.github.io/ts/index.htm)，[PDF-White](//yukisubs.files.wordpress.com/2020/04/typesetting_in_aegisub_by_unanimated_2018_white.pdf)，[PDF-Black](//yukisubs.files.wordpress.com/2020/04/typesetting_in_aegisub_by_unanimated_2018_black.pdf)，[PDF-old](//yukisubs.files.wordpress.com/2016/10/unanimated_fansub_guides.pdf)。

    * SubsByRock [Index](//subsbyrock.wordpress.com/links).

    * tekeremata的[这是什么](http://tekeremata.org/category/articulos/taller-de-fansub/) (西班牙语，向下滚动)。

    * 还有这个[白痴指南](//fansubbing.blogspot.com/2007/03/what-goes-into-fansub-aka-idiots-guide_05.html)。

* [Aegisub](http://docs.aegisub.org/manual/Overview)：fansubbers的核心工具。[二进制文件](http://plorkyeran.com/aegisub)。

    * Aegisub的[主要文档](http://docs.aegisub.org/manual/Overview)，[PDF](//yukisubs.files.wordpress.com/2017/05/aegisub-3-2-manual.pdf)，[路径标识符](http://docs.aegisub.org/3.2/Aegisub_path_specifiers/)，并收藏此页：[ASS超级标记](http://docs.aegisub.org/manual/ASS_Tags)。

* [随机fansubbing提示](http://mod16.org/hurfdurf/?p=128)（面向团体）。

* 一个日常生活：[博客文章](http://mod16.org/hurfdurf/?p=144)，[采访](//uniquec.shinsen-radio.org)，[YT播放列表](//www.youtube.com/playlist?list=PLtwIkfU56fRSZgaPHFt79ei1_Kf4cDaFY)以及以前的情况：web.archive.org/web/20021013081748/http://pepper.idge.net:80/digisub.html，[PDF](//yukisubs.files.wordpress.com/2018/02/digisub_guide_onceuponatimein2002.pdf)。

#### 采集

*理论：目的是获得源媒体。

* 最好的资源通常是原始的数字视频光盘(DVD)或原始的蓝光光盘(BDMV)，但上传并不总是可用的。

* 如果没有，那么捕捉也可以意味着购买零售媒体。考虑购买动画DVD / BD来支持工业。否则，现有的VHS / LD / DVD / BD或网络剪辑可能具有可接受的质量。

* 对于广播流，捕获意味着录制模拟流，然后使用特殊硬件进行数字化，或者对于互联网[同步广播]（//en.wikipedia.org/wiki/Simulcast）（数字），则意味着使用特殊软件进行[流复制]（//ffmpeg.org/ffmpeg.html#Stream-copy）。有时，原始版本也可以从仅限邀请的私人跟踪器获得。有关捕获字幕的信息，请参见“Remux”部分。

* 链接：对于模拟电视、8毫米、VHS和LD，请参见“模拟视频”。

* 数字电视/有线/卫星：数字[信号处理]（http://slideplayer.com/slide/6002959/）。玩得高兴。

* 数字视频光盘（DVD）：[DVD-Decrypter ](http://fileforum.betanews.com/detail/DVD-Decrypter/1011845169/1)，[DVD Decrypter指南]（http://www.doom9.org/index.html?/dvddec.htm） ，[PDF]（//yukisubs.files.wordpress.com/2016/10/dvd-decrypter_guide.pdf）和第二个指南（//www.dvd-guides.com/guides/copydvdtodvd/22-how-to-copy-a-dvd-59-using-dvd-decrypter）。

* DVD / Blu-ray Disc（BD）：[MakeMKV](//www.makemkv.com)，以及[Handbrake和MakeMKV指南](//lifehacker.com/5559007/the-hassle-free-guide-to-ripping-your-blu-ray-collection)。

* 对于简单的流提取：[MKVToolNix](//mkvtoolnix.download/downloads.html)+ [gMKVExtractGUI](//sourceforge.net/projects/gmkvextractgui)，甚至只需[FFMPEG](//wiki.archlinux.org/index.php/FFmpeg#Subtitles)。另请参见Muxing部分。

* 对于一般的字幕转换：[Subtitle Edit](http://www.nikse.dk/subtitleedit)和他们的[文档](http://www.nikse.dk/SubtitleEdit/Help)。

* 要提取字幕，请参见Muxing和Remux部分。

* 网络剪辑：

  * [youtube-dl](//github.com/rg3/youtube-dl)，[图形用户界面(GUI)](//github.com/MrS0m30n3/youtube-dl-gui)。支持多个站点，包括Crunchyroll(CR)的“行业标准”。

    * Youtube有时基于区域封锁视频。要绕过，请使用此[区域检查器](//unblockvideos.com/youtube-video-restriction-checker)和[虚拟专用网络(VPN)](//en.wikipedia.org/wiki/Virtual_private_network)，有一个出口点在未封锁的地区。

  * [Crunchyroll-XML-Decoder](//github.com/jaw20/crunchy-xml解码器) +[workaround instructions]（//gist.github.com/gdiaz384/ba8dfc45a44f92840aaf2617f802351f）（2017年1月）。仅支持多语言字幕下载。

  * Crunchyroll下载器工具包DX，[Mediafire]（//www.mediafire.com/file/0jevs7wnhh0x0u6/Crunchyroll+Downloader+Toolkit+DX.zip），[Mega]（//mega.nz/#F!wUYwDSgA!8tx_37HUBcs9KqPhkk5FmQ）。仅限Windows。注意：我没有测试过这个。

  * [Crunchyroll-Download-Tool](//gitlab.com/RIP/Crunchyroll-Download-Tool)(DX工具包的扩展，用于批量下载）。注意：我没有测试过这个。

  * Seiya的[Funimation-Downloader-nx](//github.com/seiya-dev/funimation-downloader-nx)和[GUI](//github.com/Golumpa/FuniBatchGUI)。注意：我没有测试过这个。另外：相关的[猫](//yukisubs.files.wordpress.com/2018/02/golumpascat.jpg)。

  * 对于Netflix、Amazon和Hulu，已知的唯一有效的非场景剪辑方法是屏幕捕捉软件，如[OBS]（//obsproject.com），或100%手动RTMP传输流剪辑。

 * 更多阅读：[netflix-subtitle-downloader]（//greasyfork.org/en/scripts/26654-netflix-subtitle-downloader）。注意：我没有测试过这个方法。

* DVD原始文件、BDMV和Webrips也可以从其他人那里二手获得。请参见分发部分。

#### 编码

* 视频理论（基础）：视频可以描述为快速连续显示的一系列图片。

* 编码视频的最基本原因是保留复杂变化（例如任何过滤）并使视频流更小。即使是一分钟的原始未压缩视频也有几个GigaBytes（GB）的大小。基本思想是将文件大小减小到主观“可接受”的水平，同时保留尽可能高的质量。

* 动态图画工程小组（MPEG）视频编码的工作原理是压缩一幅图片（称为“关键帧”），然后记录该帧与下一帧之间的任何变化。然后记录该第二帧与其后一帧之间的变化，以此类推。要显示任何给定帧，必须从最近的前一个关键帧开始解码所有帧。

* 视频理论（完整）：在没有理解理论的情况下遵循编码指南只会带来麻烦，但是由于需要如此多的背景知识，所以没有一个好的地方能开始学习视频编码。这个就快了：[A＆E对所有音频和视频技术指南（v3）的技术指南]（//www.animemusicvideos.org/guides/avtech31），[PDF]（//yukisubs.files.wordpress.com/2016/10/aandes_technical_guides_to_all_things_audio_and_video.pdf）。全部阅读，不要给自己找借口。 A＆E的指南已过时，但对理论非常好。现代工作流程指南在下面找到。

* 编解码器和容器理论：

   * 观看这个视频：[编解码器的工作原理 - 教程]（//vimeo.com/104554788）全部都看一遍！

   * 容器VS编解码器：[媒体格式]（//www.dr-lex.be/info-stuff/mediaformats.html）和[如何选择正确的编解码器和容器]（//www.videomaker.com/article/c03/18165-how-to-choose-the-right-codec-and-container-for-your-video-workflow）和[阅读此讨论]（//collectr.blogspot.com/2011/08/encoding-wars-return-of-revenge-of.html）。

   * 维基百科（Wiki）：[编解码器比较]（//en.wikipedia.org/wiki/Comparison_of_video_codecs），[容器比较]（//en.wikipedia.org/wiki/Comparison_of_video_container_formats），[MPEG标准]（//en.wikipedia.org/wiki/Moving_pictures_Experts_Group）。

   * HEVC评论[1]（//forums.bakabt.me/index.php?topic=45462.0），[2]（//x265.ru/en/bolshoe-sravnenie-kodekov-h265-ot-mgu），[PDF]（//yukisubs.files.wordpress.com/2016/10/msu_hevc_comparison_2015_free.pdf）和[3]（//blogs.gnome.org/rbultje/2015/09/28/vp9-encodingdecoding-performance-vs-hevch-264）。

     * 有趣的相关[博客文章]（http://archimago.blogspot.com/2016/12/musings-end-of-2016-video-encoding-hevc.html）。

     * Kokomini的[x265和Opus / AAC编码指南]（https://kokomins.wordpress.com/2019/10/10/anime-encoding-guide-for-x265-and-why-to-never-use-flac/）。

   * 参考：[由FOURCC提供的视频编解码器]（https://www.fourcc.org/codecs.php）和[相关摘要]（//docs.microsoft.com/en-us/windows/desktop/medfound/video-fourccs）。

* 亮度和颜色理论：

   * 人类[色彩感知]（//www.cambridgeincolour.com/tutorials/color-perception.htm）和[相关怪癖]（//www.cambridgeincolour.com/tutorials/cameras-vs-human-eye.htm）。

      * 我们都是盲人。自己看一下：[人类盲点测试]（https://yukisubs.files.wordpress.com/2020/04/blind-spot-test.jpg）。

   * Adobe Video Road博客：[理解颜色]（//blogs.adobe.com/VideoRoad/2010/06/understanding_color_processing.html），[什么是YUV]（//blogs.adobe.com/VideoRoad/2010/06/what_is_yuv.html），[颜色子采样]（//blogs.adobe.com/VideoRoad/2010/06/color_subsampling_or_what_is_4.html）。

* [8位 vs 16位](//www.diyphotography.net/8-bit-vs-16-bit-color-depth-use-matters).

   * [位深度教程](//www.cambridgeincolour.com/tutorials/bit-depth.htm).

   * [Doki - 讨论: 10位 h264](//doki.co/2011/07/19/discussion-10-bit-h264) 或者这里附带的PDF文件: [10位AVC广播](//yukisubs.files.wordpress.com/2016/10/using_10-bit_avc-h-264_encoding_with_422_for_broadcast_contribution_-_pierre_larbier.pdf), [为什么10位可以节省带宽](//yukisubs.files.wordpress.com/2016/10/why_does_10bit_save_bandwidth_-_ateme.pdf), [10位演示文稿](//yukisubs.files.wordpress.com/2016/10/10-bit_pristine_video_quality_presentation_-_ateme.pdf).

      * 有趣的相关[博客文章](http://archimago.blogspot.com/2016/12/quick-compare-avc-vs-hevc-8-bit-vs-10.html).

   * 理解[直方图](//www.cambridgeincolour.com/tutorials/histograms1.htm), [第2部分](//www.cambridgeincolour.com/tutorials/histograms2.htm)和一个[示例](//yukisubs.files.wordpress.com/2018/06/beluga.jpg).

   * 理解[白平衡](//www.cambridgeincolour.com/tutorials/white-balance.htm).

   * [动态范围](//www.cambridgeincolour.com/tutorials/dynamic-range.htm).

   * 有趣的案例研究:

      * 维基百科：[色彩空间](//en.wikipedia.org/wiki/Color_space)，[Rec601](//en.wikipedia.org/wiki/Rec._601)和[Rec709](//en.wikipedia.org/wiki/Rec._709)。

      * [NTSC与PAL彩色主色调](//video.stackexchange.com/questions/16840/ffmpeg-explicitly-tag-h-264-as-bt-601-rather-than-leaving-unspecified).

      * [YCbCr色彩分量数据范围的示例](http://discoverybiz.net/enu0/faq/faq_YUVDataRangeByBreeze.html)的信息。

      * 不同[YUV子采样模式](http://discoverybiz.net/enu0/faq/faq_YUVSubSampleByBreeze.html)的信息。

      * 进行色彩系列转换时不同YUV子采样模式的PSNR比较：[RGB-YUV-RGB转换的质量](http://discoverybiz.net/enu0/faq/faq_YUVbyBreeze_test_00.html)。 

* 帧速率理论：

* [人类能看到多少帧？](https://www.100fps.com/how_many_frames_can_humans_see.htm)，[PDF](//yukisubs.files.wordpress.com/2016/11/how_many_fps_can_the_human_eye_see.pdf)。

    * 帧速率（FPS）理论指南还涵盖通过模糊和亮度敏感度来实现“平滑”的内容。

    * [了解FFMPEG的图片组（GOP）选项](//esoterictek.blogspot.com/2017/04/understanding-ffmpegs-group-of-pictures.html)。

    * 变量帧速率：[献给字幕组编码器的VFR](//forums.animesuki.com/showthread.php?t=34738)，[PDF](//yukisubs.files.wordpress.com/2016/10/vfr_for_fansub_encoders.pdf)。

    * AviSynth的[VFR工作指南](http://avisynth.nl/index.php/VFR)和[VFRaC解决方法](//mod16.org/hurfdurf/?p=7)。

    * FPS理论沙盒：[frames-per-second.appspot.com](//frames-per-second.appspot.com)。

* 隔行扫描理论：

    * 一些随意的[CRT、NTSC和隔行扫描历史](http://foro.doom9.org/video-basics.htm)。

    * 关于[隔行扫描的一切 you never wanted to know](https://www.100fps.com)，[PDF](//yukisubs.files.wordpress.com/2016/11/what_is_deinterlacing_the_best_method_to_deinterlace_movies.pdf)。

    * [有关隔行电视、电影转换成视频和其他有趣的伎俩的本质](//hometheaterhifi.com/volume_7_4/dvd-benchmark-part-5-progressive-10-2000.html)。

* 编解码器位分配理论：

    * [了解速率控制模式（x264，x265）](http://slhck.info/video/2017/03/01/rate-control.html)，[PDF](//yukisubs.files.wordpress.com/2017/04/understanding_rate_control_modes_x264_x265.pdf)。

    * [CRF Guide (x264和x265的常数速率因子)](http://slhck.info/video/2017/02/24/crf-guide.html)，[PDF](//yukisubs.files.wordpress.com/2017/04/crf_guide_constant_rate_factor_in_x264_and_x265.pdf)。

    * 想要了解 x264 分辨率与比特率的关系，可以参考 [此指南](http://www.lighterra.com/papers/videoencodingh264)。这也涵盖了x264的设置。

* 分辨率理论与标准：

    * [本地分辨率和缩放](//kageru.moe/blog/article/resolutions)和[自动化脚本](https://github.com/Infiziert90/getnative)。

    * 关于分辨率标准的可疑链接：[随机文章](https://www.bestusbpoweredmonitor.com/2017/08/16/720p-vs-1080p-vs-1440p-vs-4k-vs-8k/)和 [另一篇文章](https://www.lifewire.com/720p-vs-1080p-a-comparison-1847332)。

    * 关于各种节目的[本地分辨率的博客](//anibin.blogspot.com/2017/07/blog-post.html)。

    * [缩放理论和算法](//www.cambridgeincolour.com/tutorials/image-interpolation.htm)，[Part 2](//www.cambridgeincolour.com/tutorials/image-resize-for-web.htm)。

    * 2018 年一篇有关将消费媒体提升到 4k 的技术的[状态更新](https://freetime.mikeconnelly.com/archives/1206)。

* 音频理论：

    * [音频频率和响度：第I部分-基础介绍](https://hometheaterhifi.com/technical/technical-reviews/audio-frequency-loudness-part-introduction-basics/)。

    * [真实音效与频率组成：第II部分](https://hometheaterhifi.com/technical/technical-reviews/real-sounds-frequency-composition-part-ii)。

* 编码和发布标准：这些存在的目的是确保客户端硬件解码兼容性。请注意，兼容性在动漫社区中并不受重视。

* 苹果的[通用作者要求](//developer.apple.com/library/content/documentation/General/Reference/HLSAuthoringSpec/Requirements.html#//apple_ref/doc/uid/TP40016596-CH2-SW1)。

  * Youtube的[推荐上传编码设置](//support.google.com/youtube/answer/1722171?hl=en)。

  * "场景" [发行标准](//scenerules.org)，适用于[动漫](//scenerules.org/n.html?id=2014_X264-ANIME.nfo)、[x264](//scenerules.org/n.html?id=2011_X264.2.nfo)、[DVDrips](//scenerules.org/n.html?id=2011_DVDR.nfo)、[BDrips](//scenerules.org/n.html?id=2010_BDr.nfo)。

  * 微软的[视频媒体类型](//docs.microsoft.com/en-us/windows/desktop/medfound/video-media-types)和[支持的格式](//docs.microsoft.com/en-us/windows/desktop/medfound/supported-media-formats-in-media-foundation)。

* 具体的指南（完全随机）：

* Koby / Finayra的具体[初学者指南](//tofincayra.wordpress.com/encoding/beginners-guide)，或现代A / V编码的“快速入门指南”。这个指南是TODO的翻译：[eXmendic's guide]也涵盖了16位滤波（高级）。

* 在Windows 64位上安装[HuffYUV](http://www.digitalfaq.com/forum/video-conversion/2193-cannot-install-huffyuv.html#post11627)。

* [Doom9 Forum](http://forum.doom9.org/index.php)和[指南索引](http://foro.doom9.org/guides.htm)。

* DVD视频对象的帧精确索引（.VOB）文件：[DGIndex](http://avisynth.nl/index.php/DGDecode)用于[AviSynth](http://avisynth.nl/index.php/Main_Page)。此外：请参见此[相关指南](//www.animemusicvideos.org/guides/avtech/videogetb2.html)。

* [小型编码的编码提示](https://sites.google.com/site/taumox/encoding-tips-for-mini-size)。

* [转换指南的随机索引](http://www.videohelp.com/guides/category/convert-articles-4;43)和Afterdawn的[指南索引](http://www.afterdawn.com/guides/guides_by_category.cfm)。

* [摄影监视器校准](//www.cambridgeincolour.com/tutorials/monitor-calibration.htm)。

* pixelblended的[AMV 101](https://pixelblended.com/amv101/en/)。

* l33tmeatwad的[软件列表](//www.animemusicvideos.org/forum/viewtopic.php?t=124965)和[AMVtool](https://github.com/l33tmeatwad/AMVtool)。

* DarkDream787的编码教程（PDF）：

  * [必需软件列表](//yukisubs.files.wordpress.com/2017/06/darkdream787-tutorials-required-software-list.pdf)。

  * 如何备份[DVD到HDD](//yukisubs.files.wordpress.com/2017/06/how-to-backup-dvds-to-hdd.pdf)和[蓝光到HDD](//yukisubs.files.wordpress.com/2017/06/how-to-backup-blu-rays-to-hdd.pdf)。

  * 如何从DVD [创建.SRT或.ASS字幕](//yukisubs.files.wordpress.com/2017/06/how-to-create-srt-or-ass-subtitles-from-dvd.pdf)和[从Blu-Rays](//yukisubs.files.wordpress.com/2017/06/how-to-create-srt-or-ass-subtitles-from-blu-rays.pdf)。

  * [如何从DVD / BD编码高质量音频](//yukisubs.files.wordpress.com/2017/06/how-to-encode-high-quality-audio-from-dvds-and-blu-rays.pdf)。

  * [如何使用AVISynth](//yukisubs.files.wordpress.com/2017/06/how-to-use-avisynth.pdf)。

  * [如何在MeGui中编码AVISynth脚本](//yukisubs.files.wordpress.com/2017/06/how-to-encode-avisynth-scripts-in-megui.pdf)。

  * [剪切-拆分-合并视频和音频](//yukisubs.files.wordpress.com/2017/06/cutting-splitting-merging-video-and-audio.pdf)。

  * [如何从视频，音频和字幕文件制作MKV文件](//yukisubs.files.wordpress.com/2017/06/how-to-make-an-mkv-file-from-video-audio-and-subtitle-files.pdf)。

* 随机软件列表：[请教有经验的编码人员](//dustorrent.com/community/show/ask-experienced-encoder-here)，[PDF](//yukisubs.files.wordpress.com/2016/10/ask_an_experienced_encoder.pdf)。

* 具体软件（靠近顶部表示更容易使用，靠近底部表示功能更全面）

  * [Handbrake](//handbrake.fr)，以及一个[相关指南](//lifehacker.com/5559007/the-hassle-free-guide-to-ripping-your-blu-ray-collection)。

  * vEncode[项目页](//github.com/gdiaz384/vEncode)和[发布](//github.com/gdiaz384/vEncode/releases)。注意：使用命令行界面（CLI）。

  * [MeGUI](http://www.videohelp.com/software/MeGUI)，[项目线程](http://forum.doom9.org/showthread.php?t=96032)，以及[指南](http://www.sevenforums.com/tutorials/104382-video-encoding-x264-megui.html)，[PDF](//yukisubs.files.wordpress.com/2016/10/video_encoding_x264_with_megui.pdf)。

  * StaxRip：[VideoHelp 页面](//www.videohelp.com/software/StaxRip)，[GitHub 项目页面](//github.com/stax76/staxrip)，以及[手册](//www.gitbook.com/book/stax76/staxrip-handbook/details)。

  * [Hybrid](http://www.videohelp.com/software/Hybrid)支持图形用户界面（GUI）。

    * FFMPEG：

       * 入门：[FFmpeg：终极视频和音频操作工具](//blog.superuser.com/2012/02/24/ffmpeg-the-ultimate-video-and-audio-manipulation-tool/)，[PDF](//yukisubs.files.wordpress.com/2017/04/ffmpeg_the_ultimate_video_and_audio_manipulation_tool.pdf)。

       * 入门2：[使用FFmpeg进行视频和音频转换指南](http://www.hongkiat.com/blog/ffmpeg-guide)。

       * [有用的FFmpeg 命令](http://www.labnol.org/internet/useful-ffmpeg-commands/28490)。

       * [FFmpeg和H.264编码指南](//trac.ffmpeg.org/wiki/Encode/H.264)。

       * [如何将字幕烧录到视频中](//trac.ffmpeg.org/wiki/HowToBurnSubtitlesIntoVideo)。

       * 官方[源和二进制文件](//ffmpeg.org/download.html)，[交叉编译Windows版](//trac.ffmpeg.org/wiki/CompilationGuide/CrossCompilingForWindows)，[编译助手](//github.com/rdp/ffmpeg-windows-build-helpers)，还有：nvenc编译指南和[3.2二进制文件]。

       * [FFmpeg维基](//trac.ffmpeg.org/wiki)，官方[晦涩难懂的文档](//ffmpeg.org/ffmpeg.html)，难懂的[Arch文档](//wiki.archlinux.org/index.php/FFmpeg)。

       * [创建多个输出的高级指南](//trac.ffmpeg.org/wiki/Creating%20multiple%20outputs)（同时进行480p、720p和1080p编码）。

  * [x264 项目页面](//www.videolan.org/developers/x264.html)，[文档](http://www.chaneru.com/Roku/HLS/X264_Settings.htm)，以及[二进制文件](//download.videolan.org/x264/binaries)。

  * [x265信息](http://x265.org)，[文档](//x265.readthedocs.io/en/default/introduction.html)和[二进制文件](http://msystem.waw.pl/x265)。

* 音频编码：

    * [FFMPEG 高质量音频指南](//trac.ffmpeg.org/wiki/Encode/HighQualityAudio)。

    * [eac3to](http://www.videohelp.com/software/eac3to)：带有许多图形用户界面（GUI）的命令行界面（CLI）音频编码工具。

    * DarkDream787的[如何从DVD / BD中编码高质量音频](//yukisubs.files.wordpress.com/2017/06/how-to-encode-high-quality-audio-from-dvds-and-blu-rays.pdf)。

    * Opus 编解码 [比较](//opus-codec.org/comparison) 和 [FAQ](//wiki.xiph.org/OpusFAQ)。

* 回放（计算机）：

  * 对于 DVD，诊断和保存网络流（而不是正常查看）：[VLC Media Player](//www.videolan.org/index.html)。

* 对于 Windows 用户，在以下选项中选择一个以自动安装 MPC 和 [LAV 滤镜](//www.videohelp.com/software/LAV-Filters-Megamix)：

      * [Combined Community Codec Pack (CCCP)](http://www.cccp-project.net)（体积小，但仅支持播放）

      * [K-Lite Codec Pack](//www.codecguide.com/download_k-lite_codec_pack_mega.htm)（Mega 版包含编码器的 VFW 滤镜）

      * [Kawaii Codec Pack (KCP)](http://haruhichan.com/forum/showthread.php?7545-KCP-Kawaii-Codec-Pack)

  * 如果安装了 K-Lite Codec Pack，则会自动安装 [MediaInfo](//sourceforge.net/projects/mediainfo)。否则，如果需要的话，可以手动安装。

  * [mpv](//mpv.io) 和 [预处理器](//github.com/bjin/mpv-prescalers) 是 MPlayer 的现代分支。mpv 的 [FAQ](//github.com/mpv-player/mpv/wiki/FAQ)，[Wiki](//github.com/mpv-player/mpv/wiki)， Moodkiller 的 [指南](//kametsu.com/topic/63120-mpv-made-easy-moodkiller-edition) 和 Kokomins 的 [指南](//kokomins.wordpress.com/2019/10/14/mpv-config-guide/)。 

     * [MPlayer](//www.mplayerhq.hu) 是跨平台的媒体播放器。ArchLinux 的[文档](//wiki.archlinux.org/index.php/MPlayer)，和官方的 [技术文档](//www.mplayerhq.hu/DOCS/HTML/en/index.html)

     * [SMPlayer](https://www.smplayer.info/) 是跨平台的媒体播放器，可以配置为 mpv 的包装器，并且界面与 MPC-HC 类似。

  * 关于 [LAV 拆分器流选择](https://1f0.de/lav-splitter/lav-splitter-stream-selection/) 的高级提示。

  * [madVR](http://madvr.com)，[FAQ](http://forum.doom9.org/showthread.php?t=146228)，是 GPU 加速的“渲染器”，可以以比默认设置更高的保真度显示视频。它还支持实时滤镜，用于锐化、颜色校正和其他操作。该实现是一个用于各种播放器（包括 MPC-HC 和 mpv）的 Windows 插件。在使用 K-Lite Codec Pack 自动安装或手动安装后，必须在播放器中选择使用它，因此需要按照以下指南进行操作：

     * Kametsu 指南 [MPC-HC + LAV/madVR/xy-subfilter](//kametsu.com/topic/58428-guide-installing-mpc-hc-with-madvr-lavfilters-xysubfilter-and-icaros).

     * 或者适用于 mpv 的指南：[Scum's Raws 指南](//iamscum.wordpress.com/videoplayback-guide)。

     * 更多指南 ：[ranpha's PotPlayer 指南](//imouto.my/tutorials/configuring-potplayer-for-gpu-accelerated-video-playback-with-dxva-or-cuda-and-also-high-performance-software-decoding/)，[BakaBT Wiki](http://wiki.bakabt.me/index.php/Hi10P)，[CoalGirls - 2011](//coalgirls.wakku.to/faq/playback/setup-guide-for-mpc-hc-madvr)，[另一个](//shittastes.wordpress.com/tutorials/properly-installing-and-setting-up-mpc-hc/) 和最后一个 [Nand 的指南](http://haruhichan.com/wpblog/205/hi10p-info-guide/)，[镜像](http://archive.is/VnjWi)，[PDF](//yukisubs.files.wordpress.com/2018/02/hi10pforanimefans_and_playbackguide_bynand_haruhichan.pdf)。

     * 高级指南：ranpha 的非常详细的 [madVR 设置配置指南](//imouto.my/tutorials/madvr/)，[PDF](//yukisubs.files.wordpress.com/2018/02/madvrconfiguration_-by_ranpha.pdf)。

* 播放（家庭影院电视计算机）：

    * 遥控器：使用 [这个](//www.amazon.com/Windows-Control-Infrared-Receiver-Ultimate/dp/B00224ZDFY/ref=sr_1_1?ie=UTF8&qid=1334779407&sr=8-1)，或

    * 无线键盘：[Logitech 无线键盘带触摸板](//www.amazon.com/s/ref=nb_sb_noss?url=search-alias%3Delectronics&field-keywords=logitech+wireless+keyboard+with+touchpad)，[迷你版](//www.ebay.com/sch/i.html?_from=R40&_trksid=p2380057.m570.l1313.TR12.TRC2.A0.H0.Xmini+wireless+keyboard.TRS0&_nkw=mini+wireless+keyboard&_sacat=0)。

    * 对于专用 HTPC 盒子：[Kodi](//kodi.tv)（以前称为 XBMC）。

        * 注意：Raspberry Pi 3 B 不能正确解码 10 位内容。

        * 值得注意的变体：[LibreElec](//libreelec.tv)，[OpenElec](http://openelec.tv/)，[Plex](//www.plex.tv)。

* 对于客户端/服务器模型（推荐）：可以选择[Plex](//www.plex.tv)（闭源）或[Emby](//emby.media)（开源）。

  * Plex/Emby的实时转码（免费）意味着所有客户端设备都可以正确解码流（具有通用兼容性，包括HTML5网页浏览器）。

  * 值得注意的变体：[RasPlex](http://www.rasplex.com)、[Kodi Plex插件](//kodi.tv/plex-add-on-for-kodi)和Xbox 360的Plex客户端。

  * Plex的[全客户端列表](//forums.plex.tv/discussion/190573/list-of-current-client-product-and-client-platform)。

  * Emby的[Kodi插件](//emby.media/emby-for-kodi.html)、[存储库](//github.com/MediaBrowser/plugin.video.emby/wiki/Emby-Repository)（用于安装依赖项）和[全客户端列表](http://emby.media/download.html)。

* 随机推荐：

  * [Rasplex](http://www.rasplex.com/)

  * [OpenElec上的Kodi](//openelec.tv/)

  * [Raspbian](//www.raspbian.org)

  * [RetroPi](//retropie.org.uk)

  * 或者只需使用一个[高清晰度多媒体接口](http://www.hdmi.org/consumer/hdmi_advantage.aspx)（HDMI）电缆（音频+视频）将笔记本电脑与电视临时连接。[HDMI 常见问题解答](http://www.hdmi.org/learningcenter/faq.aspx)

* QC (?): [Bitrate Viewer](http://www.winhoros.de/docs/bitrate-viewer) 能够估算MPEG1和MPEG2流的质量。我不知道这有什么用处，但Etzimal让我添加了它。o_o*

#### 多路复用和解复用

  * 理论：对于多路复用，其想法是将多个离散的文件（视频、音频、字幕、字体）合并到一起，以便进行播放。对于解复用，其想法是从包含多个流的文件中提取出至少其中的一个流。

  * 多路复用通常是指缩短、延长或延迟流以实现同步。缩短和延迟与流复制技术兼容。然而，流中任何长度的增加或修改通常需要对整个流进行转码。因此，这两个任务（编码和多路复用）有一定的重叠。

  * 解复用通常是必要的以获得需要的来源，可以视为捕获部分的一部分。

  * 通常使用的容器要么是带软字幕、字体和可能有多个音频流的[Matroska](//www.matroska.org/technical/whatis/index.html)(.mkv)，要么是带有硬编码字幕和一个音频流的标准MPEG-4(.mp4)容器。

  * 多路复用工具：

  * FFMPEG:

      * 阅读以下开关的说明：-ss, -t, -to在[FFMPEG文档](//ffmpeg.org/ffmpeg.html#Main-options)和[这个指南](//trac.ffmpeg.org/wiki/Seeking)中。

      * 使用-map开关从多流文件中提取非第一个流。[FFMPEG文档](//ffmpeg.org/ffmpeg.html#Advanced-options)和相关指南[引导](//trac.ffmpeg.org/wiki/Map)。

  * [MKVToolNix](//mkvtoolnix.download/index.html)：

    * [VideoHelp概述](//www.videohelp.com/software/MKVtoolnix)。

    * 下载: [Windows/OS-X](//www.fosshub.com/MKVToolNix.html), [Linux](//mkvtoolnix.download/downloads.html)。

    * 必需附加组件：gMKVExtractGUI。[项目页面](http://forum.doom9.org/showthread.php?t=170249)和[下载链接](//sourceforge.net/projects/gmkvextractgui/files/latest/download)。

    * MKVMerge的[CLI文档](//mkvtoolnix.download/doc/mkvmerge.html)。

    * 进阶：[创建多部分文件](http://forum.videohelp.com/threads/359121-How-to-extract-cut-parts-from-a-mkv-including-all-audio-and-subtitle-tracks)，[合并多部分文件](//forums.plex.tv/discussion/178888/howto-joining-multi-part-movies-files-with-mkvtoolnix-gui)。

    * 进阶：[有序章节](https://forums.animesuki.com/showthread.php?t=66444) (OC)概述。请不要使用有序章节。

       * [实现细节](//mod16.org/hurfdurf/?p=8)，[第2部分](//mod16.org/hurfdurf/?p=14)。

       * 为尝试修复OC：[UnlinkMKV](//github.com/gnoling/UnlinkMKV)。

    * 在处理可变帧率(VFR)时，使用[外部时间戳文件](https://mkvtoolnix.download/doc/mkvmerge.html#mkvmerge.external_timestamp_files)处理视频比特流。 

  * DVDs:

* [DVD-Decrypter](http://www.videohelp.com/software/DVD-Decrypter)，[Mega](//mega.nz/#F!wUYwDSgA!8tx_37HUBcs9KqPhkk5FmQ)，+ [流处理指南](http://www.doom9.org/index.html?/dvddec.htm)。先决条件：DVD-Decrypter需要从像[Virtual CloneDrive](//www.elby.ch/en/products/vcd.html)或物理DVD等光学设备中工作。如果Video_TS文件夹可用（即DVD副本），则使用可以制作ISO文件的软件，如[CDBurnerXP](//cdburnerxp.se/en/download)。

      * DGIndex，DGDecode的一部分（http://avisynth.nl/index.php/DGDecode），[dgmpgdec158.zip]（//mega.nz/#F！wUYwDSgA！8tx_37HUBcs9KqPhkk5FmQ）。

  * BDs：

     *转储内容后，大多数bdmv不需要特殊的解复用工具来处理。ffmpeg和mkvtoolsnix通常足够，但可以使用复用工具来加速处理。

     * [tsMuxer]（http://www.videohelp.com/software/tsMuxeR），[Mega]（//mega.nz/#F！wUYwDSgA！8tx_37HUBcs9KqPhkk5FmQ）。替代FFMPEG用于复用传输流（.ts或.m2ts）并支持解析蓝光索引（mpls）。

     * [HD-DVD / Blu-Ray Stream Extractor]（http://www.videohelp.com/software/HD-DVD-Blu-Ray-Stream-Extractor），[Mega]（//mega.nz/#F！wUYwDSgA！8tx_37HUBcs9KqPhkk5FmQ）。tsMuxer的替代品。建议同时使用以上两种。

     *注意：以上两种都需要[eac3to]（http://www.videohelp.com/software/eac3to）。

  * [MKV-Cutter]（https://www.videohelp.com/software/MKV-Cutter）（未经测试）。

  * 指南：

     * OblivionShadow和kantai.subs.moe的[高级子站合并和复用指南指南-PDF]（//kantai.subs.moe/wp-content/uploads/2016/08/Aegisub-Merging-and-Muxing-Guide.pdf），[PDF]（//yukisubs.files.wordpress.com/2018/02/aegisub_merging_and_muxing_guide_by_oblivionshadow.pdf）。

     * Baal的[如何：使用Audacity同步两个音轨进行复用]（//kametsu.com/topic/45949-how-to-synchronize-two-audio-tracks-for-muxing-with-audacity）。

     * Catar的[Muxed Releases的标准]（//kametsu.com/topic/62012-the-ctr-muxing-standards-guide）。注意：重点是媒体服务器兼容的双音轨版本。

#### 过滤

*前言：为了避免多次转码或传输无损编码的视频，理想情况下，过滤和编码应由同一人完成。

*理论：超出[IVTC]（http://foro.doom9.org/ivtc-tut.htm）的过滤任务可以视为编码器的可选子任务。常见过滤任务包括裁剪长度，切除广告，纠正各种工作室错误和提高主观视觉质量。

*担心兼容性的编码器还需要将OP / ED或整个脚本硬字幕到Distro之前的视频流中。这可以在过滤或编码阶段完成。

*除了基本任务外，过滤的回报递减。学习和实施都需要很长的时间。

*更多理论：

*RX Mastering的[视频哲学]（https://rxmastering.wordpress.com/video）。

*[数字噪音消除的背景和示例]（http://www.cinedrome.ch/hometheater/dvd/dnr）。

*理论和示例混合：[Digital ICE]（//www.youtube.com/watch?v=E0LVjGp1Wtc）（YouTube）。

*示例：

* 视频修复: [Avisynth的力量三部曲](https://vimeo.com/11133342) 和 [数字化的8毫米胶片](https://vimeo.com/49963017) (vimeo).

    * [精灵之书](http://compare.bakashots.me/compare.php?setId=2089), [KissXSis OVA](http://compare.bakashots.me/compare.php?setId=1973&comparisonId=12625), [超次元游戏海王星](http://compare.bakashots.me/compare.php?setId=2028&comparisonId=13099) (虽然过度处理但无所谓)。

    * Moozzi2的Rakudai [前](//yukisubs.files.wordpress.com/2016/10/moozzi2_rakudai_1_before.png)和[后](//yukisubs.files.wordpress.com/2016/10/moozzi2_rakudai_1_after.png)。

    * 细微的过滤器示例：[案例研究：高达拼图](//rxmastering.wordpress.com/2014/12/03/case-study-turn-a-gundam/)。

    * [NeatVideo](//www.neatvideo.com/examples) - 类似于 AviSynth 的 [TemporalDegrain()](http://avisynth.nl/index.php/Temporal_Degrain)。

    * [用 AviSynth 过滤器提高视觉品质](https://www.animemusicvideos.org/guides/avtech31/post-qual.html)、 [PDF](//yukisubs.files.wordpress.com/2016/10/amv_post_production_-_visual_quality.pdf) 。

    *  [使用过滤器和函数](http://www.l33tmeatwad.com/vapoursynth101/using-filters-functions) (Vapoursynth)。

* 理解和识别工件:

  * [了解视频压缩工件](http://blog.biamp.com/understanding-video-compression-artifacts/)。

  * [宏块 vs 蚊子噪声](https://hometheaterhifi.com/volume_12_1/algolith-mosquito-video-noise-reducer-3-2005.html)。

  * [景深](//www.cambridgeincolour.com/tutorials/depth-of-field.htm)和[超焦距距离](//www.cambridgeincolour.com/tutorials/hyperfocal-distance.htm)理论。

  * [了解相机镜头](//www.cambridgeincolour.com/tutorials/camera-lenses.htm)。

     * 在过滤时使用错误的颜色矩阵可能导致“对比度降低”或“暗角”。

     * 放大会产生“模糊”。

     * 曲面锐化和稳定会产生“畸变”。

     * 不合适的捕捉设置或设备，尤其是对于模拟视频，可能会产生“色差”或“彩虹状失真”。

  * [数字相机图像噪声-第1部分](//www.cambridgeincolour.com/tutorials/image-noise.htm)和[第2部分](//www.cambridgeincolour.com/tutorials/image-noise-2.htm)。

  * [图像锐化指南](//www.cambridgeincolour.com/tutorials/image-sharpening.htm)。

  * 待办事项：点爬行、带状

* 框架：

    * [AviSynth](http://avisynth.nl/index.php/Main_Page)：

        * [AviSynth+](http://avs-plus.net/) （64位）和 Github [发行页面](//github.com/pinterf/AviSynthPlus/releases)。

        * l33tmeatwad 的 [AviSynth 101](http://www.l33tmeatwad.com/avisynth101)。

        * [Scintilla's Guide to AviSynth Postprocessing Filters](http://www.aquilinestudios.org/avsfilters/index.html)、 [PDF](//yukisubs.files.wordpress.com/2016/10/scintilla_guide_to_avisynth_postprocessing_filters.pdf)。

* [Filtering the PPP way](https://www.otakubell.com/?page_id=291) by erik.

    * 句法: 

        * [我的第一个AviSynth脚本](http://avisynth.nl/index.php/First_script), 和 [FAQ](http://avisynth.nl/index.php/AviSynth_FAQ).

        * [脚本样例](http://avisynth.nl/index.php/Script_examples), 以及另一个 [随机样例](http://pastebin.com/jDuP5STF) (虽然过度过滤但无论如何).

        * AviSynth [CopyFromMe 模板](//gist.github.com/YukinoAi/36a9f4c0deb193b1113c8fd10d5d8fc7).

        * 一个高级的 [16位过滤模板](//tofincayra.wordpress.com/encoding/basic-avisynth-script).

    

    * 过滤列表: 

        * [内部过滤器](http://avisynth.nl/index.php/Internal_filters).

        * [外部过滤器](http://avisynth.nl/index.php/External_filters).

        * [MSU 公共过滤器](http://www.compression.ru/video/public_filters.htm).

        * real.finder 的 [索引](//forum.doom9.org/showthread.php?t=174121).

        * josemaria.alkala 的 [随机x86过滤器](//bitbucket.org/josemaria.alkala/avisynth_filters/src).

        * StainlessS 的 [代码库](//www.mediafire.com/folder/hb26mthbjz7z6/StainlessS).

    

    * 杂项:

        * [nnedi3](http://avisynth.nl/index.php/Nnedi3), [二进制文件](https://github.com/jpsdr/NNEDI3/releases/)和 [nnedi3_resize16](https://www.nmm-hd.org/newbbs/viewtopic.php?f=7&t=1117). "[...]NNEDI3最初被设计为一种 intrafield 退隔带工具，也可以用于以2的幂扩大图像[...]与早期的NNEDI版本相比，v3具有改进的预测神经网络架构和本地近邻预处理。NNEDI3的神经网络由16到256个神经元组成。32个神经元通常具有性能的最佳质量。" -[src](https://freetime.mikeconnelly.com/archives/1206)

        * [Hysteria](//www.animemusicvideos.org/forum/viewtopic.php?t=101471). 线性调节器.

        * ["Tweak" 指南](http://avisynth.nl/index.php/Tweak) 用于对颜色进行微调。提示: 使用maxsat=15-35.

        * [直方图](http://avisynth.nl/index.php/Histogram), [另一个](http://avisynth.nl/index.php/Histograms_in_RGB_%26_CMY). 用于分析颜色家族中的颜色偏移，而不需要分开的亮度。

        * [Smooth Video Project (SVP)](https://www.svp-team.com/wiki/Download), [手册](//www.svp-team.com/wiki/Manual:SVPflow), 用于帧插值。也适用于VapourSynth。

        * [SmoothAdjust](//forum.doom9.org/showthread.php?t=154971). 进行YUV颜色调整。另请参见: [Autolevels](http://www.thebattles.net/video/autolevels_comparison.html) 和 [GamMac](//forum.doom9.org/showthread.php?t=173695), [2](http://www.filmshooting.com/scripts/forum/viewtopic.php?t=27143).

        * [WhiteBalance](http://avisynth.nl/index.php/WhiteBalance).

        * [AviSynth着色器](//github.com/mysteryx93/AviSynthShader). 用于运行未本地移植的HLSL像素着色器。

        * [TemporalDegrain2](//forum.doom9.org/showthread.php?s=4c6011fbc9f07c5bdbced4d27dce5cdd&t=175798).

    * [VapourSynth](http://www.vapoursynth.com/about/)：与许多交叉兼容的过滤器一起使用的AviSynth替代品。需要[Python 3.8](//www.python.org/downloads/release/python-385/)。        

* l33tmeatwad的[VapourSynth 101](http://www.l33tmeatwad.com/vapoursynth101)和[使用滤镜与函数](http://www.l33tmeatwad.com/vapoursynth101/using-filters-functions)。

        * 官方文档的[安装](http://www.vapoursynth.com/doc/installation.html)和[入门指南](http://www.vapoursynth.com/doc/gettingstarted.html)。l33tmeatwad的[VapourSynth安装指南](//www.animemusicvideos.org/forum/viewtopic.php?t=125039)。

        * eXmendiC的[VapourSynth滤镜](//iamscum.wordpress.com/encoding-stuff/filtering-with-vapoursynth)和[PDF文件](//yukisubs.files.wordpress.com/2017/09/filtering_with_vapoursynth_by_exmendic.pdf)。

        * Ausna / Yuuki的[Vapoursynth + x265](https://blog.mxpkx.com/index.php/archives/144/)，[PDF-英文](https://yukisubs.files.wordpress.com/2020/04/vapoursynth_x265_by_yuuki.pdf)，安装指南。

        * 使用[vspipe.exe](http://www.vapoursynth.com/doc/vspipe.html)从.vpy文件中进行编码。选项：

            1. 参见[此指南](//iamscum.wordpress.com/encoding-stuff/x264-encoding-with-vapoursynth)。

            2. 使用ffmpeg / x264 / x265前端，例如[vEncode](//github.com/gdiaz384/vEncode)，该前端包含vspipe.exe。有关替代方案，请参见“编码：特定软件”部分。

            3. 在.avs文件中交错.vpy，然后编码为普通的.avs文件。请参阅[VapourSource](http://avisynth.nl/index.php/VapourSource)。

        * 滤镜列表：

            * [官方插件列表](http://www.vapoursynth.com/doc/pluginlist.html)（包括[BM3D](//github.com/HomeOfVapourSynthEvolution/VapourSynth-BM3D)和[waifu2x-caffe](//github.com/HomeOfVapourSynthEvolution/VapourSynth-Waifu2x-caffe)）。

            * VapourSynth Evolution的[滤镜索引](//github.com/HomeOfVapourSynthEvolution)。

            * HolyWu的[HAvsFunc移植的功能列表](//forum.doom9.org/showthread.php?t=166582)。

            * Irrational-Encoding-Wizardry的[Github首页](//github.com/Irrational-Encoding-Wizardry)。座右铭：“一群自闭症患者为麻瓜改进编码。”

            * vfrmaniac的[“作品”索引](https://vfrmaniac.fushizen.eu/works/)（包括FFT3DFilter二进制文件）。

            * [InsaneAA](//github.com/Beatrice-Raws/VapourSynth-insaneAA)。

        * Vapoursynth的[CopyFromMe模板](//gist.github.com/YukinoAi/fa90db376296d5673fd2a2f0e4442ee3)。

        * BeatriceRaw的[encode-scripts](//github.com/Beatrice-Raws/encode-scripts)，相关的Sword Art Online II[示例脚本](//github.com/Jensenbeatrice/Sword-Art-Online-II-scripts)。

    * [VirtualDub](http://virtualdub.org/index.html)，[v2](//www.videohelp.com/software/VirtualDub2)：

        * [有趣的历史](http://www.virtualdub.org/virtualdub_history.html)。

        * 对于稳定：[Deshaker](http://www.guthspot.se/video/deshaker.htm)，[PDF](//yukisubs.files.wordpress.com/2018/02/deshaker-video-stabilizer.pdf)。

            * [随机YouTube视频](//www.youtube.com/watch?v=nIo_AuYRVj0)关于Deshaker

            * 待办事项：此处放置一些理智的示例设置。

       * 颜色校正：[ColorMill](http://fdump.narod.ru/rgb.htm)和[指南](http://www.infognition.com/tutorials/color_correction/)。

* 使用的其他程序：    

* [AvsPmod](//avspmod.github.io)，AviSynth和VapourSynth的集成开发环境（IDE）。 todo：在此处放置其他DDL链接。

    * VapourSynth编辑器（vsedit），VapourSynth的替代IDE。[线程](//forum.doom9.org/showthread.php?t=170965)和[项目页面](//bitbucket.org/mystery_keeper/vapoursynth-editor)。

    * [Yunno](//yuuno.encode.moe) = [Jupyter](//jupyter.org) + VapourSynth。用于vsedit的替代IDE。额外依赖项：[Jupyter](//jupyter.org/install.html)和[iPython](//ipython.readthedocs.io/en/stable/install/index.html)。

    * 注意：[MPC-x86-Portable](//mpc-hc.org/downloads)，或者如果使用AviSynth+，则使用64位版本可以直接加载.avs文件。

    * Waifu2x用于升频和/或去噪。

       * 请参阅[合并示例结果](http://diff.pics/nmS9GmlpSUV7/5)和[仅上采样组件的示例](//diff.pics/vJ5W2v4l0q9y/1)。

       * 注意：某些Waifu2x的caffe版本可以使用nvidia的CUDA Deep Neural Network（CUDNN）库而不是OpenCL / AVX。这些版本更快，但需要64位Windows，[支持CUDNN的GPU](//developer.nvidia.com/cuda-gpus)，即计算能力3.0+，以及[nvidia_CUDNN.dll.7z](//mega.nz/#F!wUYwDSgA!8tx_37HUBcs9KqPhkk5FmQ)。大多数版本还有“仅CPU”模式。

       * [waifu2x-caffe-VapourSynth](//github.com/HomeOfVapourSynthEvolution/VapourSynth-Waifu2x-caffe)适用于VapourSynth的变体，支持CUDA / CUDNN。

       * [waifu2x-caffe-VapourSynth-w2xc](//github.com/HomeOfVapourSynthEvolution/VapourSynth-Waifu2x-w2xc)适用于VapourSynth的变体，支持OpenCL 1.2。

      * [waifu2x-caffe](//github.com/lltcggie/waifu2x-caffe)独立版，支持CUDNN，可以作为视频的图像序列工作。重要提示：此版本还包含上面的VapourSynth变体所需的/models文件夹。

      * [waifu2x-converter-cpp](//github.com/tanakamura/waifu2x-converter-cpp)和[DeadSix27的Fork](//github.com/DeadSix27/waifu2x-converter-cpp)是旧版的CLI独立（无框架）CUDA / OpenCL / AVX实现。 [koroshell GUI](http://inatsuka.com/extra/koroshell/)。

      * [AutoWaifu](//autowaifu.azurewebsites.net)。

* 深入阅读：

    * [kageru.moe/blog/encode](//kageru.moe/blog/encode/)。

    * 摘要：[Javascript Video Filtering](//tp7.github.io/articles/javascript-video-filtering)。

* 场景滤镜：这是过滤的可选子组件，是编码的可选子组件，是捕获的可选子组件。换句话说，要远离。

    * 基本：frameTools的sceneFilter()。请参阅[文档](//github.com/gdiaz384/frameTools)和[发布页面](//github.com/gdiaz384/frameTools/releases)。

    * 更有效且推荐：tp7的[Efficient scenefiltering with AviSynth](//tp7.github.io/articles/scenefiltering)，[PDF](//yukisubs.files.wordpress.com/2017/09/efficient-scenefiltering_with_avisynth_by_tp7.pdf)。

        * [RemapFrames](http://avisynth.nl/index.php?title=RemapFrames)，[PDF指南](//yukisubs.files.wordpress.com/2018/02/remapframes_041.pdf)，Groucho的[AviSynth二进制](https://forum.doom9.org/showthread.php?t=173259)和Frechdachs的[VapourSynth脚本](//gist.github.com/Frechdachs/353f6917d78bb99d93bfcea0f29062ed#file-fvsfunc-py-L822)。

* 使用图片组（GOP）：场景过滤也可以在[Photoshop](//www.photoshop.com/products/photoshopelements)或[Gimp](//www.gimp.org)中逐帧完成。手动编辑每个帧可以描述为场景过滤的可选组件。

* 必读：[Understanding FFMPEG's Group of Pictures (GOP) Options](//esoterictek.blogspot.com/2017/04/understanding-ffmpegs-group-of-pictures.html)。

* 剑桥色彩的[照片编辑教程](//www.cambridgeincolour.com/photo-editing-tutorials.htm)和[数字照片修复](//www.cambridgeincolour.com/tutorials/digital-photo-restoration.htm)。

* Adobe的Photoshop [Retouch and repair photos](//helpx.adobe.com/photoshop/using/retouching-repairing-images.html)用户指南。

* 重新激活平移场景：

    * 这可以用来修复卡顿和闪烁问题。

    * [全景基础知识](//www.cambridgeincolour.com/tutorials/digital-panoramas.htm)

    * [如何自动对齐层](https://www.dummies.com/software/adobe/photoshop/how-to-auto-align-layers-in-photoshop-cs6/)

    * [使用内容感知填充](//www.youtube.com/watch?v=nXVY92gazvE)，YouTube视频。 此时，可以切换到Premiere/Blender。

    * [如何在Photoshop CS6中平移和缩放](https://www.youtube.com/watch?v=kM5pIHS5j74)，YouTube视频。

* 示例：也许不太理智的[流程图](//i.imgur.com/RGoR1mV.png)。将其视为不要这样做的示例。

* 特别注意：在YUV和RGB之间转换时，请通过工作流程的每个步骤手动双重检查颜色失真，其中包括在使用waifu2x和BM3D等降噪算法时（包括在mvsfunc的封装中使用它时）。

* 导出/导入图像：

    * FFMPEG图像序列[指南1](//en.wikibooks.org/wiki/FFMPEG_An_Intermediate_Guide/image_sequence) ，[指南2](http://hamelot.io/visualization/using-ffmpeg-to-convert-a-set-of-images-into-a-video/) ，[指南3](//trac.ffmpeg.org/wiki/Create%20a%20video%20slideshow%20from%20images)。

    * [VirtualDub](http://www.virtualdub.org/blog/pivot/entry.php?id=34)“文件—打开视频文件...”或“文件—导出—图像序列...”（不建议使用）。

    * [mplayer示例](https://superuser.com/questions/135117/how-to-convert-video-to-images) ，并查看MPlayer的[Video Output Drivers（仅限MPlayer）文档](//www.mplayerhq.hu/DOCS/man/en/mplayer.1.html#VIDEO%20OUTPUT%20DRIVERS%20%28MPLAYER%20ONLY%29)的-vo“jpeg”或“png”部分（不建议使用）。

    * AviSynth：

        * [图像编写器](http://avisynth.nl/index.php/ImageWriter).

        * [图像阅读器](http://avisynth.nl/index.php/ImageReader)。（糟糕的）

        * [CoronaReader](http://avisynth.nl/index.php/ImageSequence)。（也很糟糕）

        * [语法示例](//gist.github.com/YukinoAi/bb053f9e4d65155d3123ead9fa03a18e)。

* 图像查看器：[InfranView](//www.irfanview.com)或您喜欢的图形HTTP客户端。

* 批量图像处理：[Photoshop宏](//helpx.adobe.com/photoshop/using/creating-actions.html)，[ImageMagick](//www.imagemagick.org/script/command-line-processing.php)（非常高级）和[waifu2x-caffe](//github.com/lltcggie/waifu2x-caffe)。

* Masktools：

    * [Masktools](http://avisynth.nl/index.php/MaskTools2)，[PDF](//yukisubs.files.wordpress.com/2018/02/masktools2_-_avisynth_wiki.pdf)，提供了一种有效的方法来选择视频帧的部分部分而不涉及其它部分。 如果与其他概念（如运动补偿和边缘检测）结合使用，masktools允许过滤器有选择地针对许多连续帧内的单个帧的各个方面。 既不是基于剪辑的场景过滤技术，也不是图像编辑技术提供了Masktools可以提供的灵活性和效率。

    * tp7的[MaskTools 2理论](//tp7.github.io/articles/masktools)，[PDF](//yukisubs.files.wordpress.com/2018/02/masktools_2_by_tp7.pdf)。

    * tp7的MaskTools入门和普及：俄语翻译：[PDF](//yukisubs.files.wordpress.com/2018/02/masktools_for_beginners_and_generally-tp7.pdf)。 链接：

        * http://web.archive.org/web/20160312025423/http://tp7.ruanime.org/masktools/index.html

* 06_taro的[MaskTools指南](https://www.nmm-hd.org/newbbs/viewtopic.php?f=7&t=770)。从中文翻译[PDF - 第1页](//yukisubs.files.wordpress.com/2018/02/tutorial_masktools_getting_started_tutorial_-nmm-hd_1.pdf)和[PDF - 第2部分](//yukisubs.files.wordpress.com/2018/02/tutorial_tutorial_for_masktools_-_page_2_-_nmm-hd.pdf)。

    * 进一步阅读：[Vapoursynth中的Edge Masks](https://kageru.moe/blog/article/edgemasks/)，作者为[Kageru](//github.com/kageru)。

* 实时滤镜：这个想法是在不转码视频的情况下进行播放。

  * [SmoothVideo Project (SVP)](//www.svp-team.com/wiki/Main_Page)，[示例](//www.youtube.com/watch?v=4J1PYWCJ6tE)，用于将帧插值到60fps。注意：Avisynth/Vapoursynth插件也可用。

  * 媒体播放器GPU加速的“着色器”：[MPC-HC](https://forum.videohelp.com/threads/372235-Is-there-a-way-to-Paste-MPC-HC-shader-effect-to-a-video)，[mpv]。包括锐化和缩放滤镜。

  * MadVR拥有很多滤镜。

  * 如果计算机足够强大且滤镜链足够轻，.avs文件（AviSynth）可以直接播放。

#### 翻译（TL）+校对（TLC）

* 转写：将文字（可能还包括语法）改成另一种语言。

vs

* 翻译：改变所说的话，包括隐喻，传达相同的含义。

#### 编辑+质量检查（QC）

* 编辑：编辑确保翻译易于理解，自然，一致，适应本地化或非本地化（取决于偏好）。

* 编辑的唯一要求是必须能够流利地说目标语言，这可能是一个高门槛。

* 我个人也会听外语音频，以确保校对后的对话尽可能符合文字意思，同时确保对话的选词和排版与[速读](//en.wikipedia.org/wiki/Speed_reading)技巧兼容。

* 随机：为了理解，单词中字母的顺序并不重要，因为人脑可以很好地识别模式。速读是相同的概念，但应用于句子而不是单词。英语中的“视觉阅读”中，较短的单词（如to、a、be、are、by）是可以通过解析只有较长的单词来略过的语法。任何“缺失”的含义都可以从上下文中得出。尝试通过跳过所有较小的单词来阅读。如果句子没有意义，则更改顺序和使用的单词，使其有意义。在这种情况下，缩略语是不好的。

* tun的[粉丝字幕编辑指南](http://m33w-fansubs.com/editing-guide)，[PDF](//yukisubs.files.wordpress.com/2018/02/fansub_editing_guide_by_tun.pdf)。

* [Collectr](//collectr.blogspot.com)的编辑技巧：

   * [编辑的傲慢指南](//collectr.blogspot.com/2011/01/collectrs-curmudgeonly-guide-to-editing.html)，[PDF](//yukisubs.files.wordpress.com/2017/09/collectr_blogs_curmudgeonly_guide_to_editing.pdf)。

   * [编辑极简主义](//collectr.blogspot.com/2013/10/editorial-minimalism.html)，[PDF](//yukisubs.files.wordpress.com/2017/09/collectrs_blog_-editorial_minimalism.pdf)。

* [Second Hand Translations的危险性](//collectr.blogspot.com/2012/12/the-dangers-of-second-hand-translations.html)，[PDF](//yukisubs.files.wordpress.com/2017/09/collectrs_blog_the_dangers_of_second-hand_translations.pdf)。

* 重要提示：要确定你喜欢哪种类型的编辑方式。1）标准非正式英语，2）非本地化直译，或3）本地化的meme字幕。[PNG指南](//yukisubs.files.wordpress.com/2017/09/editing_style_comparison-mod.png)。总结如下：

    1. 非本地化-直译：Doki/Eclipse。

    2. 官方标准或非正式英语：Crunchyroll、Funimation、正式发行的DVD-BD是次要来源。

    3. 本地化：Commie/DesuYo/FFF是高度本地化的meme字幕。除非你明确喜欢本地化，否则要避免使用它们。当与上述1-2的对话结合在一起时，它们是良好的标记排版来源。

    4. Hadena字幕非常糟糕，甚至到了不再有趣的地步，甚至变得有趣。 

        * 注意：这里的重点不是评论Hadena，而是反对编辑极简主义。如果字幕很好，请不要改动它们，但如果它们真的很糟糕，那么就要全部更改。

    5. 很多重新混流的人会将现有的字幕与更好/更差的音频和视频（A/V）相结合。字幕质量通常与他们复制的来源相同。

    6. 在对话和A/V中存在审查（性与暴力），请谨慎对待广播流，特别是非日本语流以及旧版DVD。

* 使用Crymore的[翻译对抗](http://www.crymore.net/category/translation-party/)来确定你喜欢哪种编辑方式，从[这个](http://www.crymore.net/2016/01/18/translation-party-commie-vs-doki-chihiro-vs-funimation-vs-mori-dagashi-kashi-episode-01)开始。虽然需要一段时间，但后面可以节约时间，因为可以从“更好”的字幕开始，并且不需要总体编辑太多。

* 关于粉丝翻译的戏剧和编辑的博客：[crymore.net](//www.crymore.net)。

* QC：[Collectr的挑剔指南](https://collectr.blogspot.com/search/label/QC)。

#### 时间轴

* 其他名称/子类别：原始时间轴、精确定时、场景定时、关键帧定时（KFT）、卡拉OK定时（K-Timing）。

* [时间轴理论](//collectr.blogspot.com/2012/05/its-all-in-timing.html)，[PDF](//yukisubs.files.wordpress.com/2017/09/collectrs_blog_its_all_in_the-timing.pdf) by Collectr。

* unanimated的[定时基础知识](//unanimated.github.io/timing-basics.htm)、[无TPP定时](//unanimated.github.io/timing-without-tpp.htm)和[附加说明](//unanimated.github.io/timing-notes.htm)。unanimated的[粉丝翻译指南](//unanimated.github.io/guides.htm)。

* Doki的[时间轴指南](//doki.co/support/doki-timing-guide)，[PDF](//yukisubs.files.wordpress.com/2016/10/doki_timing_guide.pdf)。

* Sally的[Sally动画定时指南](//drive.google.com/open?id=0B0O0wI7T8vtSSldlZHJnUVJaTTA)，[PDF](//yukisubs.files.wordpress.com/2017/09/sallys_guide_to_timing_anime.pdf)，[GDrive - PDF](//drive.google.com/open?id=0B0O0wI7T8vtSMTBtRDlFNkxIdEE)。

    * 资源：[GoogleDrive](//drive.google.com/open?id=0B0O0wI7T8vtSY2hhWmc4RFF3UVE)：[Sally定时视频](//drive.google.com/open?id=0B0O0wI7T8vtSSm9oaEc0b19YdmM)、[Sally定时示例](//drive.google.com/open?id=0B0O0wI7T8vtSTU02S0lKRlo2UUk)、[图片1](//drive.google.com/open?id=0B0O0wI7T8vtSMnlrbTlFZjhtOGs)和[图片2](//drive.google.com/open?id=0B0O0wI7T8vtSRkVJUjFMUUtoUlk)。

* WhyNot的[Aegisub定时指南](http://whynotsubs.com/A-guide-to-timing-in-Aegisubv2.pdf)，[PDF](//yukisubs.files.wordpress.com/2016/10/a-guide-to-timing-in-aegisubv2.pdf)。

* m33w-fansubs的[定时和样式指南](http://m33w-fansubs.com/timing_guide.php)。

* [skiddiks的](https://yukisubs.files.wordpress.com/2020/09/timing_with_skiddiks_scribbles-1.pdf)。   

* unanimated的《如何制作xvid关键帧》（//unanimated.github.io/scxvid.htm）。

* 对于K-timing，想法是对每个音节的发音进行时间调整。如果您还没有熟记[注音日语音节]（//wiki.anidb.net/w/AniDB_Definition:Romanisation），请保存这些平假名字符映射：[1]（//yukisubs.files.wordpress.com/2017/05/hiragana.png）和[2]（//yukisubs.files.wordpress.com/2017/05/hiragana3.png）。

* 随机的YouTube视频：

   * [Jude Ibe]（//www.youtube.com/watch?v=w6zXR6Bg7fU），[Dozo Douzo]（//www.youtube.com/watch?v=nkTbrCYmKPk）和[Govna]（//www.youtube.com/watch?v=In7nbmsqHWI&list=PLtwIkfU56fRSZgaPHFt79ei1_Kf4cDaFY&index=11）。

####排版

*理论：排版主要是确保字幕对话在视觉上易读，并且标志看起来像是视频的本地部分。排版还可以扩展到样式的开头，结尾和插入歌曲，包括华丽的卡拉OK。[更多理论](//collectr.blogspot.com/search/label/typesetting)。

*排版的最重要部分也是最简单的部分：确保对话易读。查看Underwater的样式指南-PDF（//yukisubs.files.wordpress.com/2018/02/subtitlestyling_byunderwater.pdf）。总结如下：

   1.使用非常浅的颜色作为主要颜色（白色）。

   2.有一个非常暗的边框（黑色）。

   3.使用可读的字体，如Arial或[Roboto]（//fonts.google.com/specimen/Roboto），加粗。

   4.将其放大到足够的大小，无需皱眉。

*虽然排版实际上相当直截了当，但高效地进行排版却是完全不同的事情。

* unanimated的《Aegisub排版指南》（//unanimated.github.io/ts/index.htm），[PDF-White]（//yukisubs.files.wordpress.com/2020/04/typesetting_in_aegisub_by_unanimated_2018_white.pdf），[PDF-Black]（//yukisubs.files.wordpress.com/2020/04/typesetting_in_aegisub_by_unanimated_2018_black.pdf），[PDF-v2015]（//yukisubs.files.wordpress.com/2016/10/unanimated_fansub_guides.pdf）（旧版）。 [RAR-v2015]（//www.mediafire.com/file/t3zkwtzc1t33tpg/TypesettingGuide2015-03-25.rar），[RAR-v2015镜像]（//mega.nz/#F!wUYwDSgA!8tx_37HUBcs9KqPhkk5FmQ）。

* unanimated的[Aegisub脚本]（unanimated.github.io/ts/scripts-unanimated.htm），[PDF]（//yukisubs.files.wordpress.com/2016/10/unanimated_aegisub_scripts.pdf）和[Typesetting Tools]（//github.com/TypesettingTools）。 iamevn的[镜像]（//github.com/iamevn/unanimated-Aegisub-Scripts）。

* Commie的[Aegisub排版]（http://commiesubs.com/interns/ts/index.htm），[PDF]（//yukisubs.files.wordpress.com/2016/10/commie_typesetting_in_aegisub.pdf）和[适用于Aegisub的脚本-ZIP]（//mega.nz/#F!wUYwDSgA!8tx_37HUBcs9KqPhkk5FmQ）。

* [Mocha]（//www.imagineersystems.com/products/mocha-pro），如上述指南中提到的，可用于动态跟踪标志。基本版本的Mocha还原生地包含在Adobe After Effects 11（CS6）及更高版本中。

* lyger的[Aegissub自动化脚本]（//github.com/lyger/Aegisub_automation_scripts）。

*关于[渐变]的简短指南（//yukisubs.files.wordpress.com/2019/11/ongradiants-by-bloodynoyume.pdf），由Bloody No Yume（法国小组）翻译的PDF。

* [Aegisub-Motion]（//github.com/TypesettingTools/Aegisub-Motion）和[指南]（//github.com/TypesettingTools/Aegisub-Motion/wiki）。

*创意排版的想法：[maxfireheart.blogspot.in]（//maxfireheart.blogspot.in）。

*高级：Koby的[ASS Draw Shapes]（//kametsu.com/topic/3090-ass-draw-shapes-for-subtitle-scripts）用于排版和KFX。

* 高级：由Line0编写的[使用Adobe Illustrator排版](//blog.line0.eu/typesetting-with-illustrator-and-ai2ass-part-i-the-basics)及其相关博客。

* 卡拉OK特效（KFX）：

* 理论：这是一种可选的字幕特效子类，可为卡拉OK添加额外的特殊效果。通常，KFX是指超出简单的k-timing之外的效果。可以通过应用KFX模板，修改现有效果或创建新效果来向k-timed行添加KFX。一些KFX可以存在于softsub.ass中，但是其他必须预渲染（硬编码），要么是因为创建它们的工具直接绘制视频流，与k-timing无关，要么是因为动态渲染该效果会导致播放期间的严重卡顿。

* 与所有字幕特效一样，实际上应用KFX可以非常简单，但是创建和修改新的、具有视觉吸引力的KFX则完全是另一回事。[更多介绍](//jockotan.wordpress.com/2015/08/12/the-basics-of-kfx)。

* 先决条件阅读：

  * 如何使用Karaoke模板：[1](http://docs.aegisub.org/manual/Karaoke_Templater_Tutorial_1) 和 [2](http://docs.aegisub.org/manual/Karaoke_Templater_Tutorial_2)。

  * ["我应该从哪里开始学习？"](http://forum.aegisub.org/viewtopic.php?f=13&t=1566)，[PDF](//yukisubs.files.wordpress.com/2017/09/aegisubforums-howtolearnmakingkaraoke-by-jfs.pdf) —jfs介绍了KFX的概念。

* 使用模板：

  * 基础：[由ai-chan创建的kfx模板](http://forum.aegisub.org/viewtopic.php?f=13&t=1222)，[ZIP - Mega](//mega.nz/#F!wUYwDSgA!8tx_37HUBcs9KqPhkk5FmQ)（字幕-kfx）。

  * 推荐：[Kara Effector](//github.com/KaraEffect0r/Kara_Effector) 是Aegisub的Lua插件，专注于修改提供的模板。它有很多基本的修改(形状、颜色、持续时间、数量)很简单。 大部分文档 [PDF](//yukisubs.files.wordpress.com/2017/05/kara-effector-usage-guide-1-39.pdf) 在西班牙语写的。

     * Aegisub 3.2.2的Kara Effector 3.4： [媒体库](//www.mediafire.com/file/bbb2msh84v3y8d3/Kara+Effector+3.4+%5Bfv20.02.17%5D.rar)，[Mega](//mega.nz/#F!wUYwDSgA!8tx_37HUBcs9KqPhkk5FmQ)（字幕-kfx-Kara Effector）和旧版3.3版本需要的括号（//www.mediafire.com/file/s3y4c7m439l113w/Kara+Effector+3.3+%5Bfv24.06.16%5D.rar）。

      * Kara Effector使用指南（1-39）：章节PDF可在 [Mega](//mega.nz/#F!0lVXQKaJ!lOse3jVveeEqWQouBE0ekg) 查看，或者查看这个 [合并PDF（1-39）](//yukisubs.files.wordpress.com/2017/05/kara-effector-usage-guide-1-39.pdf)。

      * [Youtube安装视频](//www.youtube.com/watch?v=AC0YZq1tDDs)，[Facebook页面](//www.facebook.com/karaeffector)，[Youtube主页](//www.youtube.com/channel/UCcFmL4la4IT5HziLd9a_d7w)和一些 [例子](//www.youtube.com/channel/UCJWQDouAf2nxvHJwdYE-Iag)。

      * 随机KE格式化的KFX：Mega [1](//mega.nz/#F!V9Um0JJL!uhcTl3v444RyE8gpqO8lHg) 和 [2，KFX_Archive_May17.zip](//mega.nz/#F!wUYwDSgA!8tx_37HUBcs9KqPhkk5FmQ)（字幕-kfx-Kara Effector）。

* 创建KFX：

  * 再次阅读此文章：["我应该从哪里开始学习？"](http://forum.aegisub.org/viewtopic.php?f=13&t=1566)，[PDF](//yukisubs.files.wordpress.com/2017/09/aegisubforums-howtolearnmakingkaraoke-by-jfs.pdf)，并使用模板。

  * 也可以使用Adobe [After Effects（AE）](http://www.adobe.com/products/aftereffects.html)创建非常专业的KFX。

  * 进一步阅读：Aegisub的 [Automation 4 Lua Overview](http://docs.aegisub.org/3.2/Automation/Lua/)，一些[Lua教程](http://lua-users.org/wiki/TutorialDirectory) 和[Programming in Lua 由Roberto Ierusalimschy（第3版），PDF](//yukisubs.files.wordpress.com/2017/05/programming-in-lua-3ed.pdf)。

  * 更多冒险：NyuFX。[Youtube](//www.youtube.com/playlist?list=PL52E2DB0433C204F2)，[SourceForge](//sourceforge.net/projects/nyufx)和[Github](//github.com/Youka/NyuFX)。

  * 更多冒险2：SSB。[Home thread](http://forum.aegisub.org/viewtopic.php?f=10&t=66095)，[Youtube demo](//www.youtube.com/user/Youkakun/videos)和[SourceForge](//sourceforge.net/projects/ssbrenderer)。

#### 分发（Distro）

#### 分发方法1：种子文件

* 基础知识： [介绍BitTorrent协议](http://bittorrent.org/introduction.html), [初学者指南](//lifehacker.com/285489/a-beginners-guide-to-bittorrent), [维基教科书](//en.wikibooks.org/wiki/The_World_of_Peer-to-Peer_%28P2P%29/Networks_and_Protocols/BitTorrent), [维基百科](//en.wikipedia.org/wiki/BitTorrent).

* 技术：[详细解释Bittorrent](//yukisubs.files.wordpress.com/2016/10/bittorrent_in_detail_tampere_uni_of_technology.pdf), [规范说明](//wiki.theory.org/BitTorrentSpecification), 和 [BEPs](http://bittorrent.org/beps/bep_0000.html)。

* 客户端：

    * 推荐： [qBitTorrent](http://www.qbittorrent.org).跨平台、跨体系结构和开源。

        * [有趣的分支](//github.com/c0re100/qBittorrent-Enhanced-Edition).

    * 只在Windows适用的替代方案： [uTorrent 2.2.1](http://www.oldversion.com/windows/download/utorrent-2-2-1-2) （此精确版本）。

      * 重要：将 [net.discoverable 设置为false](//yukisubs.files.wordpress.com/2018/06/utorrent_settingschange_by_bakabt.png)

      * 有趣的ruby[迁移脚本](https://gist.github.com/naodesu/8c3c6e9bcaf81eb1f4c24b239d232736).

    * 端口转发：[理论介绍](//en.wikipedia.org/wiki/Port_forwarding)和[相关指南](//www.noip.com/support/knowledgebase/general-port-forwarding-guide)。

    * Shana Project的[RSS指南](https://www.shanaproject.com/help/)。

    * 创建种子文件：

        * BakaBT的[如何创建种子文件](http://wiki.bakabt.me/index.php/How_to_create_torrent_files), [PDF版](//yukisubs.files.wordpress.com/2018/02/how_to_create_torrent_files_-_bakabt_wiki.pdf)

       * 用于创建种子的独立实用程序，请参阅 [dottorrent-gui](//github.com/kz26/dottorrent-gui)。

          * 此实用程序还支持AnimeBytes的 ["Source" property extension](//kametsu.com/topic/61665-animebytes-source-property-warning/)。

       * 快速创建种子文件的CLI（高级技巧）[py3createtorrent](//py3createtorrent.readthedocs.io/en/latest/user.html), [下载链接](//bitbucket.org/rsnitsch/py3createtorrent/downloads). 

         * 默认情况下需要[Python 3.1+](//www.python.org/downloads/release), 但可以使用[pyinstaller](//pythonhosted.org/PyInstaller)将其编译为本地二进制文件(.exe)。

    * 之后，将myfile.torrent上传到一些网站。这将在必要时向跟踪器注册它或开始注册过程。添加描述，以便其他对等方知道您提供的内容。

    * 对于自动种子文件提交：

        * Seiya的Anidex种子上传程序：[Kametsu线程](//kametsu.com/topic/60527-anidex-torrent-uploader-upload-torrent-to-multiply-anime-trackers)和[Github](//github.com/seiya-dev/anidex)。

        * Golumpa的[AniDexPy](https://github.com/Golumpa/AniDexPy)。通过其API上传到AniDex的简单Python工具。

    * 注意：这只分发了元文件。要分发内容，请使用[种子盒](//en.wikipedia.org/wiki/Seedbox)。

* 种子盒子理论：

    * [种子盒子](//en.wikipedia.org/wiki/Seedbox)是提供BitTorrent服务的服务器。可以在本地实现，也可以商业租用。

    * 根据[介绍BitTorrent协议](http://bittorrent.org/introduction.html)，任何BitTorrent客户端软件都可以潜在地用作种子盒子软件。

* 就商业而言，Seedbox（SaaS）提供的最流行的客户端是rTorrent，rTorrent ArchWiki和ruTorrent前端。Reddit / r / Seedboxes.有关设置本地种子盒的信息，请参见“面向自己动手（DIY）的发送版”。

* BitTorrent Tracker理论：

    * 由于后端跟踪器软件旨在始终在高性能连接上处于活动状态并需要不断维护，因此不建议运行跟踪器。请改用现有的跟踪器。但是，如果感兴趣，请阅读此处：BitTorrent Tracker Theory。

    * 还有许多低容量的PHP跟踪器，旨在为启用PHP的Web服务器和独立的临时跟踪器软件可执行文件提供服务。

* 杂项教程和指南。

* Distro Method＃2：超文本传输协议（HTTP）（+传输层安全性（TLS））

* 客户：

    * Firefox ESR与此一起使用。

    * 火狐分叉：Palemoon或Waterfox。

    * Chrome。

    * 注意：对于上述图形HTTP客户端，请始终使用uBlock Origin。

    * CLI：Aria2c，wget或cURL。

    * Mega Downloader v1.7，Mega。D8C14D88F6C8B35FDD79CD7D208D818C4683E224的SHA1哈希值

    * JDownloader2支持许多站点特定插件的HTTP连接（下载）的自动恢复。某些德语DDL网站/论坛需要。

* 文件服务器云-直接下载（DDL）：

    * 像Mega这样的云存储提供商为提供大量但有限期限的存储。

    * Anime Tosho将英语翻译的种子内容在Nyaa和TT上镜像到云存储提供商。

    * Amazon、Google和Microsoft以合理的价格提供有限的长期存储。

#### 文件传输协议（FTP）

* 如果您拥有或不介意购买域名，请考虑使用 Google 的[G Suite](//gsuite.google.com/features)以获得成本效益的云存储。

* Web服务器云：

   * 参见：“Misc：The Group Blog”。

* 自托管（HTTP）：

   * 参见“Distro：Seedboxes”和“Misc：Distro For DIY People”章节。

#### Distro Method＃3：Internet Relay Chat（IRC）

* 协议理论：[IRC和Kludges](//esoterictek.blogspot.com/2016/10/internet-relay-chat-irc-and-kludges.html)。

* 指南：Flash Squirrel的[使用IRC进行下载的方法](//forums.animesuki.com/showthread.php?t=3892)，Kametsu的[IRC教程索引](http://kametsu.com/topic/29262-tutorial-index-for-irc)，以及窗口平台和OS / X的IRC客户端安装教程。

* 客户端：[对Internet Relay Chat客户端进行比较](//en.wikipedia.org/wiki/Comparison_of_Internet_Relay_Chat_clients)。

  * 首选：[Hexchat](//hexchat.github.io)，以前称为“xchat”，是开源的，跨平台的，支持有限的脚本。

  * [KVIrc](http://www.kvirc.net)，开源，跨平台，美观。[夜间二进制](//github.com/kvirc/KVIrc/wiki/Downloading-KVIrcs-nightly-source-or-binaries)。

  * [AdiRC](//www.adiirc.com)，封闭源免费软件，跨平台，有许多主题可用。

  * [mIRC](//www.mirc.com)，专有且仅适用于Windows，但具有强大的脚本可用（例如FServe）。[白痴证明安装指南](//www.wikihow.com/Download-Subtitled-Japanese-Anime-from-mIRC)。

  * 还有许多基于Web和移动（iOS / Android）的IRC客户端，不支持DCC。

* FServers

   * 客户端：Keiichi的[Fserve指南](//www.keiichianimeforever.com/guides/irc/fserv.html)，[Microsoft Office文档（doc）](//yukisubs.files.wordpress.com/2016/10/introduction_to_irc_fserves_-_keiichi_anime_forever.doc)，WikiBook的[Fserve指南](//en.wikibooks.org/wiki/Downloading_Files_from_IRC/File_Server_%28fserve%29_Guide)。

   * 服务器：[mIRC FServer设置脚本](//www.sysreset.com)和[随机指南](http://leonardo.spidernet.net/Copernicus/831/mirc/tips5/fserve.html)。

* XDCC

   * 客户端：WikiBook的[使用XDCC指南](//en.wikibooks.org/wiki/Downloading_Files_from_IRC/XDCC_Bot_Guide)和Xertion的[XDCC命令语法](http://wiki.xertion.org/w/XDCC_Commands)。 Xertion指南包括批处理语法。

   * 服务器：[XDCC Bot Guide](http://kasumi.moe/xdccguide)，[PDF](//yukisubs.files.wordpress.com/2016/10/kasumi_xdcc_bot_guide.pdf)，以及[iroffer-dinoex 3.3设置指南](http://iroffer.dinoex.net/INSTALL-linux-en.html)，[doc](//yukisubs.files.wordpress.com/2016/10/installation_-of_iroffer_mod_dinoex_under_linux_as_a_user.doc)。此外：[iroffer-dinoex主页](http://iroffer.dinoex.de/projects/iroffer)。

  * [简化的设置指南](//gist.github.com/gdiaz384/80e0836b27a88d53dc0a9c604b972998)，[iroffer-dinoex-3.30.tar.gz镜像](//mega.nz/#F!wUYwDSgA!8tx_37HUBcs9KqPhkk5FmQ)和[Bot.config文件模板](http://pastebin.com/G5ZUbTCz)。

* 不可以使用这种协议，应该使用HTTP。

#### 新闻组

  * TODO: 这里放东西。

#### 随机发行版工具：

* CRC32：用于在文件名末尾加入CRC32（例如，myfile_[1BA919D7].mkv）：

    * [RapidCRC](//rapidcrc.sourceforge.net)（首选）。

    * 图形用户界面：[Anime Checker](http://animechecker.sourceforge.net)。

    * 命令行界面：[7z h documentation](//sevenzip.osdn.jp/chm/cmdline/commands/hash.htm)。

    * [Bash脚本](//gist.github.com/Golumpa/89e3d3eeb810d7f8f539b61cffe5b29b)。

* 基于MediaInfo的[Avdump2](//wiki.anidb.net/w/Avdump2)。这个工具是用来快速更新[AniDB.net](//anidb.net)的。参见：

    * AniDB [Wiki教程](//wiki.anidb.net/w/Tutorial:How_to_Add_Files_for_Dummies!)和[Prolix Addendum](//wiki.anidb.net/w/Tutorial:How_to_Add_Files_for_Dummies!/The_Prolix_Addendum)，[镜像](//yukisubs.wordpress.com/guides/tutorial-updating-anidb-with-avdump2)。

* line0的[截图解决方案](//forums.bakabt.me/index.php?topic=38998.0)，TODO：[PDF]。

* 截图比较网站：

    * [compare.bakashots.me](http://compare.bakashots.me)（只适用于[BakaBT](//bakabt.me)中的提供）。

    * [diff.pics](https://diff.pics)。

    * [screenshotcomparison.com](http://screenshotcomparison.com)。

*  补丁

    * 理论上，“补丁”是一些小脚本，可以接受一个已有文件，一个差异文件（patch.vcdiff）并创建一个新的基于这些差异的文件。更多理论：[Patches and xdelta3](//esoterictek.blogspot.com/2016/10/patches-and-xdelta3.html)。

    * 指南：

    * moodkiller的[xdelta3 GUI](//kametsu.com/topic/56551-xdelta3-gui-20-v208-a-patch-maker-for-all/)。

    * BakaBT的[打补丁指南](http://wiki.bakabt.me/index.php/Patching)。

* 13ack.Stab's [V2补丁指南](http://www.animepassion.net/topic/485-guide-to-v2-patches).

    * 使用补丁: 简单示例 [FFF的Mirai Niki 7 - Patch](//mega.nz/#F!wUYwDSgA!8tx_37HUBcs9KqPhkk5FmQ) 和 [一些复杂的示例](//mega.nz/#F!Mc4zwDaQ!hJ5xLfs8GzkHqKPxNp2hLQ).

    * 创建补丁:

        * CLI: xdelta3 -e 9 -s old_file new_file delta_file

        * 或者 [xdelta3 GUI](//osdn.net/projects/sfnet_xdelta3-gui) 用于 GUI 界面操作。还可参考: Moodkiller的 [xdelta3重启分支](https://github.com/Moodkiller/xdelta3-gui-2.0).

    * xdelta3.exe 的二进制版本可从上述补丁示例或 [xdelta3 GUI](//osdn.net/projects/sfnet_xdelta3-gui) 中获取。

    

    

#### 团队博客

* 原理: 提供一种集中 有关团队知识的方式，包括以下内容：

    * 最新发布信息、项目档案、下载选项（Torrents/HTTP/XDCC/fserve）、联系信息（IRC/Email）、社区反馈机制（chatbox）、公布的二次元女友、社区指南和募捐要求。

* 入门指南：

    1. （可选）阅读 [互联网和托管提供商](//esoterictek.blogspot.com/2016/10/the-internet-and-hosting-providers.html)，了解互联网运作方式以及服务费用。

    2. （可选）从 [Hover](//hover.com) 购买 mygroup.moe 域名 ，价格约为20美元（每年）。其他注册机构: [get.moe](http://get.moe)。

    3. 在 [Blogger](//www.blogger.com) 或者 [Wordpress](//wordpress.com) 上开启一个博客。

        * 注意: Wordpress 和 Weebly 收取自定义域名费用，Blogger 会禁用 TLS。

    4. 发布版本更新。 [示例](//doki.co)。

* Markdown (博客文章格式)：

    * [Markdown Cheatsheet](//github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

    * [Markdown Preview](//stackedit.io/app), [v4](//stackedit.io/editor) 和 HTML 转换器。

    

    

#### DIY 人群的发行版

* 一般强制阅读

* [互联网和托管提供商](//esoterictek.blogspot.com/2016/10/the-internet-and-hosting-providers.html)

  * 端口转发[理论](//en.wikipedia.org/wiki/Port_forwarding)和相关[指南](//www.noip.com/support/knowledgebase/general-port-forwarding-guide)。

  * [设置服务器](//wiki.installgentoo.com/index.php/Setting_up_a_Server) (包括[VPS](//en.wikipedia.org/wiki/Virtual_private_server)) 和[安全策略](//wiki.installgentoo.com/index.php/Setting_up_a_Server#Recommended_security_policy)。

  * 使用 Crontab [指南1](//help.ubuntu.com/community/CronHowto) 和[指南2 ](http://www.unixgeeks.org/security/newbie/unix/cron-1.html)在启动时启动任务。请参阅：[此示例](//gist.github.com/gdiaz384/343e3704dc1f955e6bd904d384566cb4)。

* DNS / 动态DNS (DDNS)

  * FreeDNS客户端更新协议[客户端列表](//freedns.afraid.org/scripts/freedns.clients.php)，DD-WRT DDNS [指南1](http://www.stevejenkins.com/blog/2014/11/using-freedns-afraid-org-with-dd-wrt-when-you-lose-your-free-dyndns-or-d-link-ddns-account)和[指南2](//freedns.afraid.org/guide/dd-wrt/)。

  * Namecheap的[DDNS信息](https://www.namecheap.com/support/knowledgebase/category.aspx/11/dynamic-dns)和[DDNS主机指南](https://www.namecheap.com/support/knowledgebase/article.aspx/43/11/how-do-i-set-up-a-host-for-dynamic-dns)。

* 树莓派

  * [ 树莓派](//www.raspberrypi.org), 文档[Documentation](//www.raspberrypi.org/documentation)和 [Ebay 搜索链接](//www.ebay.com/sch/i.html?_nkw=raspberry+pi+3b%2B)。 

  * 提示：使用USB上的外部存储而不是Secure Digital (SD)卡内部存储。

  * 确保设置[远程访问](//www.raspberrypi.org/documentation/remote-access)：[SSH](//www.raspberrypi.org/documentation/remote-access/ssh/README.md)，[VNC](//www.raspberrypi.org/documentation/remote-access/vnc/README.md)，( 可能还有 )[Samba](//www.raspberrypi.org/magpi/samba-file-server/)。

* 种子盒子软件

  * [rTorrent](//wiki.archlinux.org/index.php/RTorrent)与[ruTorrent](//wiki.archlinux.org/index.php/RuTorrent)前端由于非常低的资源利用率和高性能而受欢迎。安装和管理通常是自动化的：

  * [Quickbox](//quickbox.io)，[Github](//github.com/QuickBox/QB) （建议使用）。

     * 仅适用于某些Ubuntu/Debian版本的x86_64：

  * arakasi72用于Debian和Ubuntu的“ rtinst”：[Github] (//github.com/arakasi72/rtinst)。注意：我没有测试过这个。

* [qBittorrent](http://www.qbittorrent.org), [Wiki](//github.com/qbittorrent/qBittorrent/wiki)，跨平台和跨架构。

    * sudo apt-get install -y qbittorrent

    * 或编译它以获取最新的v3.x版本：请参阅此[从头开始的脚本](//gist.github.com/YukinoAi/1f58db68c7ef3235addbf001de44fba8)。 或者：

        * [官方编译文档](//github.com/qbittorrent/qBittorrent/wiki/Compiling-qBittorrent-on-Debian-and-Ubuntu)，[arm7编译指令](//gist.github.com/jDmacD/9e38542901b9672728f088abd353a0a1)和[Banana seedbox](https://github.com/qbittorrent/qBittorrent/wiki/Compiling-qBittorrent-on-Raspbian-for-LeMaker-Banana-Pro)。 

        * v4.x需要QT5。 [玩得开心](https://wiki.qt.io/Native_Build_of_Qt_5.4.1_on_a_Raspberry_Pi)。

* HTTP文件服务器

  * [静态HTTP服务器软件列表](//gist.github.com/willurd/5720255)。

  * 考虑使用使用Node.js实现的异步“HTTP-Server”。请参阅：[此指南](//gist.github.com/gdiaz384/94d3800fd5b3465fe7010917563581cd)。

保持markdown语法和符号

* Apache和Nginx通过目录联接递归自动索引Fat32格式卷存在各种问题。只是提供信息~

  * 请勿使用… [HFS ~ HTTP文件服务器](http://www.rejetto.com/hfs)（仅限Windows）。

* TLS

   * 对于加密，使用stunnel：[功能列表](//www.stunnel.org/features.html)，请参阅此[安装指南](//www.digitalocean.com/community/tutorials/how-to-set-up-an-ssl-tunnel-using-stunnel-on-ubuntu)。

   * 对于身份验证，请查看[LetsEncrypt](//letsencrypt.org/docs)以及以下资源：[EFF的Certbot](//certbot.eff.org)，stunnel的[LetsEncrypt配置](//community.letsencrypt.org/t/configure-stunnel/3611)以及有关[正确配置密码套件的配置指南](//weakdh.org/sysadmin.html)。 

   * 还请参阅此TODO：[TLS组合指南]。

   * 设置所有内容后，请使用SSL-Lab的[SSL服务器测试](//www.ssllabs.com/ssltest)来验证配置。

   

#### Remux

* 理论：Remuxers通常专注于改进其他组的工作，结合多个组的工作和/或结合更好的音频/视觉（A / V）来源与字幕。

* 字幕预处理工具：

    * Sushi的[基于音频的字幕移位器](//github.com/tp7/Sushi). [指南](//iamscum.wordpress.com/other-useful-stuff/using-sushi)。

    * eXmendiC的[时间脚本](//iamscum.wordpress.com/auto-fixing-official-subs)。注意：我没有测试过此项。

    * [Notepad++] (//notepad-plus-plus.org)。支持跨多个文件同时进行“查找和替换”。

        * [py3stringReplace] (//github.com/gdiaz384/py3stringReplace)。Notepad ++“查找和替换”的自动化版本。

    * Aegisub的[定时后处理器（TPP）] (http://docs.aegisub.org/manual/Timing_Post-Processor)。

    * Kageru's的[snap_scenechanges.py](//gist.github.com/kageru/0e4b4f0e8b443c59552b66d5f8b55d93)。

    * iamevn的[combine_lines.py](https://gist.github.com/iamevn/b21e60f6a9d572cbc5197a143f46d258)。

* 工作流程：

1. 获取原始数据（请参阅：Capping）。

2. 获取脚本。

    1. 找出哪些分组制作了系列：

         * [Anime DataBase（AniDB）] (//anidb.net)。

* 搜索Nyaa、Anidex.moe、bakabt等网站。

  * 快捷方式：[AnimeTosho](//animetosho.org)的“附件”部分。

  * [ar-fansub-db.blogspot.com](//ar-fansub-db.blogspot.com)和[arfansubdb.com](http://arfansubdb.com)（阿拉伯语，提示：使用Chrome的翻译功能）。

* 从小组获取字幕或文件.mkv。

  * 检查他们的网站以获取HTTP或torrent链接。

  * 检查小组使用的BitTorrent跟踪器。

  * 检查它们的IRC频道并寻找XDCC机器人。

  * 如果您可以找到他们文件的确切名称，请在rizon.net的#news中使用@find并将其提供给Google。

  * 通过IRC或电子邮件向小组提出问题（不太可能奏效）。

  * [这个俄罗斯网站](http://subs.com.ru)有时会有脚本。

    * 如果有必要，请使用[Notepad ++](//notepad-plus-plus.org/download)将字符编码更改为UTF-8。

* 如果您可以获取文件.mkv，则使用流复制或提取它们。 （见：Muxing）

  * 仅针对高级用户：[提取硬字幕](//redonesubs.blogspot.com/p/extracting-hardsubs.html)，[docx](//yukisubs.files.wordpress.com/2016/10/extracting_hardsubs_-_redone_subs_-_20oct16.docx)，由Zalis提供。

    * 追加说明：[提取硬字幕](//jumonjigiri.blogspot.com/p/extracting-hardsubs.html)由Jumonji-Giri提供。

  * 或者：[AVISubDetector](https://www.videohelp.com/software/AVISubDetector)，[guide-PDF](//yukisubs.files.wordpress.com/2018/02/avisubdetector_guide_howtoripthetimingandenglishsubsfromanavifileusingavisubdetector.pdf)+[py3avi2bdnxml](https://github.com/gdiaz384/py3avi2bdnxml)+[BDSup2Sub](https://www.videohelp.com/software/BDSup2Sub)可以创建类似于[此示例](https://imgur.com/a/y7Mz2)的字幕（捷克语示例）。

* 修复任何问题（特别是同步问题和标准化问题）（参见：过滤、编码、TLC、编辑、时间轴制作、排版）。

* 用复用（Mux）来保存更改（见：Muxing）。

  * 在文件名中使用现有小组标签，即使只做了微小的更改，也被认为是无礼的。使用任何其他标签、无标签、一次性标签或您自己的昵称。为了给他们信用，用原始来源小组的名称标注曲目并在任何描述中给他们信用。

  * 记得在文件名的末尾用[ ]放置CRC32（例如myfile_[1BA919D7].mkv）。（参见：Random Distro Tools的详细信息。）

* 分发（见：Distro）。

#### 为混沌服务：模拟

*“数字是精准的练习，而模拟是受控混沌的练习。”-[digitalfaq.com](http://www.digitalfaq.com/guides/video/capture-understand-sources.htm),[Forums](http://www.digitalfaq.com/forum)。

* 模拟视频广播历史：（顺便一提，非常迷人）

  * [模拟通信系统](http://slideplayer.com/slide/3990945/)的演示文稿。

  * YouTube视频：

  * [Technology Connections](//www.youtube.com/channel/UCy0tKL1T7wFoYcxCe0xjN6Q/videos) (YouTube频道)。

     * 在电子电视之前，有[机械电视](//www.youtube.com/watch?v=v5OANXk-6-w)。

     * [菲洛·法恩斯沃斯和电子电视的发明](//www.youtube.com/watch?v=NUaowcXQtOo)。

     * [光线：模拟电视如何工作](//www.youtube.com/watch?v=l4UgZBs7ZGo)。

     * 模拟彩色电视如何工作 [The Beginnings](//www.youtube.com/watch?v=dX649lnKAU0)，第二部分：[Compatible Color](//www.youtube.com/watch?v=InrDRGTPqnE)，第三部分：[more stuff](//www.youtube.com/watch?v=3JFt6t6ijLs)。

     * [这些不是像素：复习版](//www.youtube.com/watch?v=Ea6tw-gulnQ)。

     * [Trinitron：索尼曾经无敌的产品](//www.youtube.com/watch?v=0aFhzGEBQlk)。

   * [为什么电视是29.97帧每秒？](//www.youtube.com/watch?v=3GJUM6pCpew)

* 模拟解码和伪影：

  * 关于伪影的介绍和[电视与视频Comb滤波器](http://www.cockam.com/vidcomb.htm)。

  * [对比Comb滤波器类型](https://www.extron.com/company/article.aspx?id=ntscdb4)。

  * 有趣的[案例研究](https://hometheaterhifi.com/volume_9_2/runco-pfp-11-video-processor-4-2002-part-2.html)。

  * [时间基准校正器（TBC）FAQ](http://www.digitalfaq.com/forum/video-restore/2251-tbc-time-base.html) 和 [前言](http://www.digitalfaq.com/forum/video-restore/1853-alternative-avt-8710-a.html#post9889)。

* 消费者媒体概述和资源：

  * 视频维基百科：[Composite](//en.wikipedia.org/wiki/Composite_video), [S-Video](//en.wikipedia.org/wiki/S-Video), [Component](https://en.wikipedia.org/wiki/YPbPr)。 

  * 音频维基百科：TODO：这里有一些东西。

     * [Toslink还是Coax](http://thewelltemperedcomputer.com/Intro/SQ/Toslink_Coax.htm)？

  * 有趣的[案例研究](//hometheaterhifi.com/volume_8_4/toshiba-sd-K700-dvd-player-12-2001.html)。

  * 录像带家庭影院（VHS）：在磁带上最多可以记录3 MHz的模拟视频，具有240行分辨率。

     * VHS播放器[用户手册索引](http://www.digitalfaq.com/forum/vcr-repair/2668-index-user-manuals.html)。

     * YouTube视频：

* [你的录像机里的不可能的壮举](//www.youtube.com/watch?v=KfuARMCyTvg)。

     * 索尼β录像带系统为何失败：[第1部分](//www.youtube.com/watch?v=FyKRubB5N60) 和 [第2部分](//www.youtube.com/watch?v=v019trxfcmg)。

     * [Beta和VHS的比较](//www.youtube.com/watch?v=_oJs8-I9WtA)。

  * 激光光盘（LD）：数字盘上的高达5 Mhz的模拟视频，分辨率为400-425行。支持CD质量的数字音频，并有时编码了AC3或DTS。

     * NTSC - 262.5行，59.94 Hz；PAL - 312.5行，50 Hz。

     * [论坛](http://forum.lddb.com/)和[reddit](//www.reddit.com/r/LaserDisc/)。相关 [图书馆](https://yukisubs.files.wordpress.com/2018/06/antcufaalb_ld_library.jpg)。

     * Youtube 视频：

     * [激光光盘：简介](//www.youtube.com/watch?v=Eg8tK1LpLS8)

     * [激光光盘的失败：出了什么问题](//www.youtube.com/watch?v=TClRRMFZ7Sw)

     * [激光光盘：特点、鲁莽和演变](//www.youtube.com/watch?v=Nbo2QepTZNY)

     * [DVD：激光光盘的死亡之音](//www.youtube.com/watch?v=cvwuAKi1ZB4)

     * [MUSE Hi-Vision Laserdisc：1994年的蓝光光盘](//www.youtube.com/watch?v=behaBgwnB8M)

     * 光学媒体和激光光盘上最无聊的视频： Pioneer 的 [Video Tuning Fork volume 1](//www.youtube.com/watch?v=G2HBG7HrY7s&list=PLs8mgmDyfwJfhcSCHwcb4R4V0KI0LGCGO)。

         * 请跳过这个。

     * [清洁和抛光激光光盘](https://www.domesday86.com/?page_id=2855)。

     * 进一步观看：[Pioneer CLD-M301 概述](//www.youtube.com/watch?v=L6iyUSnrGk0)。

* 模拟捕捉：这个想法是将模拟音频和视频信号数字化。

  * 数字常问问题 [指南索引](http://www.digitalfaq.com/guides/video.htm)。

  * [了解视频来源](http://www.digitalfaq.com/guides/video/capture-understand-sources.htm)。

  * [数字视频捕捉介绍，录制电视](http://www.digitalfaq.com/guides/video/introduction-record-capture.htm)。

  * VirtualDub 设置指南：[使用 VirtualDub 捕获 AVI](http://www.digitalfaq.com/guides/video/capture-avi-virtualdub.htm) 和 [相关讨论](http://www.digitalfaq.com/forum/video-capture/7427-capturing-virtualdub-settings.html)。

  * 激光光盘捕获硬件的比较通过[截图比较](//originaltrilogy.com/topic/Laserdisc-players-screenshot-comparison/id/12907)。

  * 无损的[HDMI捕捉比较](https://forum.videohelp.com/threads/376473-Lossless-HDMI-capture-devices-comparison-screenshots)（用于直通配置）。

  * [8mm](//www.google.com/search?q=8mm+film+reels&source=lnms&tbm=isch)：[Reddit wiki](//www.reddit.com/r/8mm/wiki/index)。

* VHS:

     * [如何将VHS进行数据提取](http://anarchivism.org/w/How_to_Rip_VHS).

     * [视频硬件推荐;将磁带转换为数字格式的最佳录像机](http://www.digitalfaq.com/guides/video/capture-playback-hardware.htm).

  * LaserDisc:

     * 传统方法: [如何提取 LaserDisc](http://anarchivism.org/w/How_to_Rip_Laserdisc)和[reddit讨论](//www.reddit.com/r/LaserDisc/comments/3eqqhq/ripping_laserdiscs).

     * 新方法: [Doomsday Duplicator](//www.domesday86.com/?page_id=978)，查看[示例结果](//yukisubs.files.wordpress.com/2020/04/domdup_comparison.jpg)。项目[背景介绍](http://abug.org.uk/index.php/2020/07/04/domesday-86-part-1-the-project/?series=vabug-4th-july-2020)。

         * 技术背景: [硬件](//www.domesday86.com/?page_id=2233), [软件](//www.domesday86.com/?page_id=1070), [Laserdisc 解码](https://www.domesday86.com/?page_id=1379).

         * [安装和使用指南](//www.domesday86.com/?page_id=1312).

         * 一旦以原始格式捕获，内容必须在软件中进行解码。因此使用[ld-decode](//github.com/happycube/ld-decode/wiki)，这是一个“软件定义的LaserDisc播放器。”

             * [安装](//github.com/happycube/ld-decode/wiki/Installation), [基本使用指南](https://github.com/happycube/ld-decode/wiki/Basic-usage-of-ld-decode)，以及[vapoursynth中NTSC解码](//github.com/happycube/ld-decode/wiki/Creating-video-from-NTSC-decodes)。

  * 过时但有趣的:

     * [视频工作流: 捕获MPEG-2以制作DVD](http://www.digitalfaq.com/guides/video/dvd-workflows-mpeg2.htm).

     * [创建DVD的好方法(视频工作流)](http://www.digitalfaq.com/guides/video/dvd-workflows.htm).
