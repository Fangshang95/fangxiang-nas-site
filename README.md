# 方享 NAS · Fangxiang NAS

> 私有家庭 NAS。照片、视频和文件留在你自己的设备上，云端只做账号、信令和元数据。

方享 NAS 是一个面向家庭的自托管 NAS 应用：手机、PC 和电视访问同一台家庭节点，支持局域网直连、远程 P2P、相册时间线、WebDAV 共享、版本历史与影视库整理。文件本体不会上传到本项目或 TMDB。

**Status:** development preview (M1–M6.3). Non-commercial, personal/family use.

## 功能 / Features

- 私有家庭存储：手机 / PC / TV 访问家庭节点，局域网优先，远程 P2P 或限速中继。
- 文件与相册：分片上传、秒传、断点续传、缩略图、照片时间线、EXIF/GPS 索引、重复照片清理。
- 家庭权限：Owner / Admin / Member / Guest，邀请、配额、角色、审计。
- WebDAV 共享：把“我的文件 / 共享空间”挂载到电脑或第三方 WebDAV 客户端。
- 版本历史：覆盖上传生成版本，支持回滚、删除历史、保留策略与自动清理。
- 影视库：扫描本地电影/剧集文件，解析片名、年份、季集，关联字幕，记录播放进度与收藏。
- TV 端：局域网发现、4 位配对码、文件列表与视频播放。

## TMDB API usage

TMDB integration is **optional and disabled by default**. When a node owner configures a TMDB API key, 方享 NAS uses TMDB only to look up metadata for files that are already stored on the user's own device:

- searches by title and year;
- reads title, year, overview, poster/backdrop paths and basic TV season/episode metadata;
- does **not** upload video, audio, photos, documents or file contents;
- does **not** expose the API key to the cloud gateway, other users or third parties;
- is intended for **non-commercial personal and family use** only.

Without a TMDB key, the application still works with offline filename parsing and manual identification.

## Privacy

- Files stay on the user's own NAS node.
- The cloud gateway stores account, device, signaling, quota and metadata only; no file bodies.
- WebDAV credentials and device keys are stored on the node, not in this repository.

## Not affiliated with TMDB

This product uses the TMDB API but is not endorsed or certified by TMDB.

https://www.themoviedb.org/

## Contact

Please use the **Issues** tab of this repository for project questions.

---

# Fangxiang NAS (English)

Fangxiang NAS is a private, self-hosted family NAS. Phones, PCs and TVs access a node in the user's home; files never leave the user's devices. TMDB is used only for optional movie/TV metadata lookup (title/year → overview/poster), never for uploading media. The project is non-commercial and intended for personal/family use. This product uses the TMDB API but is not endorsed or certified by TMDB.
