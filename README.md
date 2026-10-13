# 40代の見た目リセット

Instagram `@taka_reset40` のリンク先サイト。

| パス | 内容 |
|---|---|
| `index.html` | ハブページ（プロフィールのリンク先） |
| `aga/index.html` | 40代のAGAクリニック選び |
| `zenshin/index.html` | 40代の全身脱毛選び |
| `kao/index.html` | 40代の顔のたるみ・しわ・くすみ改善 |
| `hige/index.html` | 旧ヒゲ脱毛ページ。`zenshin/` へ転送するだけ |

## 編集のしかた

`aga/`・`zenshin/`・`kao/`・`hige/` は自動生成されるので **直接編集しない**。
ひとつ上の階層にあるソースを編集して、ビルドし直す。

```
../aga-clinic-lp.html    ->  aga/index.html
../zenshin-datsumo-lp.html  ->  zenshin/index.html
../kao-care-lp.html        ->  kao/index.html
```

```bash
cd .. && python3 build.py
```

CTAリンク（`href="#"`）の差し替えもソース側で行う。

`index.html` はソースを持たないので直接編集してよい。

## 公開

GitHub Pages（Settings → Pages → Deploy from a branch → main / root）。
