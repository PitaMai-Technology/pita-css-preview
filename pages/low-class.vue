<script setup>
</script>

<template>

    <div class="">
        <h1 class="text-center">PitaCSS 低水準クラス サンプル</h1>

        <div class="card p20">
            <p>このカードは.cardというクラスです。これはデモをわかりやすく見せるためのクラス(カード)です。
                PitaCSSには内包されていません。<code>.card</code>
            </p>
        </div>

        <section>
            <h2>マージン・パディングクラス</h2>
            <div class="card p20 mB20">
                <p class="mB10">マージンとパディングを使った例:</p>
                <div class="p10 mL10 mR10" style="background-color: var(--gray-secondary);">
                    <span class="text-sm">p10 mL10 mR10 が適用された要素</span>
                </div>
                <div class="pY20 pX20 mT10" style="background-color: var(--gray-tertiary);">
                    <span class="text-sm">pY20 pX20 mT10 が適用された要素</span>
                </div>
            </div>
        </section>

        <section>
            <h2>幅とコンテンツ配置</h2>
            <div class="p20 mB20">
                <div class="w100 p10 mB10" style="background-color: var(--gray-secondary);">
                    <span class="text-sm">w100 (幅100%)</span>
                </div>
                <div class="w50 p10 mB10" style="background-color: var(--gray-secondary);">
                    <span class="text-sm">w50 (幅50%)</span>
                </div>
                <div class="fit-content p10 content-center" style="background-color: var(--gray-secondary);">
                    <span class="text-sm">fit-content + content-center</span>
                </div>
            </div>
        </section>

        <section>
            <h2>レスポンシブ表示制御</h2>
            <div class="card p20 mB20">
                <p class="mB10">画面幅を変更して表示の変化を確認してください！モバイル(SP)では見えたり、パソコンでは見えなかったりなどします！</p>

                <div class="demo-box p10 mB10 hide-max768">
                    <p class="text-center demo-text">
                        📱 hide-max768: 768px以下で非表示<br>
                        <span class="text-sm">（モバイル画面では見えません）</span>
                    </p>
                </div>

                <div class="demo-box p10 mB10 hide-min768">
                    <p class="text-center demo-text">
                        💻 hide-min768: 768px以上で非表示<br>
                        <span class="text-sm">（デスクトップ画面では見えません）</span>
                    </p>
                </div>

                <div class="demo-box p10 mB10 hide-max1250">
                    <p class="text-center demo-text">
                        🖥️ hide-max1250: 1250px以下で非表示<br>
                        <span class="text-sm">（デスクトップでのみ表示）</span>
                    </p>
                </div>

                <div class="demo-box p10 mB10 hide-min1250">
                    <p class="text-center demo-text">
                        📺 hide-min1250: 1250px以上で非表示<br>
                        <span class="text-sm">（デスクトップでは見えません）</span>
                    </p>
                </div>
            </div>
        </section>

        <section>
            <h2>フォントサイズクラス</h2>
            <div class="card p20 mB20">
                <p class="text-xs mB10">text-xs: とても小さいテキスト(13px固定)</p>
                <p class="text-sm mB10">text-sm: 小さいテキスト(15px固定)</p>
                <p class="text-base mB10">text-base: 基本サイズのテキスト(Clamp関数によりレスポンシブです)</p>
                <p class="text-lg mB10">text-lg: 大きいテキスト(Clamp関数によりレスポンシブです)</p>
                <p class="text-xl mB10">text-xl: より大きいテキスト(Clamp関数によりレスポンシブです)</p>
                <p class="text-2xl mB10">text-2xl: 最大サイズのテキスト(Clamp関数によりレスポンシブです)</p>
            </div>
        </section>

        <section>
            <h2>テキスト配置</h2>
            <div class="card p20 mB20">
                <p class="text-left mB10">text-left: 左寄せテキスト</p>
                <p class="text-center mB10">text-center: 中央寄せテキスト</p>
                <p class="text-right mB10">text-right: 右寄せテキスト</p>
            </div>
        </section>

        <section>
            <h2>ボタンとリンク</h2>
            <div class="card p20 mB20">
                <button class="mR10 mB10">デフォルトボタン</button>
                <button class="mR10 mB10">ホバーしてみてください</button>
                <br>
                <a href="#" class="mR10">通常のリンク</a>
                <a href="#" class="inherit-link">inherit-link クラス</a>
            </div>
        </section>

        <section>
            <h2>組み合わせ例</h2>
            <div class="card p20">
                <div class="content-center mB20">
                    <h2 class="text-2xl text-center mB10">タイトル</h2>
                    <p class="text-center text-sm text-muted">サブタイトル</p>
                </div>

                <div class="pX20 pY10 mB10" style="background-color: var(--gray-secondary); border-radius: 4px;">
                    <p class="text-base mB10">これは低水準クラスのみで構成されたコンテンツエリアです。</p>
                    <p class="text-sm">マージン、パディング、幅、フォントサイズなどの基本的なクラスを組み合わせて作成されています。</p>
                </div>

                <div class="text-center">
                    <button class="text-sm pX20">アクションボタン</button>
                </div>
            </div>
        </section>
    </div>

</template>

<style scoped>
/* カスタムカード風デザイン */
.card {
    background-color: var(--gray-primary);
    border: 1px solid var(--border-primary);
    border-radius: 8px;
    box-shadow: var(--shadow-sm);
}
</style>