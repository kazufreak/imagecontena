# 説　明　資　料

# HP追加内容
- 測り屋時次郎関連へページを追加する。
- 追加内容は、三次元データを視覚的に閲覧できるページ仕様としたい。  
# 追加項目の概要と仕様の説明
三次元データをWeb上で表示することができる[**Potree**](http://www.potree.org/)を導入して、弊社の三次元データサンプルをWebで閲覧できるようにすることがページ追加の目的です。**Potree**は、オープンソースの三次元データWEBレンダラーです。サーバに**Potree**を配置するだけで三次元データをWEB上でレンダリングができるものです。こちらで[XAMPP](https://www.apachefriends.org/jp/index.html/)でローカルサーバーを構築して実際に試した状況を記します。  
1. **XAMPP**の設置場所
   * 今回は **D:/xampp**　としました。   
2. **Potree** をサーバーへ配置
   * **D:/xampp/htdocs** へ [Github](https://github.com/potree/potree)からクローンしてきた　**Potree_1.6** を配置しました。  
3. 閲覧のテスト
   今回は、先ほど配置した **Potree_1.6/examples** 内にある **example** データでテストしてみます。     
   * サーバを起動します。（xampp-controlでXAMPPを立ち上げ、ApacheのStartボタンでサーバー起動     
    ![サーバ起動](https://github.com/kazufreak/imagecontena/blob/master/s1.png "サーバ")   
   * ブラウザを開いて、**localhost**へアクセスします。ここで、「3.閲覧のテスト」で配置した **Potree_1.6/examples** 内へアクセスすることができます。ここでは、 **http://localhost/Potree_1.6/examples/ca13.html** ファイルへアクセスしてみます。  
   ![Potree](https://github.com/kazufreak/imagecontena/blob/master/s2.png "Potree")  
   * 次に弊社のローカルファイルを閲覧してみます。 閲覧用のファイル構成は下記の構成になります。  
   ```
      rootdir
          |---libs
          |---pointclouds
          |---filename.html
          rootdir名、filenameはファイル毎に名前がついています。 
   ```
   * **D:/xampp/htdocs** ディレクトリ内へ閲覧したいフォルダーを配置します。ここでは下記のフォルダー構成としました。 
   ```
            D:/xampp/htdocs/
                        |---point
                                |---libs
                                |---pointclouds
                                |---out.html  
   ```
   * **http://localhost/point/out.html** へアクセスすると閲覧が可能です。   
4. HPへの追加イメージ  
  点群データの閲覧として、[ページのイメージ](http://www.potree.org/)このようなイメージで6ファイル程度をイメージとして配置、クリックすると閲覧できる形を考えています。または **PotreeViewer** が **Youtube** のようにページへ埋め込めればカッコいいかなとも思います。取りあえずは、閲覧用ページを実装して頂ければ嬉しいです。

***
今後の展望として、クライアントと三次元データのやり取り、イメージを共有する目的で、クライアント毎のページが作成できたらいいなと考えています。セキュリティーも個別のアカウント等の設定をすることで保つような仕様ができたらとも思います。しかし、データ容量が大きいことから、サーバー側の容量や、サーバーへの転送方法等を解決してからの話かと思いますので、その辺も相談させて頂きたいと思います。                               
                 
        
    
    
    
    
    
    

