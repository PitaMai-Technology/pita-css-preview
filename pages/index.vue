<script>
</script>

<template>
    <!-- 見出し要素 -->
    <h1 class="mB20">メインタイトル (h1)</h1>
    <h2 class="mB20">セクションタイトル (h2)</h2>
    <h3 class="mB20">サブセクション (h3)</h3>
    <h4 class="mB20">見出し4 (h4)</h4>
    <h5 class="mB20">見出し5 (h5)</h5>
    <h6 class="mB20">見出し6 (h6)</h6>

    <!-- 段落 -->
    <p>これは段落のサンプルテキストです。適切な行間とフォントサイズで表示されます。長いテキストも読みやすく調整されています。</p>

    <!-- ボタン -->

    <h2 class="mB20">ボタン要素</h2>
    <button>デフォルトボタン</button>
    <button class="info">情報ボタン</button>
    <button class="success">成功ボタン</button>
    <button class="warning">警告ボタン</button>
    <button class="error">エラーボタン</button>
    <button disabled>エラーボタン</button>


    <!-- リスト -->

    <h2 class="mB20">リスト要素</h2>
    <ul class="mB20">
        <li>順序なしリストの項目1</li>
        <li>順序なしリストの項目2</li>
        <li>順序なしリストの項目3</li>
    </ul>

    <ol>
        <li>順序ありリストの項目1</li>
        <li>順序ありリストの項目2</li>
        <li>順序ありリストの項目3</li>
    </ol>


    <!-- 画像 -->

    <h2 class="mB20">画像要素</h2>
    <img src="https://org.pitahex.com/media/s2.png" alt="サンプル画像">


    <!-- 水平線 -->
    <hr>

    <!-- テーブル -->

    <h2 class="mB20">テーブル要素</h2>
    <table>
        <thead>
            <tr>
                <th>項目1</th>
                <th>項目2</th>
                <th>項目3</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>データ1-1</td>
                <td>データ1-2</td>
                <td>データ1-3</td>
            </tr>
            <tr>
                <td>データ2-1<small>補足情報</small></td>
                <td>データ2-2</td>
                <td>データ2-3</td>
            </tr>
            <tr>
                <td>データ3-1</td>
                <td>データ3-2</td>
                <td>データ3-3</td>
            </tr>
        </tbody>
    </table>


    <!-- 引用 -->

    <h2 class="mB20">引用要素</h2>
    <blockquote>
        <p>これは引用文のサンプルです。左側にボーダーが表示され、背景色も設定されています。</p>
    </blockquote>


    <!-- コード -->

    <h2 class="mB20">コード要素</h2>
    <p>インラインコード: <code>console.log('Hello World');</code></p>

    <pre><code>// プリフォーマットされたコードブロック
function greeting(name) {
    return `Hello, ${name}!`;
}

const message = greeting('World');
console.log(message);</code></pre>


    <!-- プログレスバー -->

    <h2 class="mB20">プログレスバー要素</h2>

    <h3 class="mB20">通常のプログレスバー</h3>
    <progress value="70" max="100"></progress>

    <h3 class="mB20">テーマ別プログレスバー</h3>
    <progress class="info stripe" value="50" max="100"></progress>
    <progress class="success" value="80" max="100"></progress>
    <progress class="warning" value="60" max="100"></progress>
    <progress class="error" value="30" max="100"></progress>

    <h3 class="mB20">アニメーション付きプログレスバー</h3>
    <progress class="animated" value="90" max="100"></progress>

    <h3 class="mB20">不確定プログレスバー</h3>
    <progress></progress>
    <progress class="info"></progress>
    <progress class="success"></progress>
    <progress class="warning"></progress>
    <progress class="error"></progress>


    <!-- セクションの背景色交互表示のデモ -->

    <h2 class="mB20">セクション1（奇数番目）</h2>
    <p>このセクションは奇数番目なので背景色が設定されています。</p>



    <h2 class="mB20">セクション2（偶数番目）</h2>
    <p>このセクションは偶数番目なので通常の背景色です。</p>



    <h2 class="mB20">セクション3（奇数番目）</h2>
    <p>再び背景色が設定されたセクションです。</p>


    <NuxtLink to="/test">Test</NuxtLink>


    <div class="loader-showcase">
        <div class="loader"></div>
        <div class="loader-allow"></div>
    </div>

    <form>

        <label for="name">お名前</label>
        <input type="text" id="name" placeholder="山田太郎" required>

        <label for="email">メールアドレス</label>
        <input type="email" id="email" placeholder="example@email.com" required>

        <label for="password">パスワード</label>
        <input type="password" id="password" placeholder="8文字以上" minlength="8" required>

        <label for="age">年齢</label>
        <input type="number" id="age" placeholder="25" min="0" max="120">

        <label for="birthday">生年月日</label>
        <input type="date" id="birthday">

        <label for="phone">電話番号</label>
        <input type="tel" id="phone" placeholder="090-1234-5678" pattern="[0-9]{3}-[0-9]{4}-[0-9]{4}">

        <label for="website">ウェブサイト</label>
        <input type="url" id="website" placeholder="https://example.com">


        <label for="prefecture">都道府県</label>
        <select id="prefecture" required>
            <option value="">選択してください</option>
            <option value="tokyo">東京都</option>
            <option value="osaka">大阪府</option>
            <option value="kyoto">京都府</option>
            <option value="kanagawa">神奈川県</option>
        </select>

        <label for="message">メッセージ</label>
        <textarea id="message" rows="5" placeholder="ご質問やご要望をお書きください" required></textarea>

        <label for="file">ファイル添付</label>
        <input type="file" id="file" accept=".pdf,.doc,.docx">
    </form>


    <h2>フォーカス・エラー状態テスト</h2>
    <p>以下の要素をクリックしてフォーカス状態を確認し、無効な値を入力してエラー状態をテストしてください。</p>

    <form>
        <label for="test-email">メール（エラーテスト）</label>
        <input type="email" id="test-email" placeholder="無効なメールを入力してみてください" required>
        <small>有効なメールアドレスを入力してください</small>

        <label for="test-number">数値（エラーテスト）</label>
        <input type="number" id="test-number" min="10" max="100" placeholder="10-100の範囲で入力" required>
        <small>10から100の間で入力してください</small>

        <label for="test-url">URL（エラーテスト）</label>
        <input type="url" id="test-url" placeholder="無効なURLを入力してみてください" required>
        <small>有効なURLを入力してください（https://example.com）</small>
    </form>



    <h2 class="mB20">alertシリーズ</h2>

    <div class="alert info">
        <p>tseet</p>
    </div>

    <div class="alert success">
        <p>tseet</p>
    </div>

    <div class="alert warning">
        <p>tseet</p>
    </div>
    <div class="alert error">
        <p>tseet</p>
    </div>

    <h2 class="mB20">アコーディオンサンプル</h2>

    <details>
        <summary>2025年5月31日 電気通信事業者の届出が関東総合通信局に受理されました。</summary>
        <p>この度、弊社の電気通信事業者としての届出が正式に関東総合通信局に受理されました。これにより、より安全で信頼性の高い通信サービスを提供できるようになります。</p>
        <p>今後とも変わらぬご愛顧のほど、よろしくお願いいたします。</p>
    </details>

    <details>
        <summary>2025年5月20日 新サービスの提供開始について</summary>
        <p>新しいクラウドサービスの提供を開始いたします。詳細につきましては、以下の内容をご確認ください。</p>
        <ul>
            <li>サービス開始日：2025年6月1日</li>
            <li>対象エリア：全国</li>
            <li>料金プラン：月額1,000円〜</li>
        </ul>
    </details>

    <details>
        <summary>2025年5月15日 システムメンテナンスのお知らせ</summary>
        <p>下記日程でシステムメンテナンスを実施いたします。</p>
        <p><strong>メンテナンス日時：</strong>2025年5月25日（日）午前2:00〜午前6:00</p>
        <p>メンテナンス中はサービスをご利用いただけません。ご迷惑をおかけしますが、何卒ご理解のほどよろしくお願いいたします。</p>
    </details>

    <details>
        <summary>よくある質問：料金について</summary>
        <p>料金に関するよくある質問をまとめました。</p>
        <h4>Q. 月額料金はいくらですか？</h4>
        <h1>メインコンテンツ</h1>
        <p>ここにページの主要なコンテンツが表示されます。</p>
        <p>ナビゲーションはレスポンシブ対応しており、モバイルでは自動的に隠れます。</p>

        <h2>機能説明</h2>
        <ul>
            <li>デスクトップ：固定サイドナビゲーション</li>
            <li>モバイル：ハンバーガーメニュー形式</li>
            <li>スムーズなアニメーション</li>
            <li>ネストされたメニュー対応</li>
        </ul>
        <p>A. 基本プランは月額1,000円からご利用いただけます。</p>
        <h4>Q. 支払い方法は何がありますか？</h4>
        <p>A. クレジットカード、銀行振込、コンビニ払いに対応しています。</p>
    </details>

</template>