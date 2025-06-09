<script setup lang="ts">
</script>

<template>
    <h1 class="mB60">ドキュメントでよく使うもの</h1>
    <!-- 見出し要素 -->
    <section>
        <h1>メインタイトル (h1)</h1>
        <h2>セクションタイトル (h2)</h2>
        <h3>サブセクション (h3)</h3>
        <h4>見出し4 (h4)</h4>
        <h5>見出し5 (h5)</h5>
        <h6>見出し6 (h6)</h6>
    </section>

    <!-- 段落 -->
    <p>これは段落のサンプルテキストです。適切な行間とフォントサイズで表示されます。長いテキストも読みやすく調整されています。</p>

    <!-- ボタン -->
    <section>
        <h2>ボタン要素</h2>
        <button>デフォルトボタン</button>
        <button disabled>無効ボタン</button>
    </section>

    <!-- リスト -->

    <section>
        <h2>リスト</h2>
        <h3>順序なしリスト</h3>
        <ul>
            <li>リストアイテム1</li>
            <li>リストアイテム2
                <ul>
                    <li>ネストされたアイテム1</li>
                    <li>ネストされたアイテム2</li>
                </ul>
            </li>
            <li>リストアイテム3</li>
        </ul>

        <h3>順序ありリスト</h3>
        <ol>
            <li>最初のステップ</li>
            <li>次のステップ
                <ol>
                    <li>サブステップA</li>
                    <li>サブステップB</li>
                </ol>
            </li>
            <li>最後のステップ</li>
        </ol>
    </section>

    <!-- 画像 -->
    <section>
        <h2>画像</h2>
        <img src="https://org.pitahex.com/media/s2.png" alt="サンプル画像">
        <p>画像は自動的にレスポンシブになり、適切なサイズと余白が設定されます。</p>
    </section>


    <!-- 水平線 -->
    <hr>

    <!-- テーブル -->

    <section>
        <h2>テーブル要素</h2>
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
    </section>


    <!-- 引用 -->

    <section>
        <h2>引用要素</h2>
        <blockquote>
            <p>これは引用文のサンプルです。左側にボーダーが表示され、背景色も設定されています。</p>
        </blockquote>
    </section>


    <!-- コード -->
    <section>
        <h2>コード要素</h2>
        <p>インラインコード: <code>console.log('Hello World');</code></p>

        <pre><code>// プリフォーマットされたコードブロック
function greeting(name) {
    return `Hello, ${name}!`;
}

const message = greeting('World');
console.log(message);</code></pre>
        <p>コピー: <kbd>Ctrl</kbd> + <kbd>C</kbd></p>
    </section>

    <section>
        <!-- プログレスバー -->

        <h2>プログレスバー要素</h2>

        <h3>通常のプログレスバー</h3>
        <progress value="70" max="100"></progress>

        <h3>テーマ別プログレスバー</h3>
        <progress class="info stripe" value="50" max="100"></progress>

        <h3>アニメーション付きプログレスバー</h3>
        <progress class="animated" value="90" max="100"></progress>

        <h3>不確定プログレスバー</h3>
        <progress></progress>
        <div class="loader-showcase">
            <div class="loader"></div>
            <div class="loader-allow"></div>
        </div>
    </section>
    <section>
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
    </section>

    <section>
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
    </section>

    <section>
        <h2>サーチボックス</h2>
        <form class="wMax768 search-box">
            <input type="search" id="search-input" name="search" placeholder="キーワードを入力してください..." />
            <button type="submit">検索</button>
        </form>
    </section>

    <section>
        <h2>alertシリーズ</h2>

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
    </section>

    <section>
        <h2>アコーディオンサンプル</h2>
        <p>これらの内容はすべてダミーです。</p>

        <details>
            <summary>TEST</summary>
            <p>これはアコーディオンのサンプルです。クリックすると内容が展開されます。</p>
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
    </section>

</template>