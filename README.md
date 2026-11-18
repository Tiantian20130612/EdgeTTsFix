# EdgeTTsFix
随便编的EdgeTTs修复器
# Edge TTS 修补器 · 便携版

## 适用
- ClassIsland（内置 Edge_tts_sharp 1.1.x）
- SecRandom 2.3.100（内置 edge_tts 7.2.x，PyInstaller / Python 3.13）
- Windows 10/11 x64，能正常访问 speech.platform.bing.com

## 用法（在目标电脑上）
1. 把整个文件夹解压到任意位置（不要只把 exe 单独拷出来）；
2. 双击 一键修复.cmd或者打开EdgeTTsFix文件夹中的EdgeTTsFix.exe文件；
3. 完成后会：
   - 在 %LOCALAPPDATA%\EdgeTtsFix\app\ 安装中继；
   - 修补本机的 ClassIsland / SecRandom；
   - 写入开机自启（启动文件夹 EdgeTtsFix.cmd）；
   - 立即启动本地中继（127.0.0.1:17321）。
4. 重启 ClassIsland / SecRandom 后即可正常使用 Edge TTS 语音。
5. 设置完成可以删除EdgeTTsFix便携版.zip文件了

## 注意
- 必须保持中继在运行，语音才正常；开机自启会自动拉起它。
- 如果目标电脑的 SecRandom 不是 2.3.100（例如 3.x），
  修补器检测到内嵌 Python 版本不一致会自动跳过 SecRandom，不会损坏程序。
- 还原：双击 还原.cmd。
- 日志：%LOCALAPPDATA%\EdgeTtsFix\ 下的 relay.log / patch.log / hook.log。
