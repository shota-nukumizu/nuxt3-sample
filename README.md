 # Nuxt3でAPIデータを抽出する方法

## API Routes

 Nuxt3では、[API Routes](https://v3.nuxtjs.org/guide/features/server-routes)を活用すればNextのようなAPIサーバを開発できる。

 API Routeは`/server/api/`配下で作成する必要がある。それぞれのファイルは`req`や`res`を受け取る関数をデフォルトでエクスポートしておく必要がある。

 以下のようにすれば、簡単にサーバを開発できる。

 `server/api/hello.ts`

 ```ts
export default () => 'Hello Nuxt3 from server!'
 ```

 [JSONPlaceholder](https://jsonplaceholder.typicode.com/)からデータを取得してそれを返却するAPIサーバを作成する。


# 余談

**Nuxt3でAPIサーバを開発できることは初耳だった。ここは盲点だった。**NuxtでAPIのデータを抽出するのに1時間半かかってしまった。(あまり情報量が少ないのが主な原因として挙げられるが...)

 # 参考サイト

 [Nuxt3の新しい機能](https://zenn.dev/azukiazusa/articles/nuxt3-new-features#usefetch/useasyncdata)