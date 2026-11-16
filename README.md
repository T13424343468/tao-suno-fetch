# tao-suno-fetch

临时取歌通道（老板 2026-11-16 拍板保留）。

## 用法
1. 在页面 HTML 里找到音频直链（Suno 歌曲页 SSR 源码含 `cdn1.suno.ai/{clipUUID}.mp4`）。
2. 需要云端执行时：`gh workflow run fetch.yml --repo T13424343468/tao-suno-fetch -f song_id=<songId>`，产物走 Actions artifact。
3. 公开可取最高音质 = AAC 48kHz stereo ~192kbps（mp4 内音轨无损提取为 m4a）；WAV 需登录付费 Suno 账号，匿名取不到。
4. 注意：release 资产文件名不支持中文，会被吞掉，必须用 ASCII 文件名。
