## 自動販売機（オブジェクト、DOM、イベント処理）のミニレポート
### Q4-1. Itemクラスのメソッドについて説明せよ。
* showItemListがクラスメソッドである理由を考察せよ。
* 特定の一つの商品だけの処理ではなく複数の商品を扱う処理なため
* buyItemがインスタンスメソッドである理由を考察せよ。
* 特定の一つの商品を購入したときに一つずつ減らす処理をしているから
### Q4-2. 商品の購入ボタンをクリックすると、どのような処理でセルの値が減少するか説明せよ。
* 購入された商品の在庫数のセルをどのようにして特定するのか説明せよ。
* document.getElementById(this.id).innerHTML = this.stock;)のtihs.idで商品番号を特定し、その商品の現在の在庫数をthis.stockで特定している
* 特定したセルの値をどのように変更するのか説明せよ。
* this.stock--;で個数を減らしてdocument.getElementById(this.id).innerHTML = this.stock;で上書きすることで変更している
### Q4-3. 感想
* 今回の課題で苦労したこと
* itemArea.innerHTML += "<tr><td>" + items[i].name + "</td><td>" + items[i].price + "</td><td>"  + "<td id='" + item_list[i].id + "'>"+ items[i].stock + "<td><button type='button' id = 'button"+item_list[i].id +"'>購入</button>" + "</td></tr>";の処理がうまくできずボタンが押せない、商品の在庫が減らないなどが起こり、正確に表示させるのに苦労しました
* 演習を通して理解できたこと
* クラスの適切な定義場所
* document.getElementById()を使用することでHTMLの要素を特定して、.innerHTMLでリアルタイムで変更できること
* この自動販売機プログラムの追加機能や課題など
ルーレットであたりが出たらもう一本でてくる機能
在庫がなくなったら売り切れと表示し購入ボタンを押せなくする
